---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilizzate il nodo Proiezione planare 3D per proiettare le texture sulle superfici della trama utilizzando la proiezione planare per la mappatura delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proiezione planare 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Proiezione planare 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## Proiezione planare 3D (a colori)

**Ingresso:** *Generatori Basati Su Trama**/Utility*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una proiezione planare basata sui dati della trama cotta (Posizione e Mappe normali mondiali). Consente di proiettare e posizionare decalcomanie tra giunture, indipendentemente dalla mappatura UV originale.

## Parametri

### Input

* **Mappa posizione**: *Input colore* Mappa posizione al forno
* **Spazio Mondiale Normale**: *Input Colore* Mappa Normale Spazio Mondiale Al Forno
* **Texture proiettata**: *Input colore* Input texture per proiettare sulla destinazione.

### Parametri

* **Posizionamento**
  * **Input progetto**: *Posizione UV, Posizione spazio globale* Scegliere se la posizione di proiezione è impostata in 2D/UV o in uno spazio 3D/mondiale.
  * **Posizione UV di destinazione**:\
    Solo con input posizione UV, ideale per selezionare un punto nella vista 2D sulla mappa posizione.
  * **Posizione di destinazione**: *(valore colore)*Solo con l’input Posizione spazio mondo, consente di definire una coordinata 3D esatta.
  * **Target Normal**: *(valore colore)*
  * **Rotazione**: *0,0 - 1,0\
    Ruota la texture proiettata lungo l&#39;asse normale.*
  * **Scala**: *0,0 - 1,0*\
    Impostate la scala globale per la texture proiettata.
  * **Dimensioni**: *0,0 - 2,0* Eseguire il ridimensionamento non uniforme sulla texture proiettata.
* **Mascheratura**
  * **Profondità massima**: *0.0 - 1.0* Controlla la profondità in cui apparirà la texture proiettata, quando verrà tagliata.
  * **Dissolvenza Profondità**: *0.0 - 1.0* Impostare la transizione in modo che la profondità di taglio sia improvvisa o sbiadita.
  * **Soglia normale**: *-1.0 - 1.0* Impostare la soglia per le superfici non esattamente allineate con la normale di proiezione.
  * **Dissolvenza normale**: *0.0 - 1.0* Impostare la transizione per le superfici non allineate a una dissolvenza improvvisa o dissolvenza.

## Immagini di esempio

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
