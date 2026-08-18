---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Utilizzate il nodo Nadir patch per applicare una patch all'area inferiore dei panorami HDRI per correggere gli artefatti inferiori nelle mappe dell'ambiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir patch

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo fornisce la funzionalità di applicare patch al punto di terra centrale (nadir) di un&#39;immagine mappata a livello sferico. Può essere usato per nascondere o &quot;clonare&quot; un brutto nadir, o una fotocamera visibile o un treppiede. Funziona come una [patch clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), ma con regolazioni per immagini con mappatura sferica. L’utente seleziona un punto altrove nell’immagine, ovvero il punto clonato e fuso in basso. Non sono necessari altri input esterni oltre a un singolo HDRI per l’elaborazione, ma è possibile utilizzare una maschera esterna come canale alfa per l’effetto patch.

l&#39;effetto può essere controllato e convalidato rapidamente con [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

## Input

* **Input**: *Input colore*
* **Input maschera**: *Input scala di grigi*\
  Slot maschera opzionale utilizzato per mascherare la patch. Funziona come un alfa.

## Parametri

* **Abilita**: *False/True*\
  Attivare o disattivare l&#39;effetto applicazione di patch.
* **Visualizza helper fotogrammi**: *False/True*\
  Mostrare o nascondere le linee di supporto per il debug.
* **Thickness di fotogrammi**: *0,0 - 1,0*\
  Thickness di linee di supporto.
* **Scala patch**: *0,0 - 1,0*\
  Scala globale e uniforme della patch. Influisce sia sull&#39;origine che sulla destinazione.
* **Dimensione patch**: *0,0 - 1,0*\
  Dimensioni non uniformi del cerotto.
* **Rotazione patch**: *0.0 - 1.0*\
  Rotazione del cerotto. Influisce sull&#39;origine e sulla destinazione.
* **Alpha toppa**: *Quadrato uniforme, Gaussiano, Input maschera*\
  Imposta il valore alfa utilizzato per fondere il cerotto con lo sfondo.
* **Durezza patch**: *0,0 - 1,0*\
  Impostate la durezza/il contrasto dell&#39;alfa.
* **Offset rotazione origine**: *0,0 - 1,0*\
  Rotazione solo per la sorgente del cerotto.
* **Coordinate posizione**
  * **Posizione di origine**:\
    Posizione della sorgente. Ha maniglia nella vista 2D.
  * **Posizione patch**:\
    Posizione del bersaglio. Ha maniglia nella vista 2D.

## Immagini di esempio

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
