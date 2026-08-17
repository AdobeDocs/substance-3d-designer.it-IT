---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Utilizzate il nodo Scansione istogramma per analizzare e analizzare gli istogrammi della texture per la correzione e le regolazioni del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scansione istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# Scansione istogramma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## Scansione istogramma

**Ingresso:** *Filtri/Regolazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo molto semplice ma utile che fornisce un modo intuitivo per ridefinire il contrasto e la luminosità delle immagini in scala di grigi in ingresso. Può essere utilizzato per &quot;far crescere&quot; e &quot;rimpicciolire&quot; le maschere in modo dinamico.

[Fate clic qui per guardare un video dell’Accademia di Substance sulle operazioni dell’Istogramma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## Parametri

* **Posizione**: *0.0 - 1.0* Analogamente a un controllo luminosità, sposta il punto medio del risultato. Quando viene utilizzato su un input sfumatura, questo espande e rimpicciolisce il punto di transizione.\
  Importante: un valore predefinito pari a 0 indica che il risultato finale è sempre nero, quindi prova a iniziare con 0,5.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato. Può essere utilizzato per impostare la durezza della transizione.
* **Inverti posizione**: *False/True* Inverte il risultato finale.

## Immagini di esempio

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
