---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilizzate il nodo Selezione bordo per generare maschere selezionando i bordi della trama per creare effetti di usura e di resistenza agli agenti atmosferici basati sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selezione bordo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Selezione bordo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-select.png){width="128px"}

## Selezione bordo

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è il modo migliore per selezionare qualsiasi tipo di bordo in base alla curvatura. È possibile isolare Convessi, Concavi a qualsiasi livello o contrasto, fornendo una scorciatoia eccellente per evitare di farlo manualmente tramite un [nodo Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per evidenziare i bordi. Obbligatorio!
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta la quantità totale di evidenziazione del bordo per Convesso e Convesso.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto dell’evidenziazione sia per Convesso che per Convesso.
* **Convessa**
  * **Larghezza bordi convessi**: *0.0 - 1.0* Imposta la larghezza dell&#39;evidenziazione per i bordi convessi. Tenete presente che aumentando leggermente il valore Morbidezza si possono ottenere bordi più sottili.
  * **Sfumatura convessa**: *0.0 - 1.0* Impostate la sfumatura della transizione per i bordi convessi.
  * **Intensità convessa**: *0.0 - 1.0* Imposta l&#39;intensità massima dell&#39;evidenziazione del bordo per i bordi convessi. Impostare su 0 per non evidenziare.
* **Concave**
  * **Larghezza bordi concavi**: *0.0 - 1.0* Impostare la larghezza dell&#39;evidenziazione per i bordi concavi. Tenete presente che aumentando leggermente il valore Morbidezza si possono ottenere bordi più sottili.
  * **Sfumatura concava**: *0.0 - 1.0* Impostate la sfumatura della transizione per i bordi concavi.
  * **Intensità concava**: *0.0 - 1.0* Impostare l&#39;intensità massima dell&#39;evidenziazione dei bordi concavi. Impostare su 0 per non evidenziare.

## Immagini di esempio

![](../../../../../../assets/edge-select-ex.gif)

</td>
</tr>
</table>
