---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear per generare maschere di usura sui bordi della trama per creare danni realistici ai bordi e effetti meteorologici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 7%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questo nodo rappresenta l&#39;usura sui bordi degli oggetti. Ha alcuni parametri, ma non è il più facile da usare: ti consigliamo di giocare e dare un&#39;idea delle cose. Il nodo è abbastanza potente, anche se non è possibile eseguire alcuna maschera di esclusione personalizzata.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta la diffusione totale dell’effetto. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Soglia</b> <i>0.0 - 1.0</i> | In modo simile a Livello, imposta la diffusione totale dell’effetto. |
| <b>Larghezza bordi</b> <i>0.0 - 1.0</i> | Consente di impostare la pienezza dell’effetto di evidenziazione. Riduceteli per renderli più brillanti. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Imposta la quantità di disturbo da fondere per separare lo smoothness. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-wear-ex.gif" />
        </td>
    </tr>
</table>
