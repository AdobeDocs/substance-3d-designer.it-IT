---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Usura in pelle per generare maschere di usura sulle superfici in pelle in base alla curvatura della trama e ai punti di contatto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usura in pelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# Usura in pelle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta l&#39;usura con un motivo in pelle, con più usura sui bordi in base alla curvatura. È simile all&#39;[Edge Wear in fibra di vetro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) in termini di funzionalità e ha principalmente gli stessi parametri.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per il posizionamento degli spigoli. Obbligatorio! |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per occludere determinate aree. Consigliato, ma non obbligatorio. |
| <b>Input Grunge</b> <i>Input scala di grigi</i> | Slot di input mappa Grunge opzionale che può essere attivato tramite il parametro &quot;Usa Grunge personalizzata&quot;. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello Di Usura</b> <i>0.0 - 1.0</i> | Imposta il livello di usura globale, rivelando gradualmente. |
| <b>Indossare Contrasto</b> <i>0.0 - 1.0</i> | Imposta il contrasto dell’effetto. |
| <b>Importo Grungi</b> <i>0.0 - 1.0</i> | Imposta la quantità di grunge (motivo di pelle di default) da fondere tra i bordi. |
| <b>Mascheratura Occlusione ambientale</b> <i>0.0 - 1.0</i> | Imposta l’entità con cui l’AO maschera gli effetti di usura. |
| <b>Spessore curvatura</b> <i>0.0 - 1.0</i> | Consente di impostare l’entità dell’influenza degli spigoli della curvatura sul risultato finale. Anche se è impostato su 0, è comunque necessaria una mappa di curvatura. |
| <b>Usa Grunge personalizzata</b> <i>Falso/Vero</i> | Consente l&#39;override del motivo di pelle predefinito incorporato. Utilizzare invece uno slot di input personalizzato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-02.gif" />
        </td>
    </tr>
</table>
