---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: Utilizza il nodo Colore da mascherare per convertire determinati colori in maschere al fine di creare effetti di elaborazione e mascheratura selettivi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore da mascherare
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# Colore da mascherare

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Colore da mascherare - Icona](../../../../../../assets/color_to_mask.png "Colore da mascherare - Icona"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Estrae una maschera in scala di grigi dai colori selezionati in un’immagine a colori.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Input

</td>
<td style="border: 0;" valign="top">

### Output

</td>
<td style="border: 0;" valign="top">

### Parametri

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Input

|  |  |
| --- | --- |
| Colore <b>Input</b> | Immagine a colori di input da cui deve essere estratta una maschera in base ai suoi colori. |
| <b>Input colore</b> Colore *Disponibile quando &#39;Usa input colore&#39; è impostato su &#39;True&#39;* | Immagine a colori di input utilizzata per definire il colore di riferimento per pixel. |

## Output

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | La maschera generata come bitmap in scala di grigio. |

## Parametri

|  |  |
| --- | --- |
| <b>Usa input colore</b> booleano | Utilizzate un’immagine di input invece di un colore uniforme, per definire un colore di riferimento per pixel.    L&#39;immagine di input è fornita dall&#39;input <b>Color</b>. |
| <b>Colore</b> Float3 *Disponibile quando &#39;Usa input colore&#39; è impostato su &#39;False&#39;* | Colore uniforme di riferimento attorno al quale deve essere eseguita la selezione del colore. |
| <b>Soglia</b> Mobile | Distanza dal colore di riferimento sotto il quale vengono selezionati i colori. |
| <b>Dissolvenza selezione</b> Mobile | Applica la dissolvenza alla selezione del colore in base alla distanza dal colore di riferimento. |
| <b>Spazio colore distanza</b> Intero | Il processo Equalizza prevede il confronto dei colori per determinare la distanza tra di essi. Alcuni spazi colore e algoritmi di distanza sono più adatti a casi d&#39;uso specifici.   Questo elenco a discesa consente di selezionare lo spazio colore utilizzato per confrontare i colori:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB (dati):</i></b> il colore viene suddiviso nei canali Rosso, Verde e Blu e distribuito direttamente lungo tali assi, ignorando la percezione umana. Questa opzione è indicata per le immagini contenenti dati non elaborati.</li> <li data-preserve-html="true"><i>Lineare sRGB (colore):</i> il colore viene suddiviso nei canali Rosso, Verde e Blu e distribuito in una relazione lineare con l’intensità della luce dei pixel. Questa opzione è indicata per immagini che possono essere visualizzate su schermi.</li> <li data-preserve-html="true"><b><i>Luminanza (colore):</i></b> il colore viene suddiviso in valori di tonalità, crominanza e luminanza in cui solo il valore di luminanza viene utilizzato nel confronto. Questa opzione è indicata per immagini che possono essere visualizzate su schermi.</li> <li data-preserve-html="true"><i>Lab (Colore):</i> uno spazio colore percettivo standardizzato, che distribuisce i colori in modo tale che quelli più vicini siano effettivamente vicini nel cubo. Questa opzione è indicata per immagini che possono essere visualizzate su schermi.</li> <li data-preserve-html="true"><i>Angolo (normale):</i> il colore viene suddiviso negli assi X, Y, Z di un vettore e confrontato attraverso un prodotto dot. Questa opzione è indicata per le immagini contenenti Normali dello spazio tangente.</li> </ul> |
| <b>Spessori distanza</b> Float3 | L&#39;algoritmo della distanza del colore Lab (DeltaE2000) introduce determinati fattori di peso per ciascun valore di luminosità, crominanza e tonalità.   Valori più bassi diminuiranno l’influenza dei fattori nell’algoritmo per la differenza dei colori.   Poiché l&#39;occhio generalmente accetta differenze maggiori nella luminosità (L) rispetto alla crominanza (C) o alla tonalità (H), un rapporto predefinito per (L:C:H) è (0,5:1:1). Un rapporto di 0,5:1:1 consente di ottenere una differenza di luminosità doppia rispetto a quella ottenuta con crominanza o tonalità. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
