---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: Usate il nodo Altera per applicare alle texture gli effetti di distorsione e di spostamento necessari per la creazione di effetti di alterazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# Altera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Altera](warp.resources/warp-01.png "Nodo atomico: Altera"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Disperde i valori dei pixel nell’immagine di input in base alle pendenze calcolate da un input di sfumatura a parte, con conseguente deformazione.

A differenza dell’Alterazione direzionale, questo nodo si allontana in modo uniforme dalle aree bianche, in una direzione definita dalla pendenza o dalla sfumatura dell’Input sfumatura.

</td>
</tr>
</table>

L’utilizzo del nodo può essere un po’ complicato, in quanto il risultato dell’effetto dipende in larga misura dall’input sfumatura: piccole modifiche alla sfumatura possono fare un’enorme differenza visiva con gli stessi valori di intensità. Assicurati di provare Contrasto, Luminanza e scala dell&#39;Input sfumatura, nonché il cursore Intensità su questo nodo.

Se hai familiarità con le mappe normali, puoi immaginare che il funzionamento di questo nodo sia simile alla conversione dell&#39;input sfumatura in una [mappa normale](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), quindi alla distorsione dell&#39;input base nella direzione definita dai vettori della mappa normale. La stessa cosa si può ottenere con [Alterazione vettoriale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md). Effetti simili sono disponibili anche in [Sfocatura Pendenza](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

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
| <b>Intensità</b> *Mobile* | Consente di impostare l’intensità dell’alterazione. |
| <b>Modalità filtro input</b> *Booleano* | Controlla se per il campionamento dell’input viene utilizzato il filtro più vicino o bilineare. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | Immagine a colori o in scala di grigio. |
| <b>Input sfumatura</b> *Scala di grigi* | La pendenza del gradiente dell’immagine di input in scala di grigio determina l’effetto di alterazione nell’immagine di output. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
