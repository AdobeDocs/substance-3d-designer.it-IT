---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Rotazione vettoriale normale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## Rotazione vettoriale normale

**Ingresso:** *Filtri/Mappa Normale*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo di utilità normale che ruota tutti i vettori di una mappa normale di input nello spazio tangente. Non trasforma i pixel, ma modifica i valori che rappresentano. Può utilizzare una mappa opzionale per aggiungere rotazioni casuali alle sfaccettature in scala di grigio.

## Input

* **Normale**: *Input colore*\
  Mappa di base su cui eseguire la rotazione. Obbligatorio.
* **Mappa di rotazione (facoltativo)**: *Input scala di grigi*\
  Mappa in scala di grigi che modula l’intensità della rotazione.

## Parametri

* **Angolo di rotazione**: *0,0 - 1,0*\
  Imposta l&#39;angolo in base al quale ruotare Normalmap
* **Formato normale**: *DirectX, OpenGL*\
  Passare da un Formato mappa normale a un altro (inverte il canale verde)

## Esempi

</td>
</tr>
</table>
