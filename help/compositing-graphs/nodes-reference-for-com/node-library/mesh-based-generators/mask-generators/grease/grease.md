---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Utilizzate il nodo Grasso per generare maschere di accumulo del grasso in base alla geometria della trama e alle aree di contatto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grasso
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# Grasso

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## Grasso

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è stata creata appositamente per i volti dei personaggi e altre aree specifiche. Genera un tipo di maschera per ingrassaggio della pelle su aree con thickness basso.

## Parametri

### Input

* **Thickness**: *Input scala di grigi*\
  Mappa Thickness al forno su cui è basato l’intero effetto. Obbligatorio!
* **Disturbo**: *Input scala di grigi*\
  Facoltativo Mappa disturbo per sostituire Grassa grunge con.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Consente di impostare la quantità totale dell’effetto da visualizzare.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Soglia Thickness**: *0.0 - 1.0* Imposta il thickness minimo in cui deve comparire l&#39;effetto. Altrettanto importante è il livello. Modificalo per adattarlo alla mappa del Thickness.
* **Ignora disturbo**: *Falso/Vero* Impostare per ignorare la mappa interna della grunge grassa con uno slot di input personalizzato.

## Immagini di esempio

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
