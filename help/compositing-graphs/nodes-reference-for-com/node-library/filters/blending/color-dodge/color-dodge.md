---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: Utilizzate il nodo di fusione Scherma colore per schiarire le texture riducendo il contrasto per creare effetti di luce e bagliore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore scherma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 10%

---


# Colore scherma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-dodge.png){width="128px"}

## Colore scherma

**Ingresso:** *Filtri/Fusione*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una fusione Scherma colore. Matematicamente la formula è Sfondo / (1-Primo piano).

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
