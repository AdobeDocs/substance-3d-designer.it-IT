---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Utilizzate il nodo Pennello superficie (Surface Brush) per generare maschere basate sull'orientamento della superficie e creare così effetti di usura e meteorologia direzionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pennello superficie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# Pennello superficie

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## Pennello superficie

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un effetto interessante del pennello metallico sulla superficie di un oggetto, occluso dalla geometria dell&#39;oggetto e da AO.

## Parametri

### Input

* **Spazio Mondiale Normale**: *Input Colore*
* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Posizione**: *Input scala di grigi*
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta il livello dell’effetto globale, rivelandolo gradualmente.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Durata Scratches**: *0.0 - 8.0* Imposta la lunghezza dei graffi. I valori più piccoli somigliano di più ai punti, mentre quelli più alti sono striature lunghe.
* **Occludi asse**: *X, Y, Z, nessuno* Asse dell&#39;oggetto che deve ricevere graffi. Non modifica la direzione dei graffi.
* **Occludi intensità asse**: *0.0 - 1.0* Intensità dell&#39;effetto di occlusione dell&#39;asse.
* **Occlusione**: *0.0 - 1.0* Intensità dell&#39;AO sull&#39;occlusione dei graffi.
* **Intensità nitidezza**: *0.0 - 1.0* Impostate la quantità di post-nitidezza da applicare ai graffi.

## Immagini di esempio

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
