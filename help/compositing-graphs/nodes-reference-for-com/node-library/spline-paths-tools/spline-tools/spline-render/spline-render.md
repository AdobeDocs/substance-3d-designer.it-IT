---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rendering spline per eseguire il rendering delle spline come texture con metodi personalizzabili di larghezza, colore e fusione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Rendering spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-render-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disegna stringhe di segmenti lungo le <b>spline</b> di input sullo <b>sfondo</b>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Sfondo</b> <i>Scala di grigi</i> | Immagine in scala di grigio su cui devono essere disegnate spline. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine del risultato del disegno delle spline di input sopra lo sfondo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità</b> <i>Numero intero</i> | Metodo di selezione delle spline da disegnare:<br>- <i>Disegna elenco spline</i>: disegna tutte le spline nell&#39;elenco di input;<br>- <i>Disegna spline singola</i>: disegna solo la spline specificata dall&#39;elenco di input;<br>- <i>Disegna intervallo spline</i>: disegna solo le spline dell&#39;intervallo specificato dall&#39;elenco di input. |
| <b>Disegna indice spline</b> <i>Numero intero</i> | (Disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna singola spline&quot;) Indice della spline da disegnare. |
| <b>Disegna intervallo spline</b> <i>Intero2</i> | (Disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna intervallo spline&quot;) Intervallo di indici per le spline da disegnare. |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Per ogni spline, traccia un punto all&#39;inizio della spline e una freccia alla sua fine. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti disegnati lungo le spline.<br>Un valore più elevato determina linee più uniformi. |
| <b>Quantità spline busta</b> <i>Numero intero</i> | Numero di segmenti duplicati che devono essere disegnati lungo il thickness di ciascuna spline. |
| <b>Inizio</b> <i>Mobile</i> | Sposta l&#39;inizio della porzione della spline da disegnare.<br>Il valore rappresenta la lunghezza normalizzata della spline. |
| <b>Fine</b> <i>Mobile</i> | Sposta l&#39;estremità della porzione della spline da disegnare.<br>Il valore rappresenta la lunghezza normalizzata della spline. |
| <b>Modalità dimensioni Thickness</b> <i>Numero intero</i> | Metodo di calcolo del thickness dei segmenti disegnati:<br>- <i>Immagine</i>: il valore viene normalizzato nello spazio della texture, dove 1 rappresenta la larghezza completa dell&#39;immagine. Il thickness è relativo alla risoluzione della texture;<br>- <i>Pixel</i>: il valore è un numero assoluto di pixel nella texture, dove 1 è un pixel pieno. Il thickness è separato dalla risoluzione della texture. |
| <b>Thickness (immagine)</b> <i>Mobile</i> | (disponibile quando la modalità &quot;Dimensioni Thickness&quot; è impostata su Immagine) Il thickness dei segmenti disegnati normalizzati nello spazio della texture, dove 1 rappresenta l&#39;intera larghezza dell&#39;immagine. |
| <b>Thickness (px)</b> <i>Mobile</i> | (disponibile quando la modalità &quot;Dimensioni Thickness&quot; è impostata su Pixel) Il thickness dei segmenti disegnati come numero assoluto di pixel nella texture, dove 1 corrisponde a un pixel intero. |
| <b>Abilita giunti</b> <i>Booleano</i> | Riempie gli spazi tra i singoli segmenti disegnati lungo le spline utilizzando i dischi. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline in risoluzioni non quadrate.<br>Questo influisce anche sulla distribuzione uniforme. |
| <b>Colore</b> |  |
| <b>Intensità sfondo</b> <i>Mobile</i> | Valore moltiplicato per l’immagine di input Sfondo. |
| <b>Stile spline</b> <i>Numero intero</i> | Metodo utilizzato per colorare le spline:<br>- <i>Tinta unita</i>: i segmenti vengono disegnati utilizzando un valore in scala di grigio uniforme;<br>- <i>Sfumatura</i>: viene applicata una sfumatura dal nero al bianco lungo ogni stringa di segmenti dall&#39;inizio alla fine;<br>- <i>Height</i>: il height delle spline viene utilizzato come valore in scala di grigio per disegnare i segmenti. |
| <b>Colore spline</b> <i>Mobile</i> | Valore di scala di grigi uniforme utilizzato per disegnare i segmenti.<br>Quando è selezionato uno stile di spline diverso da &quot;Tinta unita&quot;, questo colore viene moltiplicato per il colore di stile. |
| <b>Luminanza casuale</b> <i>Mobile</i> | Per ogni stringa di segmenti non tagliati in una spline, applica uno scostamento casuale nell&#39;intervallo specificato al valore in scala di grigio utilizzato per disegnare la stringa. |
| <b>Metodo fusione</b> <i>Numero intero</i> | Metodo di fusione dei colori dello sfondo e dei segmenti sovrapposti disegnati lungo le spline:<br>- <i>Max</i>: viene utilizzato il valore più chiaro;<br>- <i>Aggiungi</i>: i valori vengono sommati. |
| <b>Segmenti casuali</b> |  |
| <b>Inizio segmenti casuali</b> <i>Mobile</i> | Regola la probabilità di taglio della stringa di segmenti più vicina all&#39;inizio della spline. |
| <b>Fine Segmenti Casuali</b> <i>Mobile</i> | Regola la probabilità di taglio della stringa di segmenti più vicina all&#39;estremità della spline. |
| <b>Scostamento casuale</b> <i>Mobile</i> | Imposta la quantità massima di spostamento applicata a ciascun segmento di taglio lungo la normale.<br>Questo parametro non ha effetto quando Start e End sono entrambi impostati su 0. |
| <b>Scostamento casuale al centro</b> <i>Mobile</i> | Sposta il centro dello spostamento casuale applicato a ciascun segmento di taglio lungo la sua normale. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/SplineRender-Demo.gif "Esempio di nodo 1")

</td>
</tr>
</table>
