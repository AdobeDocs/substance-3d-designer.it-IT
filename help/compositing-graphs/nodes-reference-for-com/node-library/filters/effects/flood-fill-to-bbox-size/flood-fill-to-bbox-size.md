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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Flood Fill a dimensioni casella

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

## Flood Fill a dimensioni casella

**Ingresso:** *Filtri/Effetti*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una mappa in scala di grigio da una base di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), con valori associati alle dimensioni di ogni singola porzione.

I valori sono relativi alle dimensioni totali dell’area di lavoro (un riquadro bianco completo significa che si estende sull’intera area di lavoro), quindi il contrasto è spesso basso.

## Parametri

* **Output**: *max(X, Y), X, Y* Imposta la metrica su cui è basato il valore: larghezza, lunghezza o entrambi.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodbbox-ex1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
