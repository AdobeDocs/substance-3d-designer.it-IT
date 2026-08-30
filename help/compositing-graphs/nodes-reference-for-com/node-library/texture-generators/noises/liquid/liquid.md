---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Utilizza il nodo Liquid per generare pattern di liquidi e fluidi per creare effetti di superficie di acqua, olio e altri fluidi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Liquido
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Liquido

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](liquid.resources/liquid.png){width="128px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Si tratta di una semplice variante di [Disturbo gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), che [altera](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) con se stessa per creare un effetto simile a un liquido.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>1 - 128</i> | Imposta la scala globale per l’effetto. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Fase che sposta il disturbo per introdurre piccole variazioni |
| <b>Intensità alterazione</b> <i>0.0 - 1.0</i> | Imposta l’intensità dell’effetto di alterazione. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="liquid.resources/liquid-ex.gif" />
        </td>
    </tr>
</table>
