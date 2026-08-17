---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilizzate il nodo Bagliore forma per aggiungere effetti di bagliore a forme e texture per creare effetti visivi luminosi e atmosferici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bagliore forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Bagliore forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## Bagliore forma (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Crea un bagliore morbido attorno a una maschera di input (per la versione in scala di grigio) o a una forma con un canale alfa (per la versione a colori). Rispetto a [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), questa funzione è più simile a quella di altri software di modifica di immagini 2D, in quanto è più completa e offre più controlli.

## Parametri

* **Modalità**: *Morbida, precisa* Alterna tra due modalità di precisione.
* **Larghezza**: *-1.0 - 1.0* Controlla la distanza del bagliore.
* **Pagine affiancate**: *0.0 - 1.0* Taglia/soglia per l’effetto di sfocatura, fa apparire il bagliore solido vicino alla forma.
* **Opacità**: *0,0 - 1,0*\
  Opacità di fusione per l’effetto bagliore.
* **(Ombra) Colore**: *(Valore colore)*Tinta di colore da applicare al bagliore.
* **Colore maschera**: *(Valore colore) *(Solo versione in scala di grigio)**Tinta unita da utilizzare per l&#39;output con mapping trasparenza.
* **Input premoltiplicato**: *False/True *(Solo versione a colori)**Indica se l&#39;input deve essere considerato premoltiplicato.
* **Output pre-moltiplicazione**: *False/True* Indica se l&#39;output deve essere premoltiplicato.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
