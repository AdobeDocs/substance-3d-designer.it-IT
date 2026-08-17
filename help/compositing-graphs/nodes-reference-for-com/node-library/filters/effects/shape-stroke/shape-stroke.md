---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Usate il nodo Traccia forma per aggiungere contorni di traccia alle forme per creare bordi ed effetti per i bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tratto forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Tratto forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-stroke.png){width="128px"}

![](../../../../../../assets/shape-stroke-grayscale.png){width="128px"}

## Tratto forma (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Aggiunge un tratto o un contorno attorno a una maschera in bianco e nero (per la versione in scala di grigio) o a una forma con un canale alfa (per la versione a colori), come si potrebbe già fare con altre applicazioni di modifica di immagini 2D. Può essere visualizzata come una versione più completa di [Rilevamento bordo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Molto utile per vari effetti di editing delle immagini.

## Parametri

* **Larghezza**: *-1.0 - 1.0* Larghezza dell&#39;effetto del tratto.
* **Opacità**: *0,0 - 1,0*\
  Opacità globale dell’effetto.
* **(Contorno) Colore**: *(Valore colore)*Colore utilizzato per l&#39;effetto contorno.
* **Colore maschera**: *(Valore colore) *(Solo versione in scala di grigio)**Tinta unita da utilizzare per l&#39;output con mapping trasparenza.
* **Input premoltiplicato**: *False/True *(Solo versione a colori)**Indica se l&#39;input deve essere considerato premoltiplicato.
* **Output pre-moltiplicazione**: *False/True* Indica se l&#39;output deve essere premoltiplicato.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapestroke-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
