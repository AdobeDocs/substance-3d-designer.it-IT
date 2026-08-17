---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sezione simmetria (Symmetry Slice) per suddividere le texture lungo gli assi di simmetria per creare pattern ed effetti specchiati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sezione simmetria
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Sezione simmetria

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## Sezione simmetria

**Entrata:** *Filtri/Trasformazioni*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Complesso nodo operativo di simmetria/mirroring. Consente un&#39;ampia varietà di operazioni geometriche con pieno controllo, ma richiede alcuni esperimenti.

Rispetto a [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) e [Symmetry](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), questo nodo ha molte più opzioni.

## Parametri

* **Modalità simmetria**: *0 - 6* Scegliere geometria simmetrica/linea speculare. Le opzioni disponibili sono Orizzontale, Verticale, Diagonale sinistra-destra, Diagonale destra-sinistra, Inverti verticale, Angolo e Angolo diagonale.
* **Modalità di trasferimento**: *0 - 6\
  Metodo fusione. Opzioni: *
* **Fusione**: *0.0 - 1.0* Fonde nuovamente l&#39;immagine originale nel risultato.
* **Capovolgi lato**: *False/True* Capovolge l&#39;origine, a indicare che il lato di origine dell&#39;operazione è invertito. La simmetria da sinistra a destra, ad esempio, diventa da destra a sinistra.
* **Capovolgi lato2**: *False/True* Utilizzato solo quando la modalità Simmetria è 5 o 6. Inverti origine angolo.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
