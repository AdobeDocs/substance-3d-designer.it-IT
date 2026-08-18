---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: Usa il nodo Sbiancamento sole per generare maschere basate sull’esposizione al sole per creare effetti realistici sbiancati e sbiaditi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sun Bleach
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Sun Bleach

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## Sun Bleach

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è simile a [Luce](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md), ma supporta anche AO, il che porta a una maschera che rappresenta lo sbiancamento della luce e la dissolvenza sopra un effetto.

## Input

* **Spazio mondo normale**: *Input colore*
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

## Parametri

* **Livello**: *0,0 - 1,0*\
  Consente di impostare la quantità totale di sbiancamento e di spostare l’effetto verso il basso.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Occlusione**: *0.0 - 1.0* Imposta l&#39;influenza dell&#39;AO sul risultato finale.

## Immagini di esempio

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
