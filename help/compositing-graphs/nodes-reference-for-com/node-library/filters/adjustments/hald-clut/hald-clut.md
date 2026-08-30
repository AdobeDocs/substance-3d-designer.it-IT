---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Utilizzate il nodo Hald CLUT per applicare le tabelle di consultazione del colore utilizzando il formato Hald CLUT per la correzione e la correzione del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](hald-clut.resources/hald-clut.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica un LUT all&#39;immagine di input. Il LUT deve essere in formato Hald con risoluzione 4096\*4096. Per ulteriori informazioni, vedere <http://www.quelsolaar.com/technology/clut.html>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>input</b> <i>Input colore</i> | Immagine su cui applicare il LUT. |
| <b>lut</b> <i>Input colore</i> | Slot di ingresso Lut. Deve essere 4096x4096. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità LUT per Alpha</b> <i>Falso/Vero</i> | Definisce se l’effetto LUT è ponderato dal canale alfa. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="hald-clut.resources/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
