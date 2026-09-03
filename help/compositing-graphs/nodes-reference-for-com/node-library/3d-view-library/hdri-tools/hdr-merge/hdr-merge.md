---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: Utilizzare il nodo Unione HDR per unire più immagini HDR in un unico panorama per creare mappe di ambiente composite.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unione HDR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# Unione HDR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hdr-merge.resources/hdr-merge-01.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Unisci più esposizioni fotografiche per creare un&#39;immagine High dynamic range. Il primo input è l’immagine più sottoesposta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input 1-16</b> <i>Input colore</i> | Immagini di input. La quantità disponibile dipende dal parametro. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Input</b> <i>2 - 16</i> | Imposta la quantità di input disponibili. |
| <b>Delta esposizione (EV)</b> <i>0.0 - 4.0</i> | Imposta la differenza di esposizione per interpretare le immagini. |
| <b>Punto bianco</b> <i>0.0 - 13.0</i> | Imposta punto bianco per eseguire alcune regolazioni sul risultato finale. |
