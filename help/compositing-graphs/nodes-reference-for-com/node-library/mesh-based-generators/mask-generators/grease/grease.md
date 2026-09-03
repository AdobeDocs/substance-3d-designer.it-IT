---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilizzate il nodo Grasso per generare maschere di accumulo del grasso in base alla geometria della trama e alle aree di contatto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grasso
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Grasso

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grease.resources/grease-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è stata creata appositamente per i volti dei personaggi e altre aree specifiche. Genera un tipo di maschera per ingrassaggio della pelle su aree con thickness basso.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Input scala di grigi</i> | Mappa Spessore eseguita i baking su cui è basato l’intero effetto. Obbligatorio! |
| <b>Disturbo</b> <i>Input scala di grigi</i> | Facoltativo Mappa disturbo per sostituire Grassa grunge con. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Consente di impostare la quantità totale dell’effetto da visualizzare. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Soglia Thickness</b> <i>0.0 - 1.0</i> | Imposta il thickness minimo in cui deve comparire l’effetto. Altrettanto importante è il livello. Modificatelo per adattarlo alla vostra mappa di spessore. |
| <b>Ignora disturbo</b> <i>Falso/Vero</i> | Imposta per ignorare la mappa della grunge di grasso interna con uno slot di input personalizzato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grease.resources/grease-02.gif" />
        </td>
    </tr>
</table>
