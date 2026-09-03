---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione normale Height (Normal Blender) per fondere height e mappa normale per combinare informazioni dettagliate sulle superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione normale height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Fusione normale height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di scelta rapida da tastiera che fonde una Heightmap in scala di grigi su una Normalmap. L&#39;input di Height viene convertito internamente in una mappa normale e quindi mescolato correttamente con l&#39;input normale.

Si tratta di un metodo più rapido per fondere i dettagli rispetto a quello manuale con nodi separati, ma potrebbe non essere sufficientemente controllato e perfezionato per determinate esigenze.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Height</b> <i>Input scala di grigi</i> | Heightmap scala di grigi con cui fondersi. |
| <b>Normale</b> <i>Input colore</i> | Base Normalmap su cui fondere. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità normale</b> <i>0.0 - 16.0</i> | Intensità della conversione normale dell&#39;input di Height. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
