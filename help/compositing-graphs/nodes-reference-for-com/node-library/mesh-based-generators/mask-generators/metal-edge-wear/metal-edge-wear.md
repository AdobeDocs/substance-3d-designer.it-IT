---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear metallo per generare maschere di usura sui bordi metallici in base alla curvatura e alla posizione della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear metallico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# Edge Wear metallico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta l&#39;usura dei bordi di un oggetto metallico, con graffi e scheggiature che appaiono sui bordi sollevati Convessi, potenzialmente mascherati da aree scure AO eseguite i baking.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Input Grunge</b> <i>Input scala di grigi</i> |  |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Spazio globale normale</b> <i>Input colore</i> |  |
| <b>Posizione</b> <i>Input colore</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello Di Usura</b> <i>0.0 - 1.0</i> | Imposta la quantità totale di usura, rivelando gradualmente. |
| <b>Indossare Contrasto</b> <i>0.0 - 1.0</i> | Imposta il contrasto del risultato finale. |
| <b>Smoothness bordi</b> <i>0.0 - 16.0</i> | Imposta lo smoothness del decadimento dai bordi della curvatura. |
| <b>Importo Grungi</b> <i>0.0 - 1.0</i> | Imposta la quantità di grunge da fondere tra i bordi. |
| <b>Scala Grungi</b> <i>1 - 16</i> | Imposta la scala della Grunge. |
| <b>Mascheratura Occlusione ambientale</b> <i>0.0 - 1.0</i> | Imposta l’entità dell’effetto dell’effetto sull’effetto finale, escludendo le aree scure. |
| <b>Spessore curvatura</b> <i>0.0 - 1.0</i> | Consente di impostare l’effetto ottenuto dai bordi convessi della curvatura sull’effetto finale. |
| <b>Usa Grunge personalizzata</b> <i>Falso/Vero</i> | Consente di attivare uno slot di input personalizzato per la mappa Grunge. |
| <b>Usa Triplanare</b> <i>Falso/Vero</i> | Abilita la proiezione [Tri Planare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) per nascondere le giunture. |
| <b>Contrasto di fusione triplanare</b> <i>0.0 - 1.0</i> | Imposta il contrasto di fusione per la proiezione triplanare. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-02.gif" />
        </td>
    </tr>
</table>
