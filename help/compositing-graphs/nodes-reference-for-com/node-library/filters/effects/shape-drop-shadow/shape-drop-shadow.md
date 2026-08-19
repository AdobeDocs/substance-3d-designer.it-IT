---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Usate il nodo Ombra esterna forma per aggiungere effetti di ombra esterna alle forme per creare profondità e dimensione nelle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombra esterna forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Ombra esterna forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## Ombra esterna forma (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue il noto effetto &quot;Ombra esterna&quot; di altri software di elaborazione di immagini 2D su una maschera di input in bianco e nero (per la versione in scala di grigio) o un’immagine con trasparenza (per la versione a colori).

Si differenzia dall&#39;effetto [Ombre](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) in quanto restituisce immagini a cui è stata applicata la trasparenza completa, il che garantisce un effetto più completo simile a quello che ci si aspetterebbe da altri software.

## Parametri

* **Angolo**: *0.0 - 1.0* Angolo di incidenza della (falsa) luce.
* **Distanza**: *-0,5 - 0,5* Distanza di discesa/allontanamento dell&#39;ombra dalla forma.
* **Dimensioni**: *0.0 - 1.0* Controlla la sfocatura/i fuzzine dell&#39;ombra.
* **Estensione**: *0.0 - 1.0* Taglia/soglia per l’effetto di sfocatura, allontana ulteriormente l’ombra.
* **Opacità**: *0,0 - 1,0*\
  Opacità di fusione per l’effetto ombra.
* **(Ombra) Colore**: *(Valore colore)*Tinta colore da applicare all&#39;ombra.
* **Colore maschera**: *(Valore colore) *(Solo versione in scala di grigio)**Tinta unita da utilizzare per l&#39;output con mapping trasparenza.
* **Input premoltiplicato**: *False/True *(Solo versione a colori)**Indica se l&#39;input deve essere considerato premoltiplicato.
* **Output pre-moltiplicazione**: *False/True* Indica se l&#39;output deve essere premoltiplicato.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
