---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/creased.html"
breadcrumb-title: ''
description: Usa il nodo Crease per generare pattern di pieghe per la creazione di effetti di tessuto piegato e texture superficiale rugosa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Creased
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crease
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 8%

---


# Crease

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](creased.resources/creased.png){width="128px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo genera un disturbo simile a un panno. Può essere interpretato come Heightmap

L’opzione Creased (Creputo) è utile quando è necessario un disturbo semi-direzionale con variazioni su larga scala.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>1 - 8</i> | Imposta la scala globale per l’effetto. |
| <b>Intensità alterazione</b> <i>0.0 - 128.0</i> | Imposta l’intensità dell’effetto di piegatura/alterazione. |
| <b>Disturbo</b> <i>0.0 - 100.0</i> | Sposta leggermente i livelli utilizzati per generare il disturbo, per introdurre la variazione. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="creased.resources/creased-ex.gif" />
        </td>
    </tr>
</table>
