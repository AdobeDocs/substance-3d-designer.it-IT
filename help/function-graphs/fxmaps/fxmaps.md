---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Scoprite come utilizzare FXMaps in Substance 3D Designer per applicare grafici a funzioni alle texture per la generazione di pattern procedurali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# FXMaps

**Il nodo FX-Map consente la creazione delle immagini procedurali**. È una delle caratteristiche più potenti della tecnologia di Substance.

FX-Map rappresenta un particolare tipo di grafico, noto come catena di Markov. Le catene di Markov rappresentano un semplice processo di base: replicare e suddividere ripetutamente un&#39;immagine. Ad ogni passaggio, un’immagine può essere ruotata, tradotta e fusa a proprio piacimento. I risultati possono essere di qualsiasi tipo, da semplici pattern a rumori complessi. FX-Maps è la base per molte delle Substance di esempio installate con Substance 3D Designer.

## Creare grafici FX-Map

Per visualizzare un grafico FX-Map, è sufficiente aggiungere un [nodo FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) a un [grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md), quindi fare clic con il pulsante destro del mouse sul nodo e premere CMD + E (OS X) o CTRL + E (Windows) per aprire il grafico. Questo grafico FX-Map verrà visualizzato in una nuova scheda del pannello Grafici; per passare da questo grafico a quello di Substance e viceversa, fate clic sulla scheda.

## A cosa servono FX-Maps?

Gli usi più comuni di FX-Maps sono la creazione di pattern ripetitivi, come strisce e mattoni, e rumori, come Perlin, Brownian e Gaussian. I rumori sono particolarmente utili per la creazione di texture organiche dall’aspetto naturale come dirt, dust, calcestruzzo, superfici in pietra, macchie liquide e così via.

I grafici FX-Map non funzionano allo stesso modo dei grafici a Substance: nei grafici a Substance, ogni nodo è indipendente e non ha alcuna conoscenza della sua posizione nel grafico complessivo, né importa da dove provengono i suoi dati immagine o dove sta andando.

Nel capitolo successivo esamineremo più dettagliatamente ciascuno dei tre nodi del grafico FX-Map, ma in breve ciascun nodo FX-Map offre una delle tre operazioni seguenti:

### Quadrante

In questo modo, l’immagine viene divisa in quattro quadranti. Si tratta del tipo di nodo più comune. Una catena di nodi quadranti può creare immagini dall&#39;aspetto molto complesso, nonché pattern complessi.

In effetti, i nodi quadranti rappresentano un livello, o **ottava**, in un grafico a quattro alberi. I grafici FX-Map nascondono questa struttura ad albero rappresentando ogni livello dell&#39;albero con un singolo quadrante: ogni volta che si collega un nodo Quadrante a un altro, si crea in realtà un livello di albero completo.

Il motivo di questa tecnica di &quot;imbroglio&quot; è quello di rimuovere la necessità di rappresentare ogni nodo a ogni livello di un albero singolarmente: dopo solo quattro strati di profondità, sarebbe necessario utilizzare 4 x 4 x 4 x 4 nodi, che è 256 nodi singoli! Al contrario, ogni nodo del Quadrante &quot;sa&quot; a quale livello si trova nell&#39;albero e genera le sue immagini di conseguenza.

Questo probabilmente non avrà molto senso per molti lettori, ma a breve approfondiremo questo argomento in modo molto più dettagliato.

### Iterazione

Ripete l’immagine passata al connettore di destra sull’immagine passata al connettore di sinistra per il numero di iterazioni impostato.

Questo nodo viene spesso utilizzato con uno o più grafici di Funzioni dinamiche per spostare o ruotare in qualche modo l’immagine di input in ogni iterazione.

### Cambia

Questa operazione richiede due ingressi e permette di passare dall&#39;uno all&#39;altro, in base alle impostazioni del selettore. Come per il nodo iterazione, l&#39;impostazione Selettore viene spesso scelta da una Funzione dinamica.

## Variabili di sistema FX-Maps

FX-Maps supporta le variabili di sistema. Queste variabili iniziano sempre con il simbolo del dollaro (&quot;$&quot;) e sono le seguenti:

| Nome | Particolarità | Tipo di dati | Scopo |
| --- | --- | --- | --- |
| $time | - | float1 | Questa variabile restituisce il tempo in secondi dall&#39;avvio del motore di rendering della Substance.È ideale per Substance che devono essere animate in base al tempo. (E.g. in alcune applicazioni, tra cui Substance Player, una Substance che utilizza $time causerà la visualizzazione di una linea temporale nell&#39;interfaccia utente. |
| $profondità | - | float1 | Restituisce il numero di ottava (livello) del nodo FX-Map. Ciò consente a un nodo di modificare il proprio comportamento in base al livello nell&#39;albero quadruplo che rappresenta. |
| $depthpow2 | - | float1 | Come sopra, ma restituisce 2 elevato alla potenza del numero di ottava (livello). Si tratta di un valore di supporto utile per alcuni calcoli comuni. |
| $number | Esegui iterazione solo dei nodi | float1 | Restituisce il numero del pattern disegnato. È possibile accedere a questa funzionalità mediante i grafici Dynamic Function che controllano un nodo Iterate per modificarne il comportamento in ogni fase dell&#39;iterazione. Si noti che $number inizia a contare da 0, non da 1. |
| $size | - | float2 | Restituisce le dimensioni del nodo corrente in pixel. |
| $sizelog2 | - | float2 | Come sopra, ma restituisce le dimensioni come valori di potenza di 2 (ad esempio, per l&#39;immagine 2048\*2048, $sizelog2 restituisce 11). |
| $pos | Solo nodi quadranti | float2 | Restituisce la posizione di nascita del pattern. Il risultato è sempre un valore compreso tra 0 e 1. |
