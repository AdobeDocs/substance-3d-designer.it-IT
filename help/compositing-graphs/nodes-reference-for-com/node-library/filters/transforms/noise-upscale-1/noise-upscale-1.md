---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Utilizzate il nodo Scala con disturbo 1 per ingrandire le texture utilizzando algoritmi basati sul disturbo per mantenere i dettagli quando si aumenta la risoluzione della texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ingrandimento disturbo 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Ingrandimento disturbo 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Ingrandimento disturbo 1

**Entrata:** *Filtri/Trasformazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Effettua una procedura basata sul disturbo di input e la ridimensiona fino a doppia risoluzione, mantenendo i dettagli ma senza introdurre troppa suddivisione in porzioni. Usa un tipo &quot;X&quot; di maschera e si fonde con un contrasto simile all&#39;input originale (il metodo di fusione interno è Copia).

Questo nodo è principalmente destinato a ottimizzare i grafici lenti che utilizzano rumori pesanti e grandi. Consente di utilizzare risoluzioni più elevate senza introdurre troppo tempo di elaborazione aggiuntivo.

Consultate anche [Noise Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) e [Noise Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) per le diverse varianti di questo processo.

## Parametri

* **Scostamento1X**: *0.0 - 1.0* Sposta le parti superiore e inferiore sull&#39;asse X.
* **Scostamento1Y**: *0,0 - 1,0*\
  Sposta le parti superiore e inferiore sull&#39;asse Y.
* **Offset2X**: *0.0 - 1.0* Sposta le parti sinistra e destra sull&#39;asse X.
* **Offset2Y**: *0.0 - 1.0* Sposta le parti sinistra e destra sull&#39;asse Y.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise1ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
