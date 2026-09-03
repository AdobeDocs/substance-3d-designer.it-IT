---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Utilizzare il nodo Spline Bridge per collegare le texture tra due spline e creare connessioni senza interruzioni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ponte spline (2 spline)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---


# Ponte spline (2 spline)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-bridge-2-splines.resources/spline-bridge-2-splines-01.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera spline da <b>Spline #1</b> a <b>Spline #2</b> lungo queste spline. Le spline generate possono essere lineari (dritte) o cubiche (curve).

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Se i dati forniti agli input <b>Spline #1</b> e <b>Spline #2</b> contengono più di una spline, verrà utilizzata solo l&#39;ultima spline di ogni elenco.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima #1</b> <i>Scala di grigi</i> | L&#39;anteprima delle spline di input #1 un&#39;immagine in scala di grigio. |
| <b>Spline Coords #1</b> <i>Colore</i> | Le coordinate dei punti delle spline di input #1 codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>#1 dati spline</b> <i>Colore</i> | I dati aggiuntivi delle spline di input #1 codificati nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline #1</b> <i>Numero intero</i> | Numero di spline di input #1. |
| <b>Anteprima #2</b> <i>Scala di grigi</i> | L&#39;anteprima delle spline di input #2 un&#39;immagine in scala di grigio. |
| <b>Spline Coords #2</b> <i>Colore</i> | Coordinate dei punti di #2 delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>#2 dati spline</b> <i>Colore</i> | I dati aggiuntivi delle spline di input #2 codificati nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline #2</b> <i>Numero intero</i> | Numero di spline di input #2. |
| <b>Inizia curva lunghezza tangente</b> <i>Scala di grigi</i> (disponibile quando &#39;Tipo spline ponte&#39; è impostato su &#39;Bezier cubico&#39;) | Immagine che descrive una curva utilizzando i valori della prima riga di pixel.<br>Questo input viene utilizzato per controllare la lunghezza delle tangenti &#39;out&#39; per il punto iniziale di ogni spline generata lungo la spline #1.<br>È possibile utilizzare un nodo Curva per creare la curva. |
| <b>Inizia curva di rotazione tangente</b> <i>Scala di grigi</i> (disponibile quando &#39;Tipo spline ponte&#39; è impostato su &#39;Bezier cubico&#39;) | Immagine che descrive una curva utilizzando i valori della prima riga di pixel.<br>Questo input viene utilizzato per controllare la rotazione delle tangenti &quot;out&quot; per il punto iniziale di ogni spline generata lungo la spline #1.<br>Il valore della scala di grigi dell&#39;immagine rappresenta un numero di giri.<br>È possibile utilizzare un nodo Curva per creare la curva. |
| <b>Curva di lunghezza tangente finale</b> <i>Scala di grigi</i> (disponibile quando &#39;Tipo spline ponte&#39; è impostato su &#39;Bezier cubico&#39;) | Immagine che descrive una curva utilizzando i valori della prima riga di pixel.<br>Questo input viene utilizzato per controllare la lunghezza delle tangenti &#39;in&#39; per il punto finale di ogni spline generata lungo la spline #2.<br>È possibile utilizzare un nodo Curva per creare la curva. |
| <b>Curva di rotazione tangente finale</b> <i>Scala di grigi</i> (disponibile quando &#39;Tipo spline ponte&#39; è impostato su &#39;Bezier cubico&#39;) | Immagine che descrive una curva utilizzando i valori della prima riga di pixel.<br>Questo input viene utilizzato per controllare la rotazione delle tangenti &quot;in&quot; per il punto finale di ogni spline generata lungo la spline #2.<br>Il valore in scala di grigio dell&#39;immagine rappresenta un numero di giri.<br>È possibile utilizzare un nodo Curva per creare la curva. |

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
| <b>Quantità spline bridge</b> <i>Numero intero</i> | Numero di spline generate lungo la spline #1 alla spline #2. |
| <b>Tipo spline bridge</b> <i>Numero intero</i> | Tipo di spline generato:<br><br>- Lineare: una spline retta da Inizio a Fine;<br>- Bezier cubico: una spline curva da Inizio a Fine, la curva è controllata dalla lunghezza e dall&#39;angolo dei punti Inizio e Fine. |
| <b>Avvia spline #1</b> <i>Mobile</i> | Sposta la posizione lungo la spline #1 da dove vengono generate le spline. Il valore corrisponde alla lunghezza normalizzata della spline #1.<br>Un valore più elevato determina un maggiore restringimento dello stesso numero di spline. |
| <b>Avvia spline #2</b> <i>Mobile</i> | Sposta la posizione lungo la spline #2 da dove vengono generate le spline. Il valore corrisponde alla lunghezza normalizzata della spline #2.<br>Un valore più elevato determina un maggiore restringimento dello stesso numero di spline. |
| <b>Fine spline #1</b> <i>Mobile</i> | Sposta la posizione lungo la spline #1 fino al punto in cui vengono generate le spline. Il valore corrisponde alla lunghezza normalizzata della spline #1.<br>Un valore inferiore determina un maggiore restringimento dello stesso numero di spline. |
| <b>Fine spline #1</b> <i>Mobile</i> | Sposta la posizione lungo la spline #2 fino al punto in cui vengono generate le spline. Il valore corrisponde alla lunghezza normalizzata della spline #2.<br>Un valore inferiore determina un maggiore restringimento dello stesso numero di spline. |
| <b>Spline offset #1</b> <i>Mobile</i> | Applica uno scostamento al punto iniziale di tutte le spline lungo l&#39;#1. spline Il valore corrisponde alla lunghezza normalizzata della spline #1.<br>Le spline che incontrano l&#39;inizio o la fine della spline vengono lasciate lì. |
| <b>Spline offset #2</b> <i>Mobile</i> | Applica uno scostamento al punto iniziale di tutte le spline lungo l&#39;#2. spline Il valore corrisponde alla lunghezza normalizzata della spline #2.<br>Le spline che incontrano l&#39;inizio o la fine della spline vengono lasciate lì. |
| <b>Offset casuale inizio</b> <i>Mobile</i> | Applica uno scostamento casuale al punto iniziale di ogni spline lungo la spline #1. Il valore rappresenta la distanza normalizzata tra spline sulla spline #1. #1<br>Se lasciate a 0, le spline vengono distribuite uniformemente tra i punti di #1 della spline iniziale e della spline finale. |
| <b>Scostamento fine casuale</b> <i>Mobile</i> | Applica uno scostamento casuale al punto finale di ogni spline lungo la spline #2. Il valore rappresenta la distanza normalizzata tra spline sulla spline #2. #2<br>Se lasciate a 0, le spline vengono distribuite uniformemente tra i punti di #2 della spline iniziale e della spline finale. |
| <b>Inizio lunghezza tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Bridge Splines Type&#39; è impostato su &#39;Cubic Bezier&#39;) | Lunghezza della tangente &#39;out&#39; per il punto iniziale sulla spline #1 di tutte le spline generate. |
| <b>Fine lunghezza tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Bridge Splines Type&#39; è impostato su &#39;Cubic Bezier&#39;) | Lunghezza della tangente &#39;in&#39; per il punto finale sulla spline #2 di tutte le spline generate. |
| <b>Inizio rotazione tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Bridge Splines Type&#39; è impostato su &#39;Cubic Bezier&#39;) | Rotazione della tangente &#39;out&#39; per il punto iniziale sulla spline #1 di tutte le spline generate.<br>Il valore è un numero di giri. |
| <b>Fine rotazione tangente</b> <i>Virgola mobile</i> (disponibile quando &#39;Bridge Splines Type&#39; è impostato su &#39;Cubic Bezier&#39;) | Rotazione della tangente &quot;in&quot; per il punto finale sulla spline #2 di tutte le spline generate.<br>Il valore è un numero di giri. |
| <b>Anteprima</b> |  |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima. Un valore più alto genera una linea più morbida. |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Mostra busta Thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-2-splines.resources/spline-bridge-2-splines-02.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-bridge-2-splines.resources/spline-bridge-2-splines-03.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-bridge-2-splines.resources/spline-bridge-2-splines-04.gif "Esempio di nodo 2")

</td>
</tr>
</table>
