---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spline Bridge per collegare le texture tra due spline e creare connessioni senza interruzioni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ponte spline (2 spline)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---


# Ponte spline (2 spline)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-bridge-2splines-icon.png "Icona nodo")

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

## Connettori di ingresso

<b>Anteprima #1</b> *Scala di grigio* L&#39;anteprima delle spline di input #1 un&#39;immagine in scala di grigio.

<b>Spline Coords #1</b> *Colore* Le coordinate dei punti delle spline di input #1 codificate nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Posizione X\
    <b>G</b> - Posizione Y\
    <b>B</b> - Height\
    <b>A</b> - Dati compressi:\
        * Segno: la spline è chiusa (negativa) o aperta (positiva);\
        * Valore assoluto: Thickness + 1.

<b>#1 dati spline</b> *Colore* I dati aggiuntivi delle spline di input #1 codificati nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Tangenti X\
    <b>G</b> - Tangenti Y\
    <b>B</b> - Non utilizzato\
    <b>A</b> - Non in uso

<b>Quantità spline #1</b> *Numero intero* Numero di spline di input #1.

<b>Anteprima #2</b> *Scala di grigio* L&#39;anteprima delle spline di input #2 un&#39;immagine in scala di grigio.

<b>Spline Coords #2</b> *Colore* Coordinate dei punti di #2 delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Posizione X\
    <b>G</b> - Posizione Y\
    <b>B</b> - Height\
    <b>A</b> - Dati compressi:\
        * Segno: la spline è chiusa (negativa) o aperta (positiva);\
        * Valore assoluto: Thickness + 1.

<b>#2 dati spline</b> *Colore* I dati aggiuntivi delle spline di input #2 codificati nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Tangenti X\
    <b>G</b> - Tangenti Y\
    <b>B</b> - Non utilizzato\
    <b>A</b> - Non in uso

<b>Quantità spline #2</b> *Numero intero* Numero di spline di input #2.

<b>Inizia curva lunghezza tangente</b> *Scala di grigi* (disponibile quando &quot;Tipo spline ponte&quot; è impostato su &quot;Bezier cubico&quot;)Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Questo input viene utilizzato per controllare la lunghezza delle tangenti &quot;out&quot; per il punto iniziale di ciascuna spline generata lungo la spline #1.\
Per creare la curva potete utilizzare un nodo Curva.

<b>Inizia curva di rotazione tangente</b> *Scala di grigi* (disponibile quando &quot;Tipo spline ponte&quot; è impostato su &quot;Bezier cubico&quot;)Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Questo input viene utilizzato per controllare la rotazione delle tangenti &quot;out&quot; per il punto iniziale di ciascuna spline generata lungo la #1. spline\
Il valore in scala di grigio dell’immagine rappresenta un certo numero di giri.\
Per creare la curva potete utilizzare un nodo Curva.

<b>Curva di lunghezza tangente finale</b> *Scala di grigi* (disponibile quando &quot;Tipo spline ponte&quot; è impostato su &quot;Bezier cubico&quot;)Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Questo input viene utilizzato per controllare la lunghezza delle tangenti &quot;in&quot; per il punto finale di ciascuna spline generata lungo la spline #2.\
Per creare la curva potete utilizzare un nodo Curva.

<b>Curva di rotazione tangente finale</b> *Scala di grigi* (disponibile quando &quot;Tipo spline ponte&quot; è impostato su &quot;Bezier cubico&quot;)Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Questo input viene utilizzato per controllare la rotazione delle tangenti &quot;in&quot; per il punto finale di ciascuna spline generata lungo la spline #2.\
Il valore in scala di grigio dell’immagine rappresenta un certo numero di giri.\
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

<b>Quantità spline bridge</b> *Intero* Numero di spline generate lungo la spline #1 alla spline #2.

<b>Tipo spline bridge</b> *Intero* Tipo di spline generato:
* Lineare: una spline retta dall&#39;inizio alla fine;
* Curva Bezier cubica: una spline curva dall&#39;inizio alla fine; la curva è controllata dalla lunghezza e dall&#39;angolo dei punti Inizio e Fine.

