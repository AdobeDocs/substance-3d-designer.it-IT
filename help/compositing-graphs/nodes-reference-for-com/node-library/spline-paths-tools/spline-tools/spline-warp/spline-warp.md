---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Usate il nodo Alterazione spline per alterare le texture lungo i tracciati spline per creare pattern curvi e organici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterazione spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# Alterazione spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-warp-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Sposta le spline di input in base alla Mappa intensità di input o alla Mappa vettoriale.

L’intensità dell’effetto di alterazione può essere regolata lungo la spline utilizzando i controlli di attenuazione.

</td>
</tr>
</table>

## Connettori di ingresso

<b>Anteprima</b> *Scala di grigio* Anteprima delle spline di input come immagine in scala di grigio.

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

<b>Mappa intensità</b> *Scala di grigi* (disponibile quando &quot;Usa mappa vettoriale&quot; è impostato su &quot;False&quot;)\
Immagine in scala di grigi di input utilizzata per controllare la direzione e l&#39;intensità dell&#39;effetto di alterazione sulle spline di input.\
Il colore di ciascun pixel nell’immagine specifica un moltiplicatore per spostare i punti della spline lungo la normale (ovvero la direzione perpendicolare alla spline), fino all’intera estensione dell’immagine.\
I valori [0; 1] nell&#39;immagine vengono rimappati all&#39;intervallo [-1; 1] se letti come moltiplicatore: 0 e 1 spostano la spline della stessa distanza ma in direzioni opposte. 0,5 lascia la spline in posizione.

<b>Mappa vettoriale</b> *Scala di grigio* (disponibile quando l’opzione &quot;Usa mappa vettoriale&quot; è impostata su &quot;True&quot;) L’immagine a colori di input utilizzata per controllare la direzione e l’intensità dell’effetto di alterazione sulle spline di input.\
Il colore di ciascun pixel nell’immagine specifica le coordinate vettoriali (X, Y) codificate nei canali rosso (X) e verde (Y). +X è corretto e +Y è inattivo.\
I valori [0; 1] nell’immagine vengono rimappati all’intervallo [-1; 1] quando letti come coordinate vettoriali: 0 rosso sposta i punti a sinistra e 0 verde sposta i punti verso l’alto. 0,5 rosso e verde lasciano la spline in posizione.

<b>Curva di attenuazione</b> *Scala di grigi* Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Quando il parametro Usa curva di attenuazione è impostato su True, questo input viene utilizzato per controllare l&#39;attenuazione dell&#39;effetto di alterazione vicino all&#39;inizio e alla fine della spline.\
La curva fornisce un profilo per l&#39;attenuazione, in cui il primo pixel della riga è l&#39;intensità dell&#39;effetto di alterazione all&#39;inizio della spline e l&#39;ultimo è l&#39;intensità alla fine. Il valore della scala di grigi è l’intensità.\
Per creare la curva potete utilizzare un nodo Curva.

## Connettori di uscita

<b>Anteprima</b> *Scala di grigi* Anteprima delle spline di output come immagine in scala di grigi.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Posizione X\
<b>G</b> - Posizione Y\
<b>B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Tangenti X\
<b>G</b> - Tangenti Y\
<b>B</b> - Non utilizzato\
<b>A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di output.

## Parametri

<b>Intensità alterazione</b> *Fluttuazione* L&#39;intensità di spostamento delle spline.

<b>Centro alterazione</b> *Float* Specifica il valore di Mappa intensità che corrisponde a lasciare in posizione le spline.\
Il valore 0 o 1 indica che le spline possono essere spostate solo su un lato.

<b>Modalità campionamento</b> *Intero* Metodo di mappatura dei valori nella mappa di intensità o nella mappa vettoriale sulle spline:\
*- Spazio texture*: i valori vengono applicati alle spline in cui si troverebbero se fossero inseriti in una texture utilizzando le coordinate UV della texture. In questo modo si applica effettivamente il valore alle spline &quot;in posizione&quot;;\
*- Orizzontale lungo la spline*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;\
*- Ora. lungo spline (rand. offset X)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coords spline), con uno scostamento orizzontale casuale nella mappa di scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);\
*- Ora. lungo spline (rand. offset Y)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline).

<b>Usa mappa vettoriale</b> *Booleano* Sostituisce il metodo di spostamento delle spline con l&#39;input di una mappa vettoriale per specificare la direzione dello spostamento.\
Il colore di ciascun pixel nell’immagine specifica le coordinate vettoriali (X, Y) codificate nei canali rosso (X) e verde (Y). +X è corretto e +Y è inattivo.\
I valori [0; 1] nell’immagine vengono rimappati all’intervallo [-1; 1] quando letti come coordinate vettoriali: 0 rosso sposta i punti a sinistra e 0 verde sposta i punti verso l’alto. 0,5 rosso e verde lasciano la spline in posizione.

<b>Usa curva di attenuazione</b> *Booleano* Consente di controllare l&#39;intensità dell&#39;effetto di alterazione lungo una spline utilizzando una curva codificata nell&#39;immagine di input Curva di attenuazione.<b></b>

<b>Porzioni mappa intensità</b> *Mobile* (disponibile quando &quot;Modalità di campionamento&quot; non è impostato su &quot;Spazio texture&quot;) Regola la suddivisione in porzioni della mappa di intensità quando questa viene mappata direttamente alle coordinate della spline (vedere l&#39;input Coord spline).<b></b>

<b>Avvia attenuazione</b> *Mobile* (disponibile quando &quot;Usa curva di attenuazione&quot; è impostato su &quot;False&quot;)Un moltiplicatore per l&#39;attenuazione dell&#39;effetto di alterazione vicino all&#39;inizio della spline.\
Il valore 1 indica che non viene applicata alcuna alterazione all&#39;inizio della spline.

<b>Termina attenuazione</b> *Mobile* (disponibile quando &quot;Usa curva di attenuazione&quot; è impostato su &quot;False&quot;)Un moltiplicatore per l&#39;attenuazione dell&#39;effetto di alterazione vicino alla fine della spline.\
Il valore 1 indica che non viene applicata alcuna alterazione alla fine della spline.<b></b>

<b>Ricalcola tangenti</b> *Booleano* Se è True, le tangenti di una spline vengono ricalcolate dopo l&#39;applicazione dell&#39;effetto di alterazione.\
In questo modo le tangenti della spline rimangono coerenti con la traiettoria quando vengono utilizzate in nodi quali Dispersione su spline o Spline Flow Mapper.

+++Anteprima
<b>Importo segmenti</b> *Numero intero* Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.\
Un valore più alto genera una linea più morbida.

<b>Mostra helper direzione</b> *Booleano* Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima.

<b>Mostra busta Thickness</b> *Booleano*\
Visualizza le linee aggiuntive ai bordi del thickness della spline.

<b>Thickness (px)</b> *Mobile* Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima.

<b>Intensità anteprima in background</b> *Mobile*\
Valore moltiplicato per l’immagine di input Anteprima sfondo.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Esempio di nodo 1](../../../../../../assets/SplineWarp-Demo.gif "Esempio di nodo 1")

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
