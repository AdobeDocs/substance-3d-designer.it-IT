---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rotazione vettoriale normale per ruotare i vettori della mappa normale per regolare l'illuminazione della superficie e l'orientamento dei dettagli.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotazione vettoriale normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# Rotazione vettoriale normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di utilità normale che ruota tutti i vettori di una mappa normale di input nello spazio tangente. Non trasforma i pixel, ma modifica i valori che rappresentano. Può utilizzare una mappa opzionale per aggiungere rotazioni casuali alle sfaccettature in scala di grigio.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Normale</b> <i>Input colore</i> | Mappa di base su cui eseguire la rotazione. Obbligatorio. |
| <b>Mappa di rotazione (facoltativo)</b> <i>Input scala di grigi</i> | Mappa in scala di grigi che modula l’intensità della rotazione. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Angolo di rotazione</b> <i>0.0 - 1.0</i> | Imposta l&#39;angolo in base al quale ruotare Normalmap |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passare da un Formato mappa normale a un altro (inverte il canale verde) |