<b>Avvia spline #1</b> *Mobile* Sposta la posizione lungo la spline #1 da dove vengono generate le spline. Il valore è la lunghezza normalizzata del #1. spline\
Un valore più elevato determina un numero di spline più stretto.

<b>Avvia spline #2</b> *Mobile* Sposta la posizione lungo la spline #2 da dove vengono generate le spline. Il valore è la lunghezza normalizzata del #2. spline\
Un valore più elevato determina un numero di spline più stretto.

<b>Fine spline #1</b> *Mobile* Sposta la posizione lungo la spline #1 fino al punto in cui vengono generate le spline. Il valore è la lunghezza normalizzata del #1. spline\
Un valore più basso determina un numero di spline uguale più stretto.

<b>Fine spline #1</b> *Mobile* Sposta la posizione lungo la spline #2 fino al punto in cui vengono generate le spline. Il valore è la lunghezza normalizzata del #2. spline\
Un valore più basso determina un numero di spline uguale più stretto.

<b>Spline offset #1</b> *Mobile* Applica uno scostamento al punto iniziale di tutte le spline lungo la spline #1. Il valore è la lunghezza normalizzata del #1. spline\
Le spline che incontrano l&#39;inizio o la fine della spline vengono lasciate lì.

<b>Spline offset #2</b> *Mobile* Applica uno scostamento al punto iniziale di tutte le spline lungo la spline #2. Il valore è la lunghezza normalizzata del #2. spline\
Le spline che incontrano l&#39;inizio o la fine della spline vengono lasciate lì.

<b>Offset casuale inizio</b> *Mobile* Applica uno scostamento casuale al punto iniziale di ogni spline lungo la spline #1. Il valore è la distanza normalizzata tra spline su spline #1.\
Se lasciate a 0, le spline sono equamente distanziate tra i punti di #1 Spline iniziale e #1 Spline finale.

<b>Scostamento fine casuale</b> *Mobile* Applica uno scostamento casuale al punto finale di ogni spline lungo la spline #2. Il valore è la distanza normalizzata tra spline su spline #2.\
Se lasciate a 0, le spline sono equamente distanziate tra i punti di #2 Spline iniziale e #2 Spline finale.

<b>Inizio lunghezza tangente</b> *Float* (disponibile quando &quot;Bridge Splines Type&quot; è impostato su &quot;Cubic Bezier&quot;)Lunghezza della tangente &quot;out&quot; per il punto iniziale sulla spline #1 di tutte le spline generate.

<b>Fine lunghezza tangente</b> *Float* (disponibile quando &quot;Bridge Splines Type&quot; è impostato su &quot;Cubic Bezier&quot;)Lunghezza della tangente &quot;in&quot; per il punto finale sulla spline #2 di tutte le spline generate.

<b>Inizio rotazione tangente</b> *Float* (disponibile quando &quot;Bridge Splines Type&quot; è impostato su &quot;Cubic Bezier&quot;)Rotazione della tangente &quot;out&quot; per il punto iniziale sulla spline #1 di tutte le spline generate.\
Il valore è un numero di giri.

<b>Fine rotazione tangente</b> *Float* (disponibile quando &quot;Bridge Splines Type&quot; è impostato su &quot;Cubic Bezier&quot;)Rotazione della tangente &quot;in&quot; per il punto finale sulla spline #2 di tutte le spline generate.\
Il valore è un numero di giri.

+++Anteprima
<b>Importo segmenti</b> *Numero intero* Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.\
Un valore più alto genera una linea più morbida.

<b>Mostra helper direzione</b> *Booleano* Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima.

<b>Mostra busta Thickness</b> *Booleano*\
Visualizza le linee aggiuntive ai bordi del thickness della spline.

<b>Thickness (px)</b> *Mobile* Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineBridge-2Splines_Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>
