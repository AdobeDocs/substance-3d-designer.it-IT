---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Utilizzate il nodo Hald CLUT per applicare le tabelle di consultazione del colore utilizzando il formato Hald CLUT per la correzione e la correzione del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## Hald CLUT

**Ingresso:** *Filtri/Regolazioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Applica un LUT all&#39;immagine di input. Il LUT deve essere in formato Hald con risoluzione 4096\*4096. Per ulteriori informazioni, vedere <http://www.quelsolaar.com/technology/clut.html>.

### Input

* **input**: *Input colore*\
  Immagine su cui applicare il LUT.
* **lut**: *Input colore* Slot di input Lut. Deve essere 4096x4096.

## Parametri

* **Intensità LUT per Alpha**: *False/True* Definisce se l&#39;effetto LUT è ponderato dal canale alfa.

Esempi

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
