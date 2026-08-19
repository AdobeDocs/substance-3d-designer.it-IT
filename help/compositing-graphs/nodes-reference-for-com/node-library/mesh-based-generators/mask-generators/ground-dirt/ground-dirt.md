---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt terreno per generare maschere di accumulo del dirt in base alla posizione e all’orientamento della trama rispetto al terreno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt terreno
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Dirt terreno

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## Dirt terreno

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un dirt accumulato da terra verso l&#39;alto, l&#39;opposto di [Dal basso in alto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) o [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). Non ha una sostituzione personalizzata della mappa.

## Input

* **Posizione**: *Input scala di grigi*\
  Mappa posizione al forno su cui basare l’effetto. Obbligatorio!
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

## Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta il livello di aspetto totale del dirt.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Height di Dirt**: *0.0 - 1.0* Imposta il height (proporzionalmente) in cui deve apparire il dirt.

## Immagini di esempio

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
