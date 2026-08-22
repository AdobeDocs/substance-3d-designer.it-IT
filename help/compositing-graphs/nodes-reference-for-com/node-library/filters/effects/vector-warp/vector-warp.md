---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-warp.html"
breadcrumb-title: ''
description: Utilizzate il nodo Alterazione vettoriale per alterare le texture utilizzando campi vettoriali per la creazione di effetti di distorsione fluidi e organici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterazione vettoriale
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Alterazione vettoriale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-warp.png){width="128px"}

![](../../../../../../assets/vector-warp-grayscale.png){width="128px"}

## Alterazione vettoriale (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Alterazione vettoriale è un effetto distorsione avanzato, simile a [Alterazione](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) e [Alterazione direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md), con la differenza principale che è guidato da una bitmap vettoriale (a colori) anziché da una mappa in scala di grigio. Questo significa che è più potente e versatile dei suoi cugini del nodo atomico.

La mappa vettoriale è simile a una mappa normale, ma non deve essere normalizzata e vengono utilizzati solo i canali R e Verde (X e Y). Se lo desideri, i canali blu e Alpha possono essere lasciati in nero. La creazione di una buona mappa vettoriale può rappresentare la sfida più grande nell&#39;utilizzo di questo nodo; puoi [convertire le mappe in scala di grigi in Normale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) oppure creare la mappa combinando i canali con[Unione RGBA.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) In alternativa, è possibile utilizzare anche un [&quot;Flow Map&quot;](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/painting/advanced-channel-painting/flow-map-painting).

Questo nodo può essere utile per eseguire distorsioni molto specifiche in direzioni diverse, in cui i nodi standard di Altera non lo tagliano.

## Parametri

### Input

* **Input**: *Input colore*\
  Mapping da distorcere.
* **Mappa Vettoriale**: *Input Colore*\
  Distorsione mappa driver. Vengono utilizzati i canali di colore Rosso e Blu.

### Parametri

* **Moltiplicatore di intensità**: *0,0 - 1,0* Per la mappa vettoriale.
* **Formato vettoriale**: *DirectX, OpenGL* Scambia il canale verde tra l’interpretazione verso l’alto e quella verso il basso.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/vector-warp-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
