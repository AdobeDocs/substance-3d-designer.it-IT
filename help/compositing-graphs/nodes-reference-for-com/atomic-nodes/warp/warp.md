---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ""
description: Usate il nodo Altera per applicare gli effetti distorsione alle texture per la creazione di effetti di alterazione e spostamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Altera
user-guide-description: ""
user-guide-title: ""
source-git-commit: b2c99a199364ff62b5790b72bcfef02a35d58ca2
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 9%
---

# Altera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Altera](warp.resources/comp_warp_1.png "Nodo atomico: Altera"){width="20%"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Disperde i valori dei pixel nell’immagine di input in base alle pendenze calcolate da un input di sfumatura a parte, con conseguente deformazione.

A differenza dell’Alterazione direzionale, questo nodo si allontana in modo uniforme dalle aree bianche, in una direzione definita dalla pendenza o dalla sfumatura dell’input sfumatura.

</td>
</tr>
</table>

<div data-preserve-html="true" style="display: block; margin: auto;"><img src="warp.resources/warp-tooltip.gif" alt="descrizione comando altera" /></div>

L’utilizzo del nodo può essere un po’ complicato, in quanto il risultato dell’effetto dipende in larga misura dall’input sfumatura: piccole modifiche alla sfumatura possono fare un’enorme differenza visiva con gli stessi valori di intensità. Assicurati di provare Contrasto, Luminanza e scala dell&#39;Input sfumatura, nonché il cursore Intensità su questo nodo.

Se hai familiarità con la Mappa normale, puoi immaginare che il funzionamento di questo nodo sia simile alla conversione dell&#39;input sfumatura in una [Mappa normale](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) e quindi alla distorsione dell&#39;input base nella direzione definita dai vettori della Mappa normale. La stessa cosa si può ottenere con [Alterazione vettoriale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md). Effetti simili sono disponibili anche in [Sfocatura Pendenza](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).



## Parametri

|  |  |
| --- | --- |
| <b>Intensità</b> *Virgola mobile* | Consente di impostare l’intensità dell’alterazione. |
| <b>modalità di filtro di input</b> *Booleano* | Controlla se per il campionamento dell’input viene utilizzato il filtro più vicino o bilineare. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | Immagine a colori o in scala di grigio. |
| <b>Input sfumatura</b> *Scala di grigi* | La pendenza del gradiente dell’immagine di input in scala di grigio determina l’effetto di alterazione nell’immagine di output. |


## Esempi

*Disponibile a breve.*
