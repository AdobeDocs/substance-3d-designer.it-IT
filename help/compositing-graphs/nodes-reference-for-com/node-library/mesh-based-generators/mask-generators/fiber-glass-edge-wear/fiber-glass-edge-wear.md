---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear fibra di vetro per generare maschere di usura sui bordi in fibra di vetro in base alla curvatura della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear in fibra di vetro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# Edge Wear in fibra di vetro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Rappresenta una maschera specificamente destinata a un&#39;usura di tipo vetroresina, potrebbe forse essere utilizzata per panno. A causa della natura molto piastrellata e ripetitiva delle fibre, la fusione triplanare può opzionalmente essere abilitata.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per evidenziare i bordi. Obbligatorio! |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per mascherare le aree occluse. Non richiesto, ma sicuramente consigliato. |
| <b>Input Grunge</b> <i>Input scala di grigi</i> | Slot personalizzato opzionale per ignorare il motivo a fibra. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Spazio globale normale</b> <i>Input colore</i> | Utilizzato solo per Triplanare. |
| <b>Posizione</b> <i>Input colore</i> | Utilizzato solo per Triplanare. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello Di Usura</b> <i>0.0 - 1.0</i> | Come una [scansione dell&#39;istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), rivela progressivamente l&#39;usura. |
| <b>Indossare Contrasto</b> <i>0.0 - 1.0</i> | Imposta il contrasto totale dell’effetto. |
| <b>Smoothness bordi</b> <i>0.0 - 16.0</i> | Consente di impostare la fuoriuscita/sfocatura dai bordi evidenziati. |
| <b>Importo Grungi</b> <i>0.0 - 1.0</i> | Imposta l’entità dell’effetto fibra da fondere tra i bordi. Modificate questo valore insieme a Livello di usura per ottenere il massimo controllo. |
| <b>Mascheratura Occlusione ambientale</b> <i>0.0 - 1.0</i> | Consente di impostare il grado di influenza dell’AO nel nascondere l’effetto. |
| <b>Spessore curvatura</b> <i>0.0 - 1.0</i> | Imposta l&#39;entità dell&#39;influenza esercitata dagli spigoli convessi rispetto alla curvatura. |
| <b>Usa Grunge personalizzata</b> <i>Falso/Vero</i> | Sostituisce le fibre incorporate con la mappa personalizzata. |
| <b>Usa Triplanare</b> <i>Falso/Vero</i> | Consente a [Tri Planare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) di nascondere le giunture. |
| <b>Contrasto di fusione triplanare</b> <i>0.0 - 1.0</i> | Controlla il contrasto dell’effetto Triplanare. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-02.gif" />
        </td>
    </tr>
</table>
