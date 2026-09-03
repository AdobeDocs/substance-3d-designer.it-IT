---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/dissolve.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dissolvenza per fondere le texture utilizzando la modalità di dissolvenza per creare effetti di transizione e dissolvenza tra le texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Dissolve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dissolvi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---


# Dissolvi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dissolve.resources/dissolve-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Unisce due input con Disturbo bianco come maschera per la transizione.

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
