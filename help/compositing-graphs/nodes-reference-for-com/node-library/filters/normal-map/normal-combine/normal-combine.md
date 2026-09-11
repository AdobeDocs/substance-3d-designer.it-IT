---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Utilizzate il nodo Combinazione normale per combinare più mappe normali per creare livelli di dettagli e dettagli delle superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinazione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Combinazione normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Normale Combina i dettagli di due mappe normali in modo matematicamente corretto.

È simile al noto metodo &quot;Overlay&quot; di altri software di editing di immagini 2D, ma funziona internamente in modo leggermente diverso (tre opzioni).

</td>
</tr>
</table>

Questo è il modo migliore e più corretto per aggiungere dettagli di mappa normale 2D a una mappa con baking.

Se desideri fondere due mappe normali senza combinarne i dettagli (ad esempio, utilizzando una maschera), devi utilizzare [Fusione normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Normale 2</b> <i>Colore</i> | Descrizione |
| <b>Normale 1</b> <i>Colore</i> | Descrizione |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Tecnica</b> *Numero intero* | Consente di impostare la tecnica di fusione interna da utilizzare, in modo da ottenere un risultato in termini di velocità.<br><br>*- Whiteout (bassa qualità)<br>* Miscelatore canale (alta qualità)<br>* Dettagliato (alta qualità)* |

## Esempi
