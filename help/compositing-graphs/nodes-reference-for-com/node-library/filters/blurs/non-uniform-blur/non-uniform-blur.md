---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sfocatura non uniforme per applicare la sfocatura con diverse intensità nelle direzioni X e Y per gli effetti anisotropi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Sfocatura non uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

## Sfocatura non uniforme (scala di grigi)

**Ingresso:** *Filtri/Sfocature*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una Sfocatura di alta qualità, in cui l’intensità è determinata da una maschera di input. Le opzioni consentono l&#39;aggiunta di Anisotropia e assimetria.

## Parametri

### Input

* **Mappa sfocatura**: *Input scala di grigi* Mappa maschera per aumentare la forza dell&#39;effetto.

### Parametri

* **Intensità**: *0.0 - 50.0* Intensità massima per applicare la sfocatura. Con la maschera della Mappa sfocatura, questa impostazione non avrà alcun effetto sulle aree nere della mappa.
* **Anisotropia**: *0.0 - 1.0* Facoltativamente aggiunge direzionalità all&#39;effetto di sfocatura. Guidata dal parametro Angle.
* **Asimmetria**: *0.0 - 1.0* Facoltativamente, aggiunge una distorsione al campionamento. Guidata dal parametro Angle.
* **Angolo**: *0.0 - 1.0* Angolo per impostare la direzionalità e la distorsione di campionamento.
* **Campioni**: *1 - 16* Quantità di campioni, determina la qualità. Moltiplicato per la quantità di blade.
* **Blade**: *1 -* 9\
  Quantità di settori di campionamento, determina la qualità. Moltiplicato per la quantità di campioni.

## Immagini di esempio

*Nell&#39;esempio seguente viene utilizzata una sfumatura a 90 gradi nello slot Mappa sfocatura.*

![](../../../../../../assets/nonuniform-example.gif)

</td>
</tr>
</table>
