---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Utilizzare il nodo Flood Fill a dimensioni casella di riepilogo per riempire le aree con valori di dimensioni del rettangolo di selezione per gli effetti di ridimensionamento procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill a dimensioni casella
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Flood Fill a dimensioni casella

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-bbox-size.resources/floodfill-to-bbox-size.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una mappa in scala di grigio da una base di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), con valori associati alle dimensioni di ogni singola porzione.

I valori sono relativi alle dimensioni totali dell’area di lavoro (un riquadro bianco completo significa che si estende sull’intera area di lavoro), quindi il contrasto è spesso basso.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Output</b> <i>max(X, Y), X, Y</i> | Imposta la metrica su cui si basa il valore: larghezza, lunghezza o entrambe. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-bbox-size.resources/floodbbox-ex1.png" />
        </td>
    </tr>
</table>
