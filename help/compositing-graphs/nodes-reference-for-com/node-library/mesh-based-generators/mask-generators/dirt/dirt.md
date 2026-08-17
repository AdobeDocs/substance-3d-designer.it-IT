---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt per generare maschere di accumulo dirt in base alla curvatura, alla posizione e all'occlusione della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Terra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 2%

---


# Terra

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dirt.png){width="128px"}

## Terra

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta i dirt in bordi e angoli occlusi e incassati, in base all&#39;AO cotto e alla curvatura.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura. Obbligatorio!
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura. Obbligatorio!
* **Input Grunge**: *Input scala di grigi*\
  Input mappa grunge personalizzata, facoltativo, abilitato dal parametro.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Spazio Mondiale Normale**: *Input Colore*\
  Utilizzato solo per Triplanare.
* **Posizione**: *Input colore*\
  Utilizzato solo per Triplanare.

### Parametri

* **Livello Dirt**: *0,0 - 1,0* Controllo principale per la quantità di dirt.
* **Contrasto Dirt**: *0.0 - 1.0* Controlla il contrasto principale per il dirt nella maschera.
* **Quantità di Grungi**: *0,0 - 1,0* Imposta la grunge del dirt. Impostate su 0 per un dirt perfettamente uniforme.
* **Mascheratura bordi**: *0.0 - 1.0* Quantità di dirt da rimuovere dai bordi sollevati (in base alla mappa di curvatura).
* **Usa Grunge personalizzata**: *False/True* Consente di utilizzare l&#39;input della mappa della grunge personalizzata anziché la Grunge incorporata.
* **Scala Grungi**: *1 - 16* Imposta la scala di affiancamento dei dettagli delle Grungi.
* **Usa Triplanare**: *Falso/Vero* Usa [Proiezione Triplanare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) per la mappatura delle Grungi, rimuove le cuciture.
* **Contrasto fusione triplanare**: *0.001 - 1.0* Imposta il contrasto della proiezione triplanare.

## Immagini di esempio

![](../../../../../../assets/dirt-ex.gif)

</td>
</tr>
</table>
