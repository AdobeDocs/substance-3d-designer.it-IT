---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Scoprite i concetti chiave dei grafici per la composizione delle Substance, inclusi nodi, connessioni e nozioni di base del flusso di lavoro.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Concetti fondamentali del grafico Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 1%

---


# Concetti fondamentali del grafico Substance

Questa pagina elenca i concetti importanti da comprendere per lavorare con i grafici a Substance in Substance 3D Designer.

## Sottografi/Pubblicazione

[La pubblicazione di un grafico](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) o la creazione di un sottografo sono due concetti astratti molto simili. Ciò significa che qualsiasi grafico o rete di nodi può essere &quot;impacchettato&quot; insieme e trasformato in una risorsa riutilizzabile e autonoma. La creazione di [sottografi](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) viene eseguita principalmente all&#39;interno dell&#39;applicazione per rendere riutilizzabili determinati contenuti in un flusso di lavoro efficiente e intelligente, in quanto questo evita la duplicazione ripetuta di un set di nodi. La pubblicazione comporta un passaggio aggiuntivo per esportare in formato risorsa Substance 3D (SBSAR), rendendo il grafico della rete dei nodi utilizzabile al di fuori dell&#39;applicazione, ad esempio quando si crea un materiale per il motore irreale.

Input, Output e Parametri esposti sono estremamente importanti per questo concetto, in quanto sono gli unici modi per interagire ancora con il grafico una volta utilizzato come sottografo o come risorsa Substance 3D pubblicata. I motivi sono i seguenti:

* Nessun output significa che il grafico <b>non genera nulla,</b> nessun dato.
* Nessun parametro esposto indica che il grafico <b>non può essere personalizzato</b> in alcun modo. Non è possibile impostare valori quali l’intensità di un effetto, l’opacità di un’immagine da fondere, il colore di un’area specifica e così via.
* Nessun input significa che in alcuni casi non è possibile personalizzare il risultato di un grafico con<b> dati di immagini personali</b>, ad esempio mappe trama eseguite i baking da cui generare effetti, un&#39;immagine di input da cui eseguire una sfocatura o una maschera personalizzata per isolare determinate aree di un&#39;immagine.

## Ingressi e uscite

Un [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)è un nodo che genera un singolo risultato 2D. È un punto finale, un punto finale per il grafico, un risultato finito. Solo i dati connessi a un output possono essere esportati al di fuori di Designer o utilizzati in altri grafici.

Ecco alcuni aspetti da considerare sugli Output:

* Puoi disporre di tutti gli output desiderati, ma devi avere <b>almeno un output</b>.
* Un output può essere <b>qualsiasi risoluzione</b> fino a 8192 px di larghezza o altezza, può essere<b> a colori o in scala di grigi</b> e può essere esportato in qualsiasi tipo di file supportato.
* Gli output possono e devono essere <b>denominati in modo univoco</b> per identificarli; è utile durante l&#39;esportazione.
* Ogni connettore sul lato destro di qualsiasi nodo è in realtà un output (vedere &quot;Sottografi per maggiori informazioni)

Un [input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) è simile a un output, ma è uno slot vuoto e aperto a cui è possibile connettersi con i propri dati. Consente di creare un grafico con dati immagine esterni definiti dall’utente, ad esempio un filtro che modifica un’immagine di input (ad esempio, una Sfocatura o una regolazione Contrasto).

Ecco alcuni aspetti da considerare:

* Gli input sono completamente <b>facoltativi</b>. È consigliabile aggiungerli solo se necessario. Non esiste un importo minimo o massimo.
* Gli input hanno una risoluzione impostata (collegata in genere al grafico) che definite, nonché se sono in scala di grigio o a colori. Tutto ciò a cui è collegato verrà convertito per corrispondere a questo.
* Gli input possono essere file bitmap dal disco rigido, altri grafici, livelli da Painter o Alchemist, ecc.
* Ogni connettore sul lato sinistro di qualsiasi nodo è un ingresso (vedere &quot;Sub-graphs for more info)

## Ereditarietà

Poiché le immagini e i valori vengono passati dai nodi ad altri, alcuni *attributi* di queste immagini, ovvero i <b>parametri di base</b>, vengono *propagati* anche nel grafico, ad esempio risoluzione, precisione (ovvero profondità di bit), Affiancamento e numero casuale.

Questa propagazione è definita dai [metodi di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) applicati da ogni nodo per questi attributi. In effetti, i nodi possono *ereditare attributi* da altri nodi o dal grafico in cui esistono.\
I metodi di ereditarietà possono essere:

* *Rispetto all&#39;elemento padre*
* *Rispetto all&#39;input*
* *Assoluto*, ovvero nessuna ereditarietà

L&#39;ereditarietà può essere astratta e difficile da gestire, pertanto ti consigliamo di dare un&#39;occhiata alla [pagina dedicata](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) per discuterne nel dettaglio.

## Parametri di esposizione

L&#39;esposizione dei parametri è un concetto che può andare molto a fondo, ma può essere sintetizzato come la scelta di determinate proprietà dei nodi nel grafico e la creazione di un elemento di controllo dell&#39;interfaccia utente dedicato per essi, che è facilmente disponibile una volta che il grafico è utilizzato come sottografo o se è pubblicato come archivio. Poiché non è più possibile selezionare rapidamente o facilmente i nodi e modificarne le proprietà, l&#39;obiettivo è creare un altro pannello di controllo principale che raggruppi tutte le proprietà relative a questo grafico specifico.

di seguito sono riportati alcuni aspetti che è necessario conoscere in merito ai parametri esposti:

* I parametri esposti <b>spostano un controllo dal nodo al grafico</b>, essenzialmente verso l&#39;alto nella gerarchia.
* I parametri esposti non possono quindi più essere modificati sul nodo, ma solo sul grafico.
* I parametri esposti possono essere completamente personalizzati con nomi, etichette, valori, tipo di editor dell&#39;interfaccia utente e possono anche essere nascosti e visualizzati per determinate condizioni.

L&#39;esposizione dei parametri è un concetto astratto e difficile per i principianti,[è disponibile una documentazione più specifica su questo argomento](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ma si consiglia di acquisire familiarità con altri aspetti di base del software prima di passare all&#39;esposizione dei parametri.
