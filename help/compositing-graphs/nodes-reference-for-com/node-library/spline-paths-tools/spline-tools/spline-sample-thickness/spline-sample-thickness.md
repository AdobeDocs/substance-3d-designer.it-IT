---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: Utilizzate il nodo Thickness campione spline per campionare i valori dei thickness lungo le spline per ottenere effetti procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Thickness di campionamento spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---


# Thickness di campionamento spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-sample-thickness-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Modifica il thickness delle spline di input mappando su di esse una mappa del Thickness di input.

L’effetto della mappa del height mappato può essere regolato modificandone il metodo di fusione e l’opacità.

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

<b>Mappa Thickness</b> *Scala di grigio* Immagine in scala di grigio di input utilizzata per modificare il thickness della spline di input.

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

<b>Modalità campionamento</b> *Intero* Metodo di mappatura dei valori nella mappa di Thickness alle spline:\
*- Spazio texture*: i valori vengono applicati alle spline in cui si troverebbero se fossero inseriti in una texture utilizzando le coordinate UV della texture. In questo modo si applica effettivamente il valore alle spline &quot;in posizione&quot;;\
*- Orizzontale lungo la spline*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;\
*- Ora. lungo spline (rand. offset X)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coords spline), con uno scostamento orizzontale casuale nella mappa di scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);\
*- Ora. lungo spline (rand. offset Y)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline).

<b>Opacità</b> *Fluttuazione* Moltiplicatore per l&#39;intensità del contributo dell&#39;input Mappa Thickness al thickness della spline.<b></b>

<b>Metodo fusione</b> *Intero* Metodo di fusione dei dati della mappa del Thickness con i <span id="_Hlk135820484"></span>thickness della spline di input:\
*- Copia*: sovrascrivere il thickness della spline con i valori Height della mappa;\
*- Aggiungi*: aggiungi i valori della mappa dei Thickness al thickness della spline;\
*- Sottrai*: sottrai i valori della mappa dei Thickness al thickness della spline;\
*- Moltiplica*: moltiplica i valori della mappa dei Thickness sul thickness della spline.

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
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-Before.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant1-After.jpg" alt="SplineSampleThickness-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-Before.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSampleThickness-Variant2-After.jpg" alt="SplineSampleThickness-Variant2-After">
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

![Esempio di nodo 1](../../../../../../assets/SplineSampleThickness-Variant1-After1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineSampleThickness-Demo.gif "Esempio di nodo 2")

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
