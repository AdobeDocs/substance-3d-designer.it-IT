---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: Utilizzate il nodo Intervallo istogramma per ridefinire i valori delle texture in base agli intervalli di istogramma per la correzione e le regolazioni del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Intervallo istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Intervallo istogramma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-1.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Ridurre e/o spostare l’intervallo di un input in scala di grigio. Può essere utilizzato per ridefinire le transizioni, in modo simile a [Luminosità contrasto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md), ma con controlli diversi che potrebbero avere più senso in alcune situazioni.\
Consultate anche [Istogramma Scan](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) per un altro modo più utile per ridefinire l&#39;intervallo.

[Fate clic qui per guardare un video dell’Accademia di Substance sull’intervallo di istogrammi.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intervallo</b> <i>0.0 - 1.0</i> | Quanto ridurre l’intervallo da. Questo effetto è simile a quello che si ottiene spostando verso l’interno i cursori dei livelli minimo e massimo. |
| <b>Posizione</b> <i>0.0 - 1.0</i> | Scostamento per la riduzione dell&#39;intervallo, impostando un punto medio diverso per la riduzione dell&#39;intervallo. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range.gif" />
        </td>
    </tr>
</table>
