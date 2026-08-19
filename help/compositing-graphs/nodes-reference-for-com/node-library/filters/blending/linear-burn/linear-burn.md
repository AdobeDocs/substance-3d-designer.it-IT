---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: Utilizzate il nodo Brucia lineare per fondere le texture utilizzando la modalità Brucia lineare per creare effetti di scurimento e contrasto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Brucia lineare
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---


# Brucia lineare

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/linear-burn.png){width="128px"}

## Brucia lineare

**Ingresso:** *Filtri/Fusione*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una fusione di Brucia lineare. Formula matematica: primo piano + sfondo - 1.

## Parametri

### Input

* **Primo piano**: *Input colore*
* **Sfondo**: *Input colore*
* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Opacità**: *0,0 - 1,0*\
  Fusione dell’opacità tra primo piano e sfondo.
* **Fusione Alpha**: *False/True*\
  Attiva/disattiva la fusione dei canali alfa di primo piano e di sfondo. Se è impostato su False, il canale alfa del primo piano viene ignorato.

## Immagini di esempio

</td>
</tr>
</table>
