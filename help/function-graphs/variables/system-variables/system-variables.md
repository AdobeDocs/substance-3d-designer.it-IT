---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: Scopri le variabili di sistema incorporate disponibili nei grafici delle funzioni di Substance 3D Designer per i flussi di lavoro avanzati.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variabili incorporate
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# Variabili incorporate

È possibile utilizzare le variabili incorporate nei [grafici delle funzioni Substance](../../../function-graphs/function-graphs.md) per accedere a valori specifici. Iniziano sempre con un simbolo `$` (Dollaro).

Alcune variabili sono disponibili solo in contesti specifici.

<b>Tutti i nodi</b>

Variabili di sistema

| Nome | Tipo | Scopo |
| --- | --- | --- |
| $size | Float2 | Restituisce la dimensione del nodo corrente in pixel.   Se utilizzato nel parametro [Dimensione output](../../../compositing-graphs/output-size/output-size.md) impostato su un *Relativo a...* [metodo di ereditarietà](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), restituisce il *valore ereditato*. |
| $sizelog2 | Float2 | Come sopra, ma restituisce le dimensioni come valori di potenza di 2 (ad esempio, per l&#39;immagine 2048\*2048, `$sizelog2` restituisce 11).   Se utilizzato nel parametro [Dimensione output](../../../compositing-graphs/output-size/output-size.md) impostato su un *Relativo a...* [metodo di ereditarietà](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), restituisce il *valore ereditato*. |
| $pixelratio | Intero | Restituisce un valore intero corrispondente alle proporzioni in pixel del nodo corrente (ereditato o assoluto): 0: Stretch 1: Square |
| $tiling | Intero | Restituisce un valore intero corrispondente alla modalità di suddivisione in porzioni del nodo corrente (ereditata o assoluta): 0: Nessuna porzione 1: Porzione orizzontale 2: Porzione verticale 3: Porzione H e V |
| $phyalsize | Float3 | Restituisce il valore della proprietà <b>Dimensioni fisiche</b> del [grafico.](../../../compositing-graphs/graph-parameters/graph-parameters.md) |
| $uvtile | Integer2 | Quando si utilizzano flussi di lavoro UDIM, questa variabile restituisce l&#39;indice dell&#39;udim corrente in U e V.   Esempio: (2, 0) per il riquadro 1003, (7, 11) per il riquadro 1118, ... |

<b>FX-Map</b>

Variabili di sistema

| Nome | Tipo | Scopo |
| --- | --- | --- |
| $pos | Float2 | Restituisce la posizione di nascita del pattern. L’origine (0, 0) si trova nell’angolo in alto a sinistra dell’immagine. |
| $profondità | A virgola mobile | Restituisce il numero di ottava (livello) del nodo [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md). Ciò consente a un nodo di modificare il proprio comportamento in base al livello nell&#39;albero quadruplo che rappresenta. |
| $depthpow2 | A virgola mobile | Come sopra, ma restituisce l&#39;inverso moltiplicativo di 2 elevato alla potenza del numero di ottava (livello) - cioè 1/(2^ottava). Si tratta di un valore di supporto utile per alcuni calcoli comuni. |
| $number | A virgola mobile | Restituisce il numero del pattern disegnato. È possibile accedere a questo elemento tramite i grafici di Dynamic Function che controllano un nodo [iterate](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md) per modificarne il comportamento in ogni passaggio dell&#39;iterazione.   `$number` inizia il conteggio da 0, non da 1.   Quando si utilizza una catena di nodi Iterate, la variabile `$number` restituirà il numero di iterazione dell&#39;ultimo nodo Iterate connesso prima del parametro di funzione utilizzato. Se si desidera recuperare il numero di iterazione da più nodi Iterate, è necessario utilizzare le &quot;variabili personalizzate&quot; attraverso i nodi [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md). |

<b>Processore pixel</b>

Variabili di sistema

| Nome | Tipo | Scopo |
| --- | --- | --- |
| $pos | Float2 | Restituisce la posizione del pixel da valutare. |

<b>Globale</b>

Variabili di sistema

| Nome | Tipo | Scopo |
| --- | --- | --- |
| $time | A virgola mobile | Questa variabile restituisce il tempo in secondi dall&#39;avvio della Substance Engine. Può essere usato nei grafici che il risultato dovrebbe cambiare in base al tempo trascorso.  **Nota:** sebbene non sia possibile apportare questa modifica di valore in Designer, le applicazioni che integrano la Substance Engine possono sfruttarla, ad esempio [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) per l&#39;animazione o [Substance 3D Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home) per [tratti dinamici](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes). |
| $normalformat | Intero | Il formato normale (ad esempio, DirectX o OpenGL) utilizzato nell’ambiente corrente.  **Nota:** questa variabile non ha alcun effetto in Designer e può essere utilizzata da altre applicazioni che integrano la Substance Engine. |
