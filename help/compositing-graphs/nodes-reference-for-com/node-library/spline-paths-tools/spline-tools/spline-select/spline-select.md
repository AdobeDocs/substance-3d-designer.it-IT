---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: Utilizza il nodo Selezione spline per selezionare e mascherare aree specifiche in base ai tracciati spline nei grafici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selezione spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---


# Selezione spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-select-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Seleziona le spline nell&#39;elenco di input in base ai criteri specificati e genera un nuovo elenco che include solo le spline selezionate.

Le spline selezionate possono anche essere tagliate.

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

<b>Modalità di selezione</b> *Intero* Metodo di selezione delle spline nell&#39;elenco di input:\
*- Primo*: seleziona la prima spline nell&#39;elenco;\
*- Ultimo*: seleziona l&#39;ultima spline dell&#39;elenco.\
*- Indice*: seleziona la spline con l&#39;indice specificato;\
*- Intervallo*: seleziona le spline che includono gli indici nell&#39;intervallo specificato.

<b>Indice spline</b> *Intero* (disponibile quando &quot;Modalità di selezione&quot; è impostato su &quot;Indice&quot;)Indice della spline da selezionare.

<b>Inizio intervallo</b> *Intero* (disponibile quando &quot;Modalità di selezione&quot; è impostato su &quot;Intervallo&quot;)L&#39;indice più basso nell&#39;intervallo delle spline selezionate.

<b>Fine intervallo</b> *Intero* (disponibile quando &quot;Modalità selezione&quot; è impostato su &quot;Intervallo&quot;)L&#39;indice più alto nell&#39;intervallo delle spline selezionate.<b></b>

<b>Inizio</b> *Mobile* Sposta l&#39;inizio della porzione della spline che deve essere selezionata. In questo modo la spline viene tagliata in modo efficace.\
Il valore rappresenta la lunghezza normalizzata della spline.

<b>Fine</b> *Mobile* Sposta l&#39;estremità della porzione della spline che deve essere selezionata. In questo modo la spline viene tagliata in modo efficace.\
Il valore rappresenta la lunghezza normalizzata della spline.

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
      <img src="../../../../../../assets/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Esempio di nodo 1](../../../../../../assets/SplineSelect-Demo.gif "Esempio di nodo 1")

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
