---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Usate il nodo Sobel curvatura per rilevare i bordi di curvatura mediante gli operatori Sobel per creare maschere basate sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Sobel curvatura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-sobel.resources/curvature-sobel-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue una semplice e intensa conversione di curvatura a passaggio singolo in [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) di input. La mappa risultante ha tinte bianche per le aree convesse e tinte nere per concave. La curvatura produce sempre linee più spesse e transizioni nitide.

Questo nodo è utile per evidenziare o scurire rapidamente alcuni bordi. È leggermente diverso da [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), in quanto produce risultati di migliore qualità, ma è ancora nitido e deciso.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 1.0</i> | L’intensità dell’effetto regola il contrasto. |
| <b>Tipo normale</b> <i>DirectX, OpenGL</i> |  |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-sobel.resources/curvature-sobel-02.png" />
        </td>
    </tr>
</table>
