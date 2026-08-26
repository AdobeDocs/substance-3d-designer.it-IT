---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Utilizzate il nodo Combinazione normale per combinare più mappe normali per creare livelli di dettagli e superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinazione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# Combinazione normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

<b>In:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Combinazione normale combina i dettagli di due mappe normali in modo matematicamente corretto.

È simile al noto metodo &quot;Overlay&quot; di altri software di editing di immagini 2D, ma funziona internamente in modo leggermente diverso (tre opzioni).

</td>
</tr>
</table>

Questo è il modo migliore e più corretto per aggiungere a una mappa con baking i dettagli della mappa normale generati in 2D.

Se desideri unire due mappe normali senza combinarne i dettagli (ad esempio, utilizzando una maschera), devi utilizzare [Fusione normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md).

## Connettori di ingresso

<b>Normale 2</b> *Colore* Descrizione

<b>Normale 1</b> *Colore* Descrizione

## Parametri

<b>Tecnica</b> *Numero intero* Imposta la tecnica di fusione interna da utilizzare, impostando la velocità in base alla qualità.\
*- Sbianca (bassa qualità)
* Miscelatore canale (alta qualità)
* Orientamento ai dettagli (alta qualità)*

## Esempi
