---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt bordi (Edge) per generare maschere di accumulo dirt sui bordi della trama per creare effetti meteorologici realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt bordi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# Dirt bordi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## Dirt bordi

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un effetto dirt che si accumula attorno ai bordi, basato solo su una mappa di curvatura.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per il posizionamento degli effetti. Obbligatorio!
* **Maschera variazione**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo, utilizzato solo quando è abilitato il parametro di esclusione.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta la quantità di dirt.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Variazione**: *0.0 - 1.0* Miscela la quantità di mascheratura/suddivisione su larga scala che deve essere applicata.
* **Ignora maschera variante**: *False/True*

## Immagini di esempio

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
