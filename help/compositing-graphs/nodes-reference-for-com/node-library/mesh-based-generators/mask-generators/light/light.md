---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce per generare maschere in base alle condizioni di illuminazione della trama per creare varianti del materiale realistiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# Luce

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-2.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è un po&#39; diversa dagli altri Generatori: semplicemente fa una falsa illuminazione, basata sulla mappa normale dello spazio mondiale, restituendo una maschera &quot;lightmap&quot; in bianco e nero.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Angolo orizzontale</b> <i>0.0 - 1.0</i> | Imposta l’angolo orizzontale della luce falsa. |
| <b>Angolo verticale</b> <i>0.0 - 1.0</i> | Imposta l’angolo verticale della luce falsa. |
| <b>Lucentezza evidenziazione</b> <i>0.0 - 0.999</i> | Imposta la distanza di decadimento dell’area evidenziata. |
| <b>Livello evidenziazione</b> <i>0.0 - 1.0</i> | Consente di impostare il livello di luminosità dell’area evidenziata. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-ex.gif" />
        </td>
    </tr>
</table>
