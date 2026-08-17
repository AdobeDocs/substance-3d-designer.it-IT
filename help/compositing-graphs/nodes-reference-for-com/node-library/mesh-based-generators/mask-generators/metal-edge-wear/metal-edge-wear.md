---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Edge Wear metallo per generare maschere di usura sui bordi metallici in base alla curvatura e alla posizione della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear metallico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Wear metallico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## Edge Wear metallico

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta l&#39;usura dei bordi di un oggetto metallico, con graffi e scheggiature che appaiono sui bordi sollevati Convessi, potenzialmente mascherati da aree scure di AO cotte.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Input Grunge**: *Input scala di grigi*
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Spazio Mondiale Normale**: *Input Colore*
* **Posizione**: *Input colore*

### Parametri

* **Livello di usura**: *0,0 - 1,0* Imposta la quantità totale di usura, rivelando gradualmente.
* **Indossare il contrasto**: *0.0 - 1.0* Imposta il contrasto del risultato finale.
* **Smoothness bordi**: *0.0 - 16.0* Imposta lo smoothness del decadimento dai bordi dalla curvatura.
* **Quantità Grungi**: *0,0 - 1,0* Imposta la quantità di grungi da fondere tra i bordi.
* **Scala Grungi**: *1 - 16* Imposta la scala delle Grungi.
* **Mascheratura Occlusione ambiente**: *0.0 - 1.0* Imposta l&#39;effetto dell&#39;AO sull&#39;effetto finale, escludendo le aree scure.
* **Spessore curvatura**: *0,0 - 1,0* Imposta la quantità di effetto che i bordi convessi della curvatura hanno sull&#39;effetto finale.
* **Usa Grunge personalizzata**: *False/True* Abilita uno slot di input personalizzato per la mappa della Grunge.
* **Usa Triplanare**: *Falso/Vero* Abilita proiezione [Triplanare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) per nascondere le giunture.
* **Contrasto fusione triplanare**: *0.0 - 1.0* Imposta il contrasto di fusione per la proiezione triplanare.

## Immagini di esempio

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
