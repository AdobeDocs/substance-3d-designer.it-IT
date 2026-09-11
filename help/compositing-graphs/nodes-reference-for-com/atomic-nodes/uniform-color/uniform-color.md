---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: Utilizzate il nodo Colore uniforme per generare texture di colore uniformi per la creazione di riempimenti di colore uniforme e livelli base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# Colore uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: colore uniforme](uniform-color.resources/comp_uniform_1.png "Nodo atomico: colore uniforme"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Genera un valore piatto a colori o in scala di grigi.

Si tratta di un nodo semplice che viene utilizzato molto spesso come punto di partenza per aggiungere colori o creare valori specifici.

</td>
</tr>
</table>

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

>[!TIP]
>
> Ottimizzazione delle prestazioni
> 
> Entrambe queste regolazioni riducono il tempo di calcolo del nodo e l&#39;ingombro della memoria:
> 
> * Se è necessario un valore in scala di grigio, assicurarsi di impostare il [metodo colore](#parameters) del nodo su &#39;Scala di grigio&#39;.
> * Poiché l&#39;output del nodo è un colore piatto, è possibile utilizzare la risoluzione più bassa possibile. Impostare il parametro &#39;[Dimensioni output](../../../../compositing-graphs/output-size/output-size.md)&#39; del nodo per utilizzare il [metodo di ereditarietà &#39;Absolute&#39;](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) e una risoluzione di 16x16 pixel.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parametri

</td>
<td style="border: 0;" valign="top">

### Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Metodo colore</b> *Booleano* | Alterna tra un’immagine in scala di grigio e un’immagine a colori in output. |
| <b>Colore di output</b> *Float/Float4* | Seleziona il colore piatto da usare nell’immagine di output.   Quando si utilizza il metodo colore, il canale di Alpha viene usato per l’opacità, dove 0 è completamente trasparente e 1 è completamente opaco. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Colore/Scala di grigi* |  |

## Esempi

*Disponibile a breve.*
