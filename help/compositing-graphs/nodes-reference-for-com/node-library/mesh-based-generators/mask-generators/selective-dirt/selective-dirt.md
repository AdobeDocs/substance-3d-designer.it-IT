---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt selettivo per generare maschere di accumulo dirt selettivo in base alla geometria della trama per un'attenuazione atmosferica realistica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt selettivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Dirt selettivo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## Dirt selettivo

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) rappresenta un semplice effetto dirt sui bordi convessi.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Maschera variazione**: *Input scala di grigi*\
  Mappa di variazione facoltativa, che può essere abilitata tramite parametri.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta il livello totale dell’effetto, rivelandolo gradualmente.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Variazione**: *0.0 - 1.0* Imposta la quantità di variazione/grunge da fondere nell&#39;effetto.
* **Ignora maschera di variante**: *False/True* Consente di eseguire l&#39;override della variante con uno slot di input personalizzato.

## Immagini di esempio

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
