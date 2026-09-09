---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Utilizzate il nodo Anteprima esposizione per visualizzare in anteprima le regolazioni di esposizione negli ambienti HDRI prima del rendering finale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anteprima esposizione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Anteprima esposizione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/hdr-exposure-preview.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo helper per visualizzare l&#39;anteprima dei passaggi di esposizione. Gli utenti impostano un valore minimo e un valore massimo, il nodo genera un&#39;immagine molto più grande con un numero diverso di versioni esposte dell&#39;input originale. Le diverse versioni sono sempre impilate orizzontalmente, la quantità dipende dalla risoluzione del nodo o del grafico.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Esposizione massima (EV)</b> <i>-8.0 - 8.0</i> | Esposizione massima dell’immagine più luminosa in alto. |
| <b>Esposizione minima (EV)</b> <i>-8.0 - 8.0</i> | Esposizione minima dell’immagine più scura in basso. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exp-preview-ex.png" />
        </td>
    </tr>
</table>
