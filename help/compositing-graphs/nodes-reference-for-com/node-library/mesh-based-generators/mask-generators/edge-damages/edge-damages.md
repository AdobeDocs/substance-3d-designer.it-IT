---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-damages.html"
breadcrumb-title: ''
description: Utilizzate il nodo Danni bordo per generare maschere di danno sui bordi della trama per creare effetti realistici di usura e rottura dei bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Damages
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Danni ai bordi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 2%

---


# Danni ai bordi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-damages.png){width="128px"}

## Danni ai bordi

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta il danno arrecato ai bordi convessi in rilievo in base alla curvatura e all’AO cotto.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per il posizionamento degli effetti. Obbligatorio!
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per il posizionamento degli effetti. Obbligatorio!
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Quantità di danno al bordo da applicare.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Intensità danni**: *0.0 - 1.0* Si sposta tra un aspetto frammentato e uniforme e un aspetto caotico, graffiato e fortemente danneggiato.

## Immagini di esempio

![](../../../../../../assets/edge-damages-ex.gif)

</td>
</tr>
</table>
