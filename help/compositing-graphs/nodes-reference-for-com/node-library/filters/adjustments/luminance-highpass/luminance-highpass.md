---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Utilizzate il nodo Superficie luminanza per estrarre i dettagli di luminanza ad alta frequenza dalle texture per migliorare i dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passa luminanza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# Passa luminanza

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## Passa luminanza

**Ingresso:** *Filtri/Regolazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Consente di annullare le informazioni di illuminazione eseguendo un [highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)sul valore Luminanza dell&#39;input. Utile per correggere texture fotografate con informazioni sull’illuminazione. Può essere combinato in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) con più passaggi per rimuovere diverse frequenze di dettagli di illuminazione.

Mantenere i colori è un&#39;operazione leggermente migliore rispetto a [Illuminazione Annulla basse frequenze.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

## Parametri

* **Raggio**: *0.0 - 64.0* Raggio dell&#39;effetto passa-alto. Un raggio più piccolo annulla un’illuminazione più piccola e si regola in base alle immagini di input.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
