---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ""
description: Utilizzate il nodo Processore valori per elaborare e manipolare i valori della texture utilizzando le operazioni matematiche per le regolazioni personalizzate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elaboratore valori
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%
---

# Elaboratore valori

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nodo atomico: processore valori](value-processor.resources/comp_valueprocessor_1.png "Nodo atomico: processore valori"){width="100%"}

<b>In:</b> Nodi Atomici

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Calcola un [grafico della funzione Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) e ne genera il risultato.

È paragonabile a un [processore pixel](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), con la differenza che non calcola una funzione per ogni pixel, ma piuttosto un singolo valore e lo rende [disponibile in un grafico a Substance](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="value-processor.resources/value-processor-tooltip.gif" alt="descrizione comando di value-processor" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>


>[!TIP]
>
> Questo nodo è un buon punto di partenza per conoscere [Substance grafici di funzione](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Tenete inoltre presente che l&#39;utilizzo di questo tipo di grafico e l&#39;esecuzione di operazioni matematiche sono obbligatori per ottenere qualsiasi risultato da questo nodo.


## Parametri

|  |  |
| --- | --- |
| <b>Funzione processore di valore</b> *Qualsiasi tipo di valore disponibile* | [Il grafico della funzione Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) è stato valutato per calcolare il valore di output. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Immagine di input n. </b> *Scala di grigi/Colore* | Utilizzare un nodo [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) o [Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) per accedere ai valori nell&#39;input dell&#39;indice specificato. |


## Esempi

*Disponibile a breve.*
