---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spigolo (Edge Speckle) per generare pattern di usura con chiazze sui bordi della trama per creare effetti di danno realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-speckle.resources/edge-speckle.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta i bordi con una leggera macchia aggiunta per dividerli. Vedere anche [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per l&#39;evidenziazione dei bordi. Obbligatorio! |
| <b>Maschera variante</b> <i>Input scala di grigi</i> | Slot maschera opzionale utilizzato per mascherare gli effetti del nodo. Attivare con &quot;Ignora maschera di variazione&quot;. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta la quantità totale di evidenziazione dei bordi. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Selezione bordo</b> <i>0.0 - 1.0</i> | Imposta l’influenza degli spigoli convessi. |
| <b>Variazione</b> <i>0.0 - 1.0</i> | Consente di impostare l’entità della divisione dell’effetto tramite la maschera di variazione. |
| <b>Ignora maschera variante</b> <i>Falso/Vero</i> | Sostituisce la maschera incorporata con uno slot di input personalizzato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-speckle.resources/edge-speckle-ex.gif" />
        </td>
    </tr>
</table>
