---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Utilizza il nodo Da Flood Fill a colore scala di grigio per riempire le aree collegate con colori in scala di grigio per la creazione di pattern monocromatici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da Flood Fill a Scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Da Flood Fill a scala di grigi/colore

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fill a gradazioni di grigio/colore casuali

**Ingresso:** *Filtri/Effetti*

**&#x200B;**&#x200B;Semplice&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Usa i dati di Flood Fill per generare campioni di valori cromatici o in scala di grigio. A differenza di [Flood Fill a gradazioni di grigio casuali](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), questi due nodi consentono un maggiore controllo per impostare la variazione e i toni esatti, con una mappa di input aggiuntiva per determinare il valore base da casualizzare per cella.

È un sistema potente che offre a ogni cella un valore o un colore unico, mantenendo comunque il controllo e basandolo su un input predeterminato.

## Parametri

### Input

* **Flood Fill**: *Input colore*
* **Input colore/scala di grigi**: *Input colore/scala di grigi*

### Parametri

* **Regolazione luminanza/colore**: *-1.0 - 1.0* Impostare il valore di distorsione o di base per il nodo. Quando si utilizza un input Scala di grigio o Colore, questo viene utilizzato per modificare il valore iniziale come punto di partenza.
* **Luminanza/Colore casuale**: *-1.0 - 1.0* Impostate la quantità di variazione.

</td>
</tr>
</table>
