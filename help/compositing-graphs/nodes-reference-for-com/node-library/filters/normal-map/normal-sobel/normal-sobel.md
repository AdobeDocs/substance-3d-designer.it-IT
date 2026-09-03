---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sobel normale (Normal Sobel) per generare mappe normali da mappe di height utilizzando il rilevamento degli spigoli Sobel per i dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# Sobel normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-sobel-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Converte un input Heightmap in un output Normalmap. Una versione leggermente più avanzata del [nodo atomico normale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), questo nodo utilizza il campionamento Sobel anziché il metodo di campionamento standard.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 3.0</i> | Forza delle normali convertite. |
| <b>Formato Normale</b> <i>OpenGL, DirectX</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
