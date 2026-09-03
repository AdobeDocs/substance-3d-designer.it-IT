---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Usa il nodo Mosaico per creare effetti di porzioni di mosaico dividendo le texture in blocchi e pattern pixelati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# Mosaico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-01.png){width="128px"}

![](mosaic.resources/mosaic-02.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

&quot;Facetizza&quot; una mappa sfumatura esistente, uniforme e inclinata eseguendo un effetto [Altera](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) in più passaggi. Quando la stessa mappa viene utilizzata per entrambi gli input, in pratica cresce e accentua le aree più luminose.

Questa opzione è utile per aggiungere una maggiore definizione alle mappe in scala di grigio, ad esempio Heightmap, in quanto può introdurre una maggiore definizione alle forme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Colore</b> <i>Ingresso colore/scala di grigi</i> |  |
| <b>Mappa mosaico</b> <i>Input scala di grigi</i> | Altera mappa driver. Può essere uguale all&#39;input Primo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Esempi</b> <i>0 - 16</i> | Determina la qualità dei campioni multipli. |
| <b>Intensità</b> <i>0.0 - 1.0</i> | Intensità dell’effetto. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaic-03.png" />
        </td>
    </tr>
</table>
