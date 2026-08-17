---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spigolo (Edge Speckle) per generare pattern di usura con chiazze sui bordi della trama per creare effetti di danno realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## Edge Speckle

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta i bordi con una leggera macchia aggiunta per dividerli. Vedere anche [Dirt Edge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per l&#39;evidenziazione dei bordi. Obbligatorio!
* **Maschera variazione**: *Input scala di grigi*\
  Slot maschera opzionale utilizzato per mascherare gli effetti del nodo. Attivare con &quot;Ignora maschera di variazione&quot;.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta la quantità totale di evidenziazione dei bordi.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Selezione bordo**: *0.0 - 1.0* Imposta l&#39;influenza dei bordi convessi.
* **Variazione**: *0.0 - 1.0* Imposta l&#39;entità della divisione dell&#39;effetto della maschera di variazione.
* **Sovrascrivi maschera di variazione**: *False/True* Sovrascrive la maschera incorporata con uno slot di input personalizzato.

## Immagini di esempio

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
