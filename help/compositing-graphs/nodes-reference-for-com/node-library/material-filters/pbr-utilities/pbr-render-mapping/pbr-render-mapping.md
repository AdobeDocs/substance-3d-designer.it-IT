---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Utilizza il nodo Mappatura PBR render per convertire gli output di materiale in diversi formati di mappatura PBR render.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura PBR render
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Mappatura PBR render

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## Mappatura PBR render (a colori/in scala di grigi)

**Ingresso:** *Filtri materiale/Utility PBR*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo è un nodo di estensione per il [nodo di PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), che consente di mappare una texture separata sulla forma da un [PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) precedente. Il suo obiettivo principale è quello di consentire di ridefinire ogni canale separato dal [PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), sulla forma, per creare interruzioni composite del canale mappa, come negli esempi seguenti. Puoi creare liberamente il tuo metodo composito e le maschere utilizzando i nodi di Mappatura PBR render come componente.

Esistono versioni a colori e in scala di grigi per i due tipi di dati: usa il colore per le mappe diffuse, usa la scala di grigi per le mappe di rugosità, metalliche e altre mappe in scala di grigi.

### Input

* **Texture**: *Input colore/scala di grigi*\
  Texture da mappare su forma.
* **UV**: *Input colore* Input obbligatorio di dati UV da un [nodo di PBR render.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## Parametri

* **Colore di sfondo**: *(Valore colore)*Imposta un valore di colore a tinta unita da utilizzare nello sfondo.

## Immagini di esempio

L&#39;esempio è un composto di quattro diversi nodi di mappatura PBR render, utilizzando una [Selezione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) su una [Sfumatura lineare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) come maschere.

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
