---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: Utilizzate il nodo da multi-angolo a normale per generare mappa normale da immagini acquisite da più angoli per ottenere dettagli accurati della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da multi-angolo a normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# Da multi-angolo a normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal-01.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo costruisce una Normalmap a partire da una serie di fotografie/scansioni realizzate in diverse condizioni di illuminazione. Consente una conversione Normalmap molto più accurata rispetto all’estrazione di Normali da una singola immagine di albedo.

È più complicato di [Multi-Angolo per l&#39;Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), in quanto richiede l&#39;utilizzo di angoli di illuminazione impostati e precisi per i vostri input. L’angolo di illuminazione di ogni campione deve essere distribuito uniformemente e i campioni devono essere inseriti in sequenza. Quindi, per tre campioni, gli angoli di illuminazione devono essere presi a: 0, 120, 240 - o qualsiasi offset uniforme di quello (come 90, 210, 330).

>[!NOTE]
>
> Per informazioni sulla versione di Albedo di questo nodo, vedere [Multi-Angolo a albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md). Se desideri pre-elaborare i tuoi input, [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) e [Multi Clona /Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) possono essere utili, poiché sono destinati a essere combinati con questi nodi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input 1-8</b> <i>Input colore</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Quantità di campioni</b> <i>2 - 8</i> | Imposta la quantità di campioni (input) da elaborare. |
| <b>Intensità</b> <i>0.0 - 1.0</i> | Imposta l&#39;intensità di Normalmap. |
| <b>Angolo luce primo campione</b> <i>0.0 - 360.0</i> | Imposta la direzione dell’angolo di illuminazione del primo input. |
| <b>Angolo luce campione successivo</b> <i>Senso antiorario, senso orario</i> | Consente di impostare la direzione in cui si sposta l’illuminazione nel campione successivo. |
