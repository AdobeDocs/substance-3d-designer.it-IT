---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: Utilizzare il nodo Elenco unione spline per unire più spline in un unico elenco spline per operazioni combinate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elenco unione spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 1%

---


# Elenco unione spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-merge-list-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Unisce tutte le spline dell&#39;elenco di input in un&#39;unica spline.

</td>
</tr>
</table>

## Connettori di ingresso

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

<b>Anteprima</b> *Scala di grigio* Anteprima delle spline unite come immagine in scala di grigio.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline unite codificate nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Posizione X\
    <b>G</b> - Posizione Y\
    <b>B</b> - Height\
    <b>A</b> - Dati compressi:\
        * Segno: la spline è chiusa (negativa) o aperta (positiva);\
        * Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline unite codificate nei canali RGBA di un&#39;immagine a colori.\
    <b>R</b> - Tangenti X\
    <b>G</b> - Tangenti Y\
    <b>B</b> - Non utilizzato\
    <b>A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline unite.

## Parametri

<b>Soglia distanza spline chiusa</b> *Mobile* La distanza nello spazio della texture al di sotto della quale due estremità di una stessa spline vengono elaborate come un singolo punto che chiude la spline.\
In questo modo si evitano sovrapposizioni durante la dispersione delle forme o la mappatura delle immagini lungo le spline.

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
      <img src="../../../../../../assets/SplineMergeList-Variant2-Before.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant2-After.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-Before.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMergeList-Variant1-After.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Demo sui nodi](../../../../../../assets/SplineMergeList-Demo.gif "Demo sui nodi")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
