---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce per generare maschere in base alle condizioni di illuminazione della trama per creare variazioni di materiale realistiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# Luce

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## Luce

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è un po&#39; diversa dagli altri Generatori: semplicemente fa una falsa illuminazione, basata sulla mappa normale dello spazio mondiale, restituendo una maschera &quot;lightmap&quot; in bianco e nero.

## Parametri

* **Angolo orizzontale**: *0.0 - 1.0* Imposta l&#39;angolo orizzontale della luce falsa.
* **Angolo verticale**: *0.0 - 1.0* Imposta l&#39;angolo verticale della luce falsa.
* **Luce lucidità**: *0.0 - 0.999* Imposta la diffusione di decadimento dell&#39;area evidenziata.
* **Livello di evidenziazione**: *0.0 - 1.0* Imposta il livello di luminosità dell&#39;area evidenziata.

## Immagini di esempio

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
