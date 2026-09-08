---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/plasma.html"
breadcrumb-title: ''
description: Usa il nodo del plasma per generare pattern di disturbo simili a quelli del plasma per creare effetti di texture organici e fluidi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Plasma
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Plasma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 7%

---


# Plasma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/plasma.png){width="128px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo genera una variante leggermente diversa di [disturbo gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), con striature scure più lunghe come valli. Dispone di un controllo di distanza simile per la scala, che mantiene la suddivisione in porzioni.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>1 - 128</i> | Imposta la scala globale per l’effetto. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Fase-sposta il disturbo per introdurre piccole variazioni. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/plasma-ex.gif" />
        </td>
    </tr>
</table>
