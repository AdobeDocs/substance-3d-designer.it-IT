---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Utilizzare il nodo Elenco punti per creare e gestire elenchi di punti per la generazione di spline e percorsi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elenco punti
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Elenco punti

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](point-list.resources/point-list-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera un elenco di punti attraversati da una spline.

Se agli input di <b>Point</b> viene fornito un elenco di punti esistente, l&#39;elenco generato viene aggiunto all&#39;elenco di input.

</td>
</tr>
</table>

>[!TIP]
>
> Questo nodo può essere utilizzato per fornire punti al nodo [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) per generare spline.

>[!IMPORTANT]
>
> I connettori <b>Elenco punti</b> e <b>Numero punto</b> sono *incompatibili* con <b>Coord spline</b>, <b>Dati spline</b> e <b>Quantità spline</b>, in quanto si basano su dati diversi.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima dei punti come immagine in scala di grigio. |
| <b>Input elenco punti</b> <i>Colore</i> | Elenco di punti di input codificati nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> * Parte intera: Smoothness;<br> * Parte frazionale: Thickness. |
| <b>Input numero punto</b> <i>Numero intero</i> | Numero di punti di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima dei punti come immagine in scala di grigio. |
| <b>Elenco punti</b> <i>Colore</i> | Elenco di output dei punti codificati nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> * Parte intera: Smoothness;<br> * Parte frazionale: Thickness. |
| <b>Numero punto</b> <i>Numero intero</i> | Numero di punti di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Numero punto</b> <i>Numero intero</i> | Numero di punti generati. |
| <b>Regolazione Smoothness globale</b> <i>Mobile</i> | Applica un offset uniforme al valore di smoothness di tutti i punti.<br>Il valore di smoothness risultante è fissato all&#39;intervallo [0;1]. |
| <b>Proprietà punti</b> |  |
| <b>p# Proprietà</b> <i>Float3</i> | Imposta le proprietà del punto p#.<br>*- Height:* Regola il height del punto in cui un valore inferiore indica una posizione inferiore o più profonda;<br>*- Smoothness:* Sposta l&#39;inizio dell&#39;arrotondamento della spline in corrispondenza di p#, in cui un valore pari a 0 determina una traiettoria rigida e 1 in una completamente arrotondata;<br>*- Thickness:* Regola il thickness della spline in corrispondenza di p#. Thickness viene utilizzato da nodi Spline specifici. |
| <b>Coordinate punti</b> |  |
| <b>p#</b> <i>Float2</i> | Imposta la posizione del punto p# nello spazio della texture. |
| <b>Anteprima</b> |  |
| <b>Mostra etichette</b> <i>Booleano</i> | Per ogni punto, visualizza il nome del punto accanto nell&#39;output &quot;Anteprima&quot;. |
| <b>Dimensioni etichetta</b> <i>Virgola mobile</i> (disponibile quando &#39;Mostra etichette&#39; è impostato su &#39;True&#39;) | Dimensione dell’etichetta per ogni punto nello spazio della texture, dove 0,1 è un decimo della larghezza della texture. |
| <b>Mostra punti</b> <i>Booleano</i> | Visualizza i punti nell&#39;output &quot;Preview&quot;. |
| <b>Dimensioni Punti</b> <i>Virgola mobile</i> (disponibile quando &#39;Mostra punti&#39; è impostato su &#39;True&#39;) | Raggio dei punti nello spazio della texture, dove 0,1 è un decimo della larghezza della texture. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](point-list.resources/PointList-Variant1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](point-list.resources/PointList-Demo1.gif "Esempio di nodo 2")

</td>
</tr>
</table>
