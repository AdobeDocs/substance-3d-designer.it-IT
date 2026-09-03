---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: Utilizzate il nodo Scala con disturbo 2 per ingrandire le texture utilizzando l’interpolazione basata sul disturbo per mantenere la qualità della texture a dimensioni maggiori.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Noise Upscale 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---


# Noise Upscale 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-2.resources/noise-upscale-2-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Effettua una procedura basata sul disturbo di input e la ridimensiona fino a doppia risoluzione, mantenendo i dettagli ma senza introdurre troppa suddivisione in porzioni. Usa un tipo &quot;X&quot; di maschera e si fonde con meno contrasto rispetto all&#39;input originale (i metodi di fusione interni sono Max e Min).

Questo nodo è principalmente destinato a ottimizzare i grafici lenti che utilizzano rumori pesanti e grandi. Consente di utilizzare risoluzioni più elevate senza introdurre troppo tempo di elaborazione aggiuntivo.

Consultate anche [Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) e [Noise Upscale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) per le diverse varianti di questo processo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scostamento1X</b> <i>0.0 - 1.0</i> | Sposta le parti superiore e inferiore sull&#39;asse X. |
| <b>Scostamento1Y</b> <i>0.0 - 1.0</i> | Sposta le parti superiore e inferiore sull&#39;asse Y. |
| <b>Offset2X</b> <i>0.0 - 1.0</i> | Sposta le parti sinistra e destra sull&#39;asse X. |
| <b>Offset2Y</b> <i>0.0 - 1.0</i> | Sposta le parti destra e sinistra sull&#39;asse Y. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-2.resources/noise-upscale-2-02.png" />
        </td>
    </tr>
</table>
