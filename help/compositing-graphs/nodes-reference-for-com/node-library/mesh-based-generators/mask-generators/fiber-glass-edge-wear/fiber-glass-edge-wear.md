---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear fibra di vetro per generare maschere di usura sui bordi in fibra di vetro in base alla curvatura della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear in fibra di vetro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# Edge Wear in fibra di vetro

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fiber-glass-edge-wear.png){width="128px"}

## Edge Wear in fibra di vetro

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Rappresenta una maschera specificamente destinata a un&#39;usura di tipo vetroresina, potrebbe forse essere utilizzata per panno. A causa della natura molto piastrellata e ripetitiva delle fibre, la fusione triplanare può opzionalmente essere abilitata.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per evidenziare i bordi. Obbligatorio!
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per mascherare le aree occluse. Non richiesto, ma sicuramente consigliato.
* **Input Grunge**: *Input scala di grigi*\
  Slot personalizzato opzionale per ignorare il motivo a fibra.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Spazio Mondiale Normale**: *Input Colore*\
  Utilizzato solo per Triplanare.
* **Posizione**: *Input colore*\
  Utilizzato solo per Triplanare.

### Parametri

* **Livello di usura**: *0.0 - 1.0* Come una [scansione di istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), rivela progressivamente l&#39;usura.
* **Contrasto usura**: *0.0 - 1.0* Imposta il contrasto totale dell&#39;effetto.
* **Smoothness bordi**: *0.0 - 16.0* Imposta l&#39;effetto di sfocatura dai bordi evidenziati.
* **Quantità Grunge**: *0,0 - 1,0* Imposta l’entità dell’effetto fibra da fondere tra i bordi. Modificate questo valore insieme a Livello di usura per ottenere il massimo controllo.
* **Mascheratura Occlusione ambiente**: *0.0 - 1.0* Imposta l&#39;influenza dell&#39;AO nel nascondere l&#39;effetto.
* **Spessore curvatura**: *0,0 - 1,0* Imposta la quantità di influenza esercitata dai bordi convessi della curvatura.
* **Usa Grunge personalizzata**: *False/True* Esegue l&#39;override delle fibre incorporate con la mappa personalizzata.
* **Usa Triplanare**: *Falso/Vero* Consente a [Triplanare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) di nascondere le giunture.
* **Contrasto fusione triplanare**: *0.0 - 1.0* Controlla il contrasto dell&#39;effetto triplanare.

## Immagini di esempio

![](../../../../../../assets/fiber-glass-edge-wear-ex.gif)

</td>
</tr>
</table>
