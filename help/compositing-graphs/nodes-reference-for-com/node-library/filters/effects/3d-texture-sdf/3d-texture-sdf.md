---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Utilizza il nodo SDF Texture 3D per generare texture dei campi distanza con segno dai dati 3D per creare forme ed effetti uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SDF texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# SDF texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

<b>Ingresso:</b> Filtro > Effetto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **SDF** della texture 3D genera il *campo distanza con segno* di una forma dalla maschera *texture 3D* dell&#39;input **&#x200B;**&#x200B;che rappresenta le sezioni del *volume* della forma.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input maschera</b> <i>Scala di grigi</i> | La maschera <i>texture 3D</i> che rappresenta le sezioni del <i>volume</i> di una forma. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Soglia</b> <i>Mobile</i> | Quando il volume della forma è descritto da una <i>sfumatura di dissolvenza</i>, imposta il valore della sfumatura in base al quale la <i>superficie</i> della forma viene <i>rilevata</i>. |
| <b>Output</b> <i>Numero intero</i> | Il tipo di campo distanza che deve essere generato:<br>- <i>Campo distanza</i>: genera un campo distanza che descrive le distanze <i>esterne</i> della forma.<br>- <i>Signed distance field</i>: genera un campo distanza che descrive le distanze <i>esterne</i> (positive) e <i>interne</i> (negative) della forma. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
