---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: Utilizzare il nodo Conversione gradazioni di grigio per convertire le texture di colore in gradazioni di grigio utilizzando vari metodi di conversione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversione in scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 7%

---


# Conversione in scala di grigi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: conversione in scala di grigi](grayscale-conversion.resources/comp_grayscaleconversion_1.png "Nodo atomico: conversione in scala di grigi"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Converte un’immagine a colori in scala di grigi pesando la luminanza di ciascun canale di colore.

Questo nodo può essere utilizzato come metodo ottimizzato per estrarre un canale in scala di grigio da un’immagine a colori, impostando tutti i valori di &quot;Spessori canale&quot; su 0 ad eccezione del canale desiderato, che deve essere impostato su 1.

</td>
</tr>
</table>

La maggior parte dei nodi può essere impostata per l&#39;output in scala di grigio o a colori, in cui il primo è preferito per motivi di semplicità e prestazioni.

In effetti, si consiglia di lavorare in scala di grigi sin dall&#39;inizio e colorare le immagini in un secondo momento del flusso di lavoro, utilizzando ad esempio un nodo [Mappa sfumatura](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md).

Ciò significa che un nodo di conversione della scala di grigi è generalmente riservato solo per i casi in cui si desidera convertire specificamente un&#39;immagine a colori in scala di grigi. In questi casi potete anche osservare la [conversione avanzata della scala di grigi](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) e il [colore da mascherare](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md).

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

## Parametri

</td>
<td style="border: 0;" valign="top">

### Connettori di ingresso

</td>
<td style="border: 0;" valign="top">

### Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Spessori canale</b> *Float4* | Imposta lo spessore di ciascuno dei canali RGBA nella conversione in scala di grigio.   Per impostazione predefinita, viene effettuata una divisione uniforme sui canali RGB. |
| <b>Alfa unico livello</b> *Booleano* | Imposta il comportamento dell&#39;Alpha sul risultato finale in scala di grigio, in quanto i valori in scala di grigio non possono contenere informazioni Alpha.   Se *è True*, la conversione in scala di grigio viene moltiplicata per il canale di Alpha dell&#39;immagine di input. |
| <b>Valore sfondo</b> *Mobile* | Imposta il valore dello sfondo di base quando l’input ha una maschera alfa. Ad esempio, determina quali pixel devono essere trattati come trasparenti.   *Disponibile quando &#39;Unico livello alfa&#39; è impostato su &#39;True&#39;.* |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Colore* PRIMARIO | Immagine a colori da elaborare. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* |  |

## Esempi

*Disponibile a breve.*
