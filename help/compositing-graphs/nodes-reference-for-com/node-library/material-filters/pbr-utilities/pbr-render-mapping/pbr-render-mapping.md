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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# Mappatura PBR render

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render-mapping.resources/pbr-render-mapping-color.png)![](pbr-render-mapping.resources/pbr-render-mapping-grayscale.png)

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo è un nodo di estensione per il [nodo di PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), che consente di mappare una texture separata sulla forma da una [PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) precedente. Il suo obiettivo principale è quello di consentire di ridefinire ogni canale separato dal [PBR render](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), sulla forma, per creare interruzioni composite del canale mappa, come negli esempi seguenti. Puoi creare liberamente il tuo metodo composito e le maschere utilizzando i nodi di Mappatura PBR render come componente.

Esistono versioni a colori e in scala di grigi per i due tipi di dati: usa il colore per le mappe diffuse, usa la scala di grigi per le mappe di rugosità, metalliche e altre mappe in scala di grigi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Texture</b> <i>Ingresso colore/scala di grigi</i> | Texture da mappare su forma. |
| <b>UV</b> <i>Input colore</i> | Input obbligatorio di dati UV da un [nodo di PBR render.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Impostate un valore di colore a tinta unita da utilizzare nello sfondo. |

## Esempi

L&#39;esempio è un composto di quattro diversi nodi di mappatura PBR render, utilizzando una [Selezione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) su una [Sfumatura lineare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) come maschere.

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-ex.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-ex-2.png" />
        </td>
    </tr>
</table>
