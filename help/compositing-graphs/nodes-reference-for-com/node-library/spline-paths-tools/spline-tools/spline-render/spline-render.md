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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---


# Rendering spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

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

## Connettori di ingresso

<b>Sfondo </b>*Scala di grigi* Immagine in scala di grigi su cui devono essere disegnate spline.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:\
<b> R</b> - Posizione X\
<b> G</b> - Posizione Y\
<b> B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.\
<b> R</b> - Tangenti X\
<b> G</b> - Tangenti Y\
<b> B</b> - Non in uso\
<b> A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di input.

## Connettori di uscita

<b>Output</b> *Scala di grigi*\
Immagine del risultato del disegno delle spline di input sopra lo sfondo.

## Parametri

<b>Modalità</b> *Intero* Metodo di selezione delle spline da disegnare:
* *Disegna elenco spline*: disegna tutte le spline nell&#39;elenco di input;
* *Disegna spline singola*: disegna solo la spline specificata dall&#39;elenco di input;
* *Disegna intervallo spline*: disegna solo le spline dell&#39;intervallo specificato dall&#39;elenco di input.

<b>Disegna indice spline</b> *Intero* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna spline singola&quot;)Indice della spline da disegnare.

<b>Disegna intervallo spline</b> *Intero2* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna intervallo spline&quot;)Intervallo di indici per le spline da disegnare.

<b>Mostra helper direzione</b> *Booleano* Per ogni spline, disegna un punto all&#39;inizio della spline e una freccia alla sua fine.

<b>Importo segmenti</b> *Intero* Regola il numero di segmenti disegnati lungo le spline.\
Un valore più alto genera linee più morbide.

<b>Quantità spline busta</b> *Numero intero*\
Numero di segmenti duplicati che devono essere disegnati lungo il thickness di ciascuna spline.

<b>Inizio</b> *Mobile* Sposta l&#39;inizio della porzione della spline che deve essere disegnata.\
Il valore rappresenta la lunghezza normalizzata della spline.

<b>Fine</b> *Mobile* Sposta l&#39;estremità della spline che deve essere disegnata.\
Il valore rappresenta la lunghezza normalizzata della spline.

<b>Modalità dimensioni Thickness</b> *Intero* Metodo di calcolo del thickness dei segmenti disegnati:
* *Immagine*: il valore viene normalizzato nello spazio della texture, dove 1 indica la larghezza completa dell&#39;immagine. il thickness è relativo alla risoluzione della texture;
* *Pixel*: il valore è un numero assoluto di pixel nella texture, dove 1 è un pixel pieno. Il thickness è separato dalla risoluzione della texture.

<b>Thickness (immagine)</b> *Mobile* (disponibile quando la modalità &quot;Dimensioni Thickness&quot; è impostata su Immagine)Il thickness dei segmenti disegnati si normalizza nello spazio della texture, dove 1 rappresenta la larghezza completa dell&#39;immagine.

<b>Thickness (px)</b> *Mobile* (disponibile quando l’opzione &quot;Modalità dimensioni Thickness&quot; è impostata su Pixel) Il thickness dei segmenti disegnati come numero assoluto di pixel nella texture, dove 1 corrisponde a un pixel intero.

<b>Abilita giunti</b> *Booleano* Riempie gli spazi tra i singoli segmenti disegnati lungo le spline, utilizzando i dischi.

<b>Correzione non quadrata </b>*Booleano* Regola le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

+++Colore
<b>Intensità sfondo</b> *Mobile* Valore moltiplicato per l&#39;immagine di input dello sfondo.

<b>Stile spline</b> *Intero* Metodo utilizzato per colorare le spline:
* *Solido*: i segmenti vengono disegnati utilizzando un valore in scala di grigio uniforme;
* *Sfumatura*: una sfumatura dal nero al bianco viene applicata lungo ogni stringa di segmenti dall’inizio alla fine;
* *Height*: il height delle spline viene utilizzato come valore in scala di grigio per disegnare i segmenti.

<b>Colore spline</b> *Mobile* Valore di scala di grigi uniforme utilizzato per disegnare i segmenti.\
Quando è selezionato uno stile di spline diverso da &quot;Tinta unita&quot;, questo colore viene moltiplicato per il colore di stile.

<b>Luminanza casuale</b> *Mobile* Per ogni stringa di segmenti non tagliati in una spline, applica uno scostamento casuale nell&#39;intervallo specificato al valore in scala di grigio utilizzato per disegnare la stringa.

<b>Metodo fusione</b> *Intero* Metodo per fondere i colori dello sfondo e i segmenti sovrapposti disegnati lungo le spline:
* *Max*: viene utilizzato il valore più chiaro;
* *Aggiungi*: i valori vengono aggiunti insieme.

+++

+++Segmenti casuali
<b>Inizio segmenti casuali</b> *Mobile* Regola la probabilità che la stringa di segmenti più vicina all&#39;inizio della spline venga tagliata.

<b>Fine Segmenti Casuali</b> *Mobile* Regola la probabilità che la stringa di segmenti più vicina all&#39;estremità della spline venga tagliata.

<b>Scostamento casuale</b> *Mobile* Imposta la quantità massima di spostamento applicata a ciascun segmento tagliato lungo la normale.\
Questo parametro non ha effetto quando Inizio e Fine sono entrambi impostati su 0.

<b>Scostamento casuale al centro</b> *Mobile* Sposta il centro dello spostamento casuale applicato a ciascun segmento tagliato lungo la sua normale.

+++

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

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
