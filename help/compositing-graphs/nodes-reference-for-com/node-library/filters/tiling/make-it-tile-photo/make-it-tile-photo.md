---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilizzate il nodo Crea foto in porzioni per convertire le fotografie in texture di porzioni uniformi per la creazione di materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crea foto in piastrelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Crea foto in piastrelle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## Crea foto in porzioni (scala di grigi)

**Entrata:** *Filtri/Divisione in porzioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo fornisce la funzionalità di correzione dei bordi per qualsiasi immagine che potrebbe non essere affiancata a causa di bordi non continui. ma solo sui bordi dell&#39;immagine di input. Se desiderate regolare la scala o il riquadro in diversi modi, osservate [Crea un riquadro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

## Parametri

* **Alterazione maschera H**: *-100.0 - 100.0* Introduce alterazioni sull&#39;asse orizzontale per evitare transizioni indefinite.
* **Alterazione maschera V**: *-100.0 - 100.0* Introduce alterazioni sull&#39;asse verticale per evitare transizioni indefinite.
* **Dimensione maschera H**: *0,0 - 1,0* Imposta la distanza orizzontale del bordo di transizione.
* **Dimensione maschera V**: *0,0 - 1,0* Imposta la distanza verticale del bordo di transizione.
* **Precisione maschera H**: *0.0 - 1.0* Imposta la transizione in senso orizzontale.
* **Precisione maschera V**: *0.0 - 1.0* Imposta la transizione in senso verticale.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
