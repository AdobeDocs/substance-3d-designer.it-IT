---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-blend-node.html"
breadcrumb-title: ''
description: Utilizza il nodo Fusione colori per fondere le texture in modalità colore, per mantenere la luminanza durante la modifica di tonalità e saturazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore (nodo di fusione)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Colore (nodo di fusione)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-blend-node.resources/difference.png){width="128px"}

<b>Ingresso:</b> Filtri > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue una modalità di fusione Colore, che mantiene la luminanza dello Sfondo e al tempo stesso adotta la tonalità e la crominanza del Primo piano.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Primo piano</b> <i>Input colore</i> |  |
| <b>Sfondo</b> <i>Input colore</i> |  |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo. |
| <b>Fusione alfa</b> <i>Falso/Vero</i> | Attiva/disattiva la fusione dei canali alfa di primo piano e di sfondo. Se è impostato su False, il canale alfa del primo piano viene ignorato. |
