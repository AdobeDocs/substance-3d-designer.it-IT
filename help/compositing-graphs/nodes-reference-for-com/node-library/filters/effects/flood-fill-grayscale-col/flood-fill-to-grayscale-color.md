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
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Da Flood Fill a scala di grigi/colore

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/floodfill-to-grayscale.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/floodfill-to-color.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Usa i dati di Flood Fill per generare campioni di valori cromatici o in scala di grigio. A differenza di [Flood Fill a gradazioni di grigio casuali](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), questi due nodi consentono un maggiore controllo per impostare la variazione e i toni esatti, con una mappa di input aggiuntiva per determinare il valore base da casualizzare per cella.

È un sistema potente che offre a ogni cella un valore o un colore unico, mantenendo comunque il controllo e basandolo su un input predeterminato.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Input colore</i> |  |
| <b>Input colore/scala di grigi</b> <i>Input colore/scala di grigi</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Regolazione Luminanza/Colore</b> <i>-1.0 - 1.0</i> | Impostare la distorsione o il valore base per il nodo. Quando si utilizza un input Scala di grigio o Colore, questo viene utilizzato per modificare il valore iniziale come punto di partenza. |
| <b>Luminanza/Colore casuale</b> <i>-1.0 - 1.0</i> | Imposta l&#39;importo della variazione. |
