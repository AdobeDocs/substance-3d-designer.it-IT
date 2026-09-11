---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rilievo per creare effetti in rilievo sulle texture e aggiungere profondità e rilievo ai dettagli delle superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Effetto rilievo
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 9%

---


# Effetto rilievo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Rilievo](emboss.resources/comp_emboss_1.png "Nodo atomico: Rilievo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Applica un effetto rilievo illuminando i lati delle forme in un’immagine a seconda della direzione della sorgente di luce specificata.

Ad esempio, il nodo esegue una semplice ombreggiatura 2D basata su 2 input, simulando la caduta della luce su una superficie con variazione di height e profondità.

</td>
</tr>
</table>

Questo nodo non viene utilizzato spesso per progetti di tipo PBR, ma può essere utile in alcuni casi in cui si desidera una semplice illuminazione al forno nella texture. In alternativa, [Rilievo con lucentezza](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) e [Rilievo di Uber](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) offrono una funzionalità simile ma più ampia.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Intensità</b> *Mobile* | Regola l’intensità globale dell’effetto di illuminazione.   Consente di impostare l’intensità della mappa del &quot;height&quot; e quindi l’intensità dell’effetto di luce. |
| <b>Angolo chiaro</b> *Mobile* | Consente di impostare l’angolo di simulazione della luce.   Definisce l’angolo di illuminazione della luce dell’immagine in rilievo. |
| <b>Colore evidenziazione</b> *Float/Float4* | Consente di impostare il colore delle aree rivolte verso l’angolo di luce.   Consente di impostare il colore dell’evidenziazione se l’immagine di input è a colori. |
| <b>Colore ombra</b> *Float/Float4* | Consente di impostare il colore delle aree rivolte all’esterno dell’angolo di luce.   Imposta il colore delle aree in ombra dell’immagine in rilievo. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | Fornisce i colori di base non ombreggiati. La vedete come una sorta di texture diffusa o di colore di base. |
| <b>Input intensità</b> *Scala di grigi* | Rappresenta la mappa di altezza utilizzata per calcolare l&#39;illuminazione sulla superficie. Il nero è basso e il bianco è alto. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
