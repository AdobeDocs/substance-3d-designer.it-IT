---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Usa il nodo Mosaico per creare effetti di porzioni di mosaico dividendo le texture in blocchi e pattern pixelati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# Mosaico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mosaic-1.png){width="128px"}

![](../../../../../../assets/mosaic-grayscale.png){width="128px"}

## Mosaico (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

&quot;Facetizza&quot; una mappa sfumatura esistente, uniforme e inclinata eseguendo un effetto [Altera](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) in più passaggi. Quando la stessa mappa viene utilizzata per entrambi gli input, in pratica cresce e accentua le aree più luminose.

Questa opzione è utile per aggiungere una maggiore definizione alle mappe in scala di grigio, ad esempio Heightmap, in quanto può introdurre una maggiore definizione alle forme.

## Parametri

### Input

* **Colore**: *Input scala di colore/grigio*
* **Mappa mosaico**: *Input scala di grigi*\
  Altera mappa driver. Può essere uguale all&#39;input Primo.

### Parametri

* **Esempi**: *0 - 16* Determina la qualità del campione multiplo.
* **Intensità**: *0,0 - 1,0* Intensità dell&#39;effetto.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mosaci-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
