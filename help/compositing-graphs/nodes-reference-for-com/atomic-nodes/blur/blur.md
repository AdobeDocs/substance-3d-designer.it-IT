---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sfocatura per applicare effetti di sfocatura alle texture, per attenuare i dettagli e creare effetti di sfocatura leggera.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---


# Sfocatura

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icona nodo sfocatura](../../../../assets/blur-9.png){width="200px"}

**In:** Nodi Atomici

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo Sfocatura esegue un’operazione di &quot;sfocatura in rettangolo&quot;: calcolando la media dei valori dei pixel su una distanza impostata, il risultato è un aspetto sfocato e poco nitido. Offre l&#39;operazione di sfocatura più semplice, veloce e semplice disponibile in [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html).

Anche se la sfocatura funziona bene per operazioni semplici e veloci, come ad esempio ammorbidire leggermente alcuni bordi, in uno scenario più impegnativo [Sfoca HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) è una scelta migliore, compromettendo le prestazioni per la qualità.

</td>
</tr>
</table>

## Parametri

* **Intensità**: 0-illimitato\
  Consente di impostare l’intensità o la distanza della sfocatura. Il numero non è limitato, ma con valori alti l’intera immagine diventa un colore medio.

L’esempio seguente mostra la Sfocatura del nodo a sinistra rispetto a [Sfocatura HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) a destra quando si utilizzano valori alti (in questo caso 50). A valori di circa 1-2 la differenza non è evidente.

| Sfocatura (atomica) | Sfocatura HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="../../../../assets/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="../../../../assets/blur-hq.png"/></div> |
