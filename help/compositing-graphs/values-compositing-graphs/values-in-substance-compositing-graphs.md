---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Scoprite i tipi di valore e la gestione dei dati nei grafici di composizione delle Substance per una creazione efficace dei materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Valori nei grafici Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---


# Valori nei grafici Substance

Dopo l&#39;introduzione del motore [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) v7 nella versione 2019.1.0, è ora possibile elaborare i valori nel grafico della Substance e[non solo nelle funzioni](../../function-graphs/function-graphs.md). I dati dei valori sono gli stessi dati utilizzati nelle funzioni (tra cui valori interi, mobili e booleani) e sono quindi nettamente diversi dai dati dell’immagine a colori o in scala di grigi, che rappresentano i valori dei pixel di un’intera immagine. In particolare, quando si menzionano i dati Valori, ciò significa *Intero 1, Intero 2, Intero 3 e Intero 4, Float 1, Float 2, Float 3 e Float 4 e Booleano*. Ognuno di essi ha una codifica a colori distinta e nella maggior parte dei casi non è interscambiato tra loro.

Sono disponibili alcuni casi di utilizzo, ad esempio:

* Restituzione ed elaborazione di dati non di immagine, ad esempio proprietà di materiale a valore singolo o metadati aggiuntivi. Ad esempio, il valore IOR di un materiale.
* Ottimizzazione dei calcoli del grafico che non devono essere calcolati per pixel (un&#39;alternativa al [processore pixel](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)). Ad esempio, una tinta unita casuale.
* Collegamento delle proprietà di un nodo a un altro elaborando i dati dell&#39;immagine in valori. Ad esempio, i valori Minimo e Massimo per un’immagine con cui regolare i Livelli.

## Nuovi nodi Value e input

Due nuovi nodi atomici funzionano con valori:

|  |  |
| --- | --- |
| <div><img alt="Icona nodo processore valori" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="values-in-substance-compositing-graphs.resources/valueprocessor.png" title="Icona nodo processore valori" width="100px"/></div>  <b>[Processore valori](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | [Elaboratore valori](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) accetta un numero qualsiasi di input in scala di grigio o a colori e consente di restituire un singolo valore dai calcoli basati su tali input. |
| <div><img alt="Icona nodo di input valore" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="values-in-substance-compositing-graphs.resources/inputnumeric.png" title="Icona nodo di input valore" width="100px"/></div>  **[Input valore](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)** | L&#39;[Input valore](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)consente di creare uno slot di input nei sottografi definito in modo esplicito come valore. |

Inoltre, altri nodi li gestiscono in un modo specifico:

Il [nodo di output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) viene automaticamente regolato in modo da diventare un output di valore se si collega una connessione di valore a tale nodo, come in precedenza per Scala di grigi e Colore.

![Nodo del valore di output](values-in-substance-compositing-graphs.resources/values-output.gif "Nodo del valore di output"){width="512px"}

Su ogni singolo nodo ([Atomic](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)e [Library](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/Instance) è presente una nuova scheda che consente di definire gli input di valore.

![Aggiunta di valori di input nel nodo](values-in-substance-compositing-graphs.resources/values-inputs.gif "Aggiunta di valori di input nel nodo")

## Utilizzo dei valori

L’utilizzo di Valori è leggermente diverso dal normale lavoro del grafico a Substance:

Le connessioni di valore possono essere effettuate solo da un [processore di valore](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), da un [input di valore](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) o da un [sotto-grafico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md). Ciò significa che un processore di valori è l&#39;unico modo per creare una connessione di valore da zero, non c&#39;è un nodo di &quot;valore statico&quot; o qualcosa di simile. Create invece un processore valori, inserite un valore statico e impostatelo come output per ottenere lo stesso risultato.

Elaboratore valori può restituire un solo valore. Se si desidera restituire più valori o set o gruppi di valori, sarà necessario creare un [grafico secondario](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

Per evidenziare la posizione in cui i valori sono esposti o in uso, qualsiasi nodo con input di valori o output di valori viene evidenziato con un bordo giallo spesso:

![Utilizzo dei valori](values-in-substance-compositing-graphs.resources/yellowhighlight.png "Utilizzo dei valori")
