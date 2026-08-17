---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear per generare maschere di usura sui bordi della trama per creare danni realistici ai bordi e effetti meteorologici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questo nodo rappresenta l&#39;usura sui bordi degli oggetti. Ha alcuni parametri, ma non è il più facile da usare: ti consigliamo di giocare e dare un&#39;idea delle cose. Il nodo è abbastanza potente, anche se non è possibile eseguire alcuna maschera di esclusione personalizzata.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta la diffusione totale dell’effetto.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Soglia**: *0.0 - 1.0* Simile al livello, imposta la diffusione totale dell&#39;effetto.
* **Larghezza bordi**: *0.0 - 1.0* Imposta la pienezza dell&#39;effetto di evidenziazione. Riduceteli per renderli più brillanti.
* **Disturbo**: *0,0 - 1,0*\
  Imposta la quantità di disturbo da fondere per separare lo smoothness.

## Immagini di esempio

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
