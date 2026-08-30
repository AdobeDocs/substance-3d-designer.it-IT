---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: Utilizzate il nodo Danni bordo per generare maschere di danno sui bordi della trama per creare effetti realistici di usura e rottura dei bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Danni ai bordi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 6%

---


# Danni ai bordi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-damages.resources/edge-damages.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta i danni arrecati ai bordi convessi in rilievo in base alla curvatura e all&#39;AO eseguito i baking.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per il posizionamento degli effetti. Obbligatorio! |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per il posizionamento degli effetti. Obbligatorio! |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Quantità di danno al bordo da applicare. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Intensità danni</b> <i>0.0 - 1.0</i> | Si sposta tra un aspetto scheggiato e uniforme e un aspetto caotico, graffiato e fortemente danneggiato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-damages.resources/edge-damages-ex.gif" />
        </td>
    </tr>
</table>
