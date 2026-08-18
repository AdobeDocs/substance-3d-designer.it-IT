---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Utilizzate il nodo Noise Upscale 3 per ingrandire le texture utilizzando algoritmi avanzati basati sul disturbo per mantenere i dettagli a risoluzioni più elevate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento disturbo 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Aumento disturbo 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Aumento disturbo 3

**Entrata:** *Filtri/Trasformazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Effettua una procedura basata sul disturbo di input e la ridimensiona fino a doppia risoluzione, mantenendo i dettagli ma senza introdurre troppa suddivisione in porzioni. Usa una maschera definita dall’utente per fondere il disturbo sulla scala originale.

Questo nodo è principalmente destinato a ottimizzare i grafici lenti che utilizzano rumori pesanti e grandi. Consente di utilizzare risoluzioni più elevate senza introdurre troppo tempo di elaborazione aggiuntivo.

Consultate anche [Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) e [Noise Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), che nella maggior parte dei casi tendono a nascondere le porzioni in modo leggermente migliore.

## Parametri

### Input

* **Scala di grigi**: *Input scala di grigi*\
  Immagine Disturbo di destinazione.
* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

*Nessun parametro.*

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise3ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
