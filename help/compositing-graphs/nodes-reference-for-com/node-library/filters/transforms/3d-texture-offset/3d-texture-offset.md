---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: Usate il nodo Scostamento texture 3D per scostare le texture nello spazio 3D per creare effetti di parallasse e variazioni di superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scostamento texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Scostamento texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtextureoffsetgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtextureoffsetcolor.png){width="200px"}

</td>
</tr>
</table>

<b>Entrata:</b> Filtro > Trasformazione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Scostamento texture 3D** applica una *trasformazione offset* negli assi **X**, **Y** e **Z** su un oggetto descritto dalla *texture 3D* connessa all&#39;**Input**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi/Colore</i> | La <i>texture 3D</i> che descrive un oggetto 3D.<br>L&#39;oggetto è comunemente descritto in un <i>cubo di unità</i>. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scostamento</b> <i>Float3</i> | Quantità di scostamento nello <i>spazio mondiale</i> applicata all&#39;oggetto descritto dalla <i>texture 3D</i> connessa all&#39;<b>input</b>. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtextureoffset-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtextureoffset-node.png" />
        </td>
    </tr>
</table>
