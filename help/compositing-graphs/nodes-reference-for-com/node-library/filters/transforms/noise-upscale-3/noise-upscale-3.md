---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Utilizzate il nodo Noise Upscale 3 per ingrandire le texture utilizzando algoritmi avanzati basati sul disturbo per mantenere i dettagli a risoluzioni più elevate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento disturbo 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# Aumento disturbo 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-3.resources/noise-upscale.png){width="128px"}

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Effettua una procedura basata sul disturbo di input e la ridimensiona fino a doppia risoluzione, mantenendo i dettagli ma senza introdurre troppa suddivisione in porzioni. Usa una maschera definita dall’utente per fondere il disturbo sulla scala originale.

Questo nodo è principalmente destinato a ottimizzare i grafici lenti che utilizzano rumori pesanti e grandi. Consente di utilizzare risoluzioni più elevate senza introdurre troppo tempo di elaborazione aggiuntivo.

Consultate anche [Noise Upscale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) e [Noise Upscale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), che nella maggior parte dei casi tendono a nascondere le porzioni in modo leggermente migliore.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Scala di grigi</b> <i>Input scala di grigi</i> | Immagine Disturbo di destinazione. |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-3.resources/noise3ex.png" />
        </td>
    </tr>
</table>
