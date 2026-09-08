---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: Utilizzare il nodo Merge di Alpha per combinare texture RGB con canali alfa per la creazione di texture RGBA.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Unione Alpha
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Unione Alpha

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rgb-a-merge.png)

<b>Ingresso:</b> Filtri > Canali

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Aggiunge un canale alfa a un input senza canale alfa. Da non confondere con [RGBA Merge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), questo nodo è molto più semplice e aggiunge solo il canale alfa.

Nodo semplice ma pratico per quando si desidera semplicemente mascherare qualcosa o quando il risultato richiede un canale alfa.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>RGB</b> <i>Input colore</i> | Immagine a colori senza canale alfa |
| <b>A</b> <i>Input scala di grigi</i> | Immagine in scala di grigio da utilizzare come risultato alfa. |
