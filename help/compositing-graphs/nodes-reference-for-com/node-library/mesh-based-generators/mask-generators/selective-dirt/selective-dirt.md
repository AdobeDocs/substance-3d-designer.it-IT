---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt selettivo per generare maschere di accumulo dirt selettivo in base alla geometria della trama per un'attenuazione atmosferica realistica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt selettivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 8%

---


# Dirt selettivo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](selective-dirt.resources/selective-dirt.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) rappresenta un semplice effetto dirt sui bordi convessi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Maschera variante</b> <i>Input scala di grigi</i> | Mappa di variazione facoltativa, che può essere abilitata tramite parametri. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta il livello totale dell’effetto, rivelandolo gradualmente. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Variazione</b> <i>0.0 - 1.0</i> | Imposta la quantità di variazione/grunge da fondere nell&#39;effetto. |
| <b>Ignora maschera variante</b> <i>Falso/Vero</i> | Consente di sostituire la variante con uno slot di input personalizzato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="selective-dirt.resources/selective-dirt-ex.gif" />
        </td>
    </tr>
</table>
