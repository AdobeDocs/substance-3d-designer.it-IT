---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spline Cubic per creare spline cubiche uniformi con quattro punti di controllo per tracciati curvi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Cubic)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---


# Spline (Cubic)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-cubic.resources/spline-cubic-01.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una singola spline tra due punti <b>p1 </b>e <b>p2</b> in posizioni arbitrarie.

La traiettoria della spline è controllata dalla tangente &quot;out&quot; di <b>p1</b> e dalla tangente &quot;in&quot; di <b>p2</b>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Direzione capovolgimento</b> <i>Booleano</i> | Inverte la direzione della spline. |
| <b>Aggiungi spline di input</b> <i>Booleano</i> | Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate. Questo incide anche sulla distribuzione uniforme. |
| <b>Height</b> |  |
| <b>Inizia Height</b> <i>Mobile</i> | Regola il height del punto p1 in cui un valore più basso indica una posizione più bassa o più profonda. Questo influisce sul height della spline a p1. |
| <b>Fine Height</b> <i>Mobile</i> | Regola il height del punto p2 in cui un valore più basso indica una posizione più bassa o più profonda. Questo influisce sul thickness della spline a p2. |
| <b>Height tangente automatico</b> <i>Booleano</i> | Imposta automaticamente il height delle tangenti della spline per l&#39;interpolazione lineare dal Height iniziale al Height finale. |
| <b>p1 Height tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Height tangente automatico&#39; è True) | Regola il height della tangente &quot;out&quot; del punto p1 in cui un valore inferiore indica una posizione più bassa o più profonda. Questo influisce sul height lungo la spline quando si allontana da p1. |
| <b>Height tangente p2</b> <i>Virgola mobile</i> (disponibile quando &#39;Height tangente automatico&#39; è True) | Regola il height della tangente &quot;in&quot; del punto p2 in cui un valore inferiore indica una posizione più bassa o più profonda. Questo influisce sul height lungo la spline quando si allontana da p2. |
| <b>Thickness</b> |  |
| <b>Inizia Thickness</b> <i>Virgola mobile</i> | Regola il thickness del punto p1. Questo influisce sul thickness della spline a p1.<br>Nota: il Thickness viene utilizzato da nodi della spline specifici. |
| <b>Fine Thickness</b> <i>Virgola mobile</i> | Regola il thickness del punto p2. Questo influisce sul thickness della spline a p2.<br>Nota: il Thickness viene utilizzato da nodi della spline specifici. |
| <b>Thickness tangente automatico</b> <i>Booleano</i> | Imposta automaticamente il thickness delle tangenti della spline per l&#39;interpolazione lineare dal Thickness iniziale al Thickness finale.<br>Nota: il Thickness viene utilizzato da nodi della spline specifici. |
| <b>p1 Thickness tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Thickness tangente automatico&#39; è True) | Regola il thickness della tangente &#39;out&#39; del punto p1. Questo influisce sul thickness lungo la spline mentre si allontana da p1.<br>Nota: il Thickness viene utilizzato da nodi della spline specifici. |
| <b>Thickness tangente p2</b> <i>Virgola mobile</i> (disponibile quando &#39;Thickness tangente automatico&#39; è True) | Regola il thickness della tangente &quot;in&quot; del punto p2. Questo influisce sul thickness lungo la spline mentre si allontana da p2.<br>Nota: il Thickness viene utilizzato da nodi della spline specifici. |
| <b>Coordinate punti</b> |  |
| <b>p1</b> <i>Float2</i> | Imposta la posizione del punto p1 nello spazio della texture. |
| <b>p1 Tangente</b> <i>Float2</i> | Imposta la posizione della maniglia tangente &#39;out&#39; del punto p1 nello spazio della texture. |
| <b>p2</b> <i>Float2</i> | Imposta la posizione del punto p2 nello spazio della texture. |
| <b>P2 Tangente</b> <i>Float2</i> | Imposta la posizione della maniglia tangente &quot;in&quot; del punto p2 nello spazio della texture. |
| <b>Anteprima</b> |  |
| <b>Mostra tangenti</b> <i>Booleano</i> | Visualizza la tangente del punto p1 &#39;out&#39; e la tangente del punto p2 &#39;in&#39; nell&#39;output di anteprima. |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima. Un valore più alto genera una linea più morbida. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness in pixel della visualizzazione spline nell&#39;output di anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](spline-cubic.resources/spline-cubic-02.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-cubic.resources/spline-cubic-03.jpg "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 3](spline-cubic.resources/spline-cubic-04.gif "Esempio di nodo 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
