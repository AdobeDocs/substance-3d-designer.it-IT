---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Usura pittura per generare maschere di usura della pittura in base alla geometria della trama per creare effetti di ritaglio della pittura realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usura pittura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---


# Usura pittura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/paint-wear.png){width="128px"}

## Usura pittura

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera ritaglia il colore e riduce i bordi.

## Parametri

### Input

* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Maschera variazione**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta la quantità totale di usura della pittura, rivelando gradualmente.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Occlusione**: *0.0 - 1.0* Imposta la quantità di effetto dell&#39;AO cotto sulla prevenzione dell&#39;usura nelle aree più scure.
* **Raggio**: *0.0 - 2.0* Imposta la distanza di diffusione dell&#39;effetto di ritaglio dai bordi convessi.
* **Variazione**: *0.0 - 1.0* Impostate la quantità di variazione (grunge) da fondere nell&#39;effetto.
* **Ignora maschera di variante**: *False/True* Abilita lo slot di input della mappa delle varianti personalizzate (grungi).

## Immagini di esempio

![](../../../../../../assets/paint-wear-ex.gif)

</td>
</tr>
</table>
