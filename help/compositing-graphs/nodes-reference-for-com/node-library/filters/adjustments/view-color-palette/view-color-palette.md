---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: Utilizzate il nodo Visualizza tavolozza colori per visualizzare i dati della tavolozza dei colori estratti dalle texture per l'analisi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visualizza tavolozza colori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# Visualizza tavolozza colori

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Quantizza colore](view-color-palette.resources/view-color-palette-01.png "Icona Quantizza colore"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Inserisce una tavolozza di colori in un quadrato o in un rettangolo per visualizzarla più facilmente nella vista Grafico o 2D.\
L&#39;impacchettamento mira a lasciare il minor numero possibile di slot vuoti.

</td>
</tr>
</table>

L&#39;ordine dei colori nella tavolozza viene mantenuto, con i colori che scorrono da sinistra a destra e dall&#39;alto verso il basso in modo simile alla disposizione del testo.

Questo nodo può essere utilizzato per visualizzare le tavolozze prodotte dai seguenti nodi: [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crea tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modifica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tavolozza</b> <i>Colore</i> PRIMARIO | Un elenco ordinato di colori RGB codificati come una riga di pixel. La tavolozza può contenere un massimo di 256 colori.   Questa è la tavolozza che il nodo prepara ed esegue il rendering. |
| <b>Quantità colore tavolozza</b> <i>Numero intero</i> | Quantità di colori memorizzati nella tavolozza.   Se tale numero non corrisponde alla quantità effettiva di colori nell&#39;input dell&#39;immagine &quot;Palette&quot;, la visualizzazione potrebbe essere incompleta o disporre di più spazi vuoti del necessario. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Visualizzazione della tavolozza compressa. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Visualizza tavolozza colori: esempio 1](view-color-palette.resources/view-color-palette-02.png "Visualizza tavolozza colori: esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Visualizza tavolozza colori: esempio 2](view-color-palette.resources/view-color-palette-03.png "Visualizza tavolozza colori: esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Visualizza tavolozza colori: esempio 3](view-color-palette.resources/view-color-palette-04.png "Visualizza tavolozza colori: esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Visualizza tavolozza colori: esempio 4](view-color-palette.resources/view-color-palette-05.png "Visualizza tavolozza colori: esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
