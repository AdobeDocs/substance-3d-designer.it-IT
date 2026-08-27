---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: Usate il nodo Riempimento spline per riempire le aree definite dalle spline chiuse con texture o colori.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Riempimento spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Riempimento spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-fill-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Riempie l&#39;interno delle spline di input di un colore bianco a tinta unita. L&#39;esterno è pieno di nero pieno.

Le spline aperte vengono chiuse con una linea retta dall&#39;inizio alla fine. Le intersezioni in cui la spline si interseca vengono risolte invertendo i lati interni ed esterni delle linee in corrispondenza di tali intersezioni.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Si consiglia di non utilizzare questo nodo su spline che si trovano al di fuori del riquadro [0,1]. Il processo di riempimento non è affidabile in quel caso.

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

<b>Output</b> *Scala di grigi*\
Immagine del risultato del riempimento delle spline di input con un colore bianco piatto su uno sfondo nero piatto.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineFill-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>
