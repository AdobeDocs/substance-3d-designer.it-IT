---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Utilizzate il nodo del filtro Curvatura per generare mappe di curvatura da mappe di height per rilevare superfici convesse e concave.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura (Nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# Curvatura (Nodo filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## Curvatura

**Ingresso:** *Filtri/Effetti*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una semplice e intensa conversione di curvatura a passaggio singolo in [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) di input. La mappa risultante ha tinte bianche per le aree convesse e tinte nere per concave. La curvatura produrrà sempre linee sottili come pixel e transizioni nitide.

Questo nodo è utile per evidenziare o scurire rapidamente alcuni bordi. È limitato rispetto a [Curvatura arrotondata](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (che produce risultati di qualità superiore) e [Curvatura obliqua](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (che ha più opzioni).

## Parametri

* **Intensità**: *0,0 - 10,0* Intensità dell&#39;effetto. Aumenta il contrasto del risultato.
* **Formato normale**: *DirectX, OpenGL*\
  Passa da un formato Normalmap a un altro (inverte il canale Verde).

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
