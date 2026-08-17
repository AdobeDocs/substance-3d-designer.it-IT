---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Usate il nodo Sobel curvatura per rilevare i bordi di curvatura mediante gli operatori Sobel per creare maschere basate sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# Sobel curvatura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## Sobel curvatura

**Ingresso:** *Filtri/Effetti*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una semplice e intensa conversione di curvatura a passaggio singolo in [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) di input. La mappa risultante ha tinte bianche per le aree convesse e tinte nere per concave. La curvatura produce sempre linee più spesse e transizioni nitide.

Questo nodo è utile per evidenziare o scurire rapidamente alcuni bordi. È leggermente diverso da [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), in quanto produce risultati di migliore qualità, ma è ancora nitido e deciso.

## Parametri

* **Intensità**: *0,0 - 1,0* L’intensità dell’effetto regola il contrasto.
* **Tipo normale**: *DirectX, OpenGL*

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
