---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Utilizzate il nodo Usura in pelle per generare maschere di usura sulle superfici in pelle in base alla curvatura della trama e ai punti di contatto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usura in pelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Usura in pelle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## Usura in pelle

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta l&#39;usura con un motivo in pelle, con più usura sui bordi in base alla curvatura. È simile all&#39;[Edge Wear in fibra di vetro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) in termini di funzionalità e ha principalmente gli stessi parametri.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per il posizionamento degli spigoli. Obbligatorio!
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per occludere determinate aree. Consigliato, ma non obbligatorio.
* **Input Grunge**: *Input scala di grigi*\
  Slot di input mappa Grunge opzionale che può essere attivato tramite il parametro &quot;Usa Grunge personalizzata&quot;.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello di usura**: *0.0 - 1.0* Imposta il livello di usura globale, rivelando gradualmente.
* **Contrasto usura**: *0.0 - 1.0* Imposta il contrasto dell&#39;effetto.
* **Quantità Grungi**: *0,0 - 1,0* Imposta la quantità di grungi (motivo di pelle predefinito) da fondere tra i bordi.
* **Mascheratura Occlusione ambiente**: *0.0 - 1.0* Imposta l&#39;entità con cui l&#39;AO maschera gli effetti di usura.
* **Spessore curvatura**: *0.0 - 1.0* Imposta l&#39;estensione con cui i bordi della curvatura influiscono sul risultato finale. Anche se è impostato su 0, è comunque necessaria una mappa di curvatura.
* **Usa Grunge personalizzata**: *False/True* Consente l&#39;override del motivo di pelle predefinito incorporato. Utilizzare invece uno slot di input personalizzato.

## Immagini di esempio

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
