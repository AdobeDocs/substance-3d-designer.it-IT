---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: Utilizzate il nodo di fusione Differenza per fondere le texture in modo da creare effetti di inversione e contrasto in modalità di differenza.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Differenza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Differenza

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

## Differenza

**Ingresso:** *Filtri/Fusione*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue un metodo di fusione per differenza tra gli input in primo piano e in sfondo. Sottrae lo sfondo dal primo piano, restituendo un risultato assoluto (mai un valore negativo).

## Parametri

### Input

* **Sfondo**: *Input colore*
* **Primo piano**: *Input colore*
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
