---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Usura stoffa per generare maschere di usura sulle superfici dei tessuti in base alla curvatura della trama e alle aree di contatto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usura stoffa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Usura stoffa

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

La maschera rappresenta i bordi sfalsati sui materiali in tessuto. Usa una mappa di altezza dei dettagli del tessuto che determina la maggior parte dell&#39;aspetto; senza una mappa appropriata, l&#39;effetto sembra molto semplice.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Height</b> <i>Input scala di grigi</i> | Height solo per il motivo tessuto. Non si tratta del height dell&#39;oggetto (eseguito i baking), ma piuttosto di un pattern di dettaglio Affiancamento. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Curvatura</b> <i>Input scala di grigi</i> | Curvatura eseguita i baking/generata per determinare gli spigoli in rilievo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Quantità bordi netti</b> <i>0.0 - 1.0</i> |  |
| <b>Morbidezza usura</b> <i>0.0 - 5.0</i> | Determina la sfocatura dei bordi usurati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-02.gif" />
        </td>
    </tr>
</table>
