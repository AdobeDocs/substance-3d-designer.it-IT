---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ""
description: Usate il nodo Alterazione direzione per applicare la distorsione direzionale alle texture per creare effetti di flusso e movimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterazione direzionale
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 9%
---

# Alterazione direzionale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: alterazione direzionale](directional-warp.resources/comp_directionalwarp_1.png "Nodo atomico: alterazione direzionale")

</td>
<td style="border: 0;" valign="top">

Sposta i pixel in una direzione specifica in base a una mappa di intensità, con possibile deformazione.

Altera un input nella direzione impostata dall’utente, moltiplicato per una mappa di intensità impostata dall’utente. Funziona in modo simile a Altera, ma solo in una direzione specifica.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="directional-warp.resources/directional-warp-tooltip.gif" alt="descrizione comando per alterazione direzione" /></div>

Il nodo Altera è un nodo semplice ma utile che può essere utilizzato come base per altri effetti più avanzati. Ci sono alternative più avanzate, ad esempio altri nodi correlati di interesse sono [Sfocatura Pendenza](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) e [Alterazione vettoriale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).



## Parametri

|  |  |
| --- | --- |
| <b>Intensità</b> *Mobile* | Consente di impostare l’intensità dell’alterazione. |
| <b>Angolo di alterazione</b> *Mobile* | Imposta l’angolo dell’effetto di alterazione, in numero di giri. |
| <b>Modalità filtro input</b> *Booleano* | Controlla se per il campionamento dell&#39;<b>input</b> viene utilizzato il filtro più vicino o bilineare. |
| <b>Offset mappa intensità</b> *Mobile* | Questo valore viene sottratto dai valori dell&#39;immagine <b>di input intensità</b>. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | L’immagine in scala di grigio o a colori di input sulla quale deve essere applicato l’effetto di alterazione. |
| <b>Input intensità</b> *Scala di grigi* | Immagine in scala di grigio che definisce la quantità di alterazione da applicare all&#39;immagine <b>Input</b>. |


## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Alterazione direzionale - Esempio 1](directional-warp.resources/dir-warp.gif "Alterazione direzionale - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Alterazione direzionale - Esempio 2](directional-warp.resources/dir-warp02.gif "Alterazione direzionale - Esempio 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Alterazione direzionale - Esempio 3](directional-warp.resources/dir-warp03.gif "Alterazione direzionale - Esempio 3"){zoomable="yes"}

</td>
</tr>
</table>
