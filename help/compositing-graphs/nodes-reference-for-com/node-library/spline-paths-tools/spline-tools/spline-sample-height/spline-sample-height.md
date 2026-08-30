---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-height.html"
breadcrumb-title: ''
description: Utilizzate il nodo Height campione spline per campionare i valori dei height lungo le spline per ottenere effetti di spostamento procedurale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height di campionamento spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Height di campionamento spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-sample-height.resources/spline-sample-height-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Modifica il height delle spline di input mappando su di esse una mappa del Height di input.

L’effetto della mappa del height mappato può essere regolato modificandone il metodo di fusione e l’opacità.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |
| <b>Mappa Height</b> <i>Scala di grigi</i> | Immagine in scala di grigio di input utilizzata per modificare il height della spline di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità campionamento</b> <i>Numero intero</i> | Metodo di mappatura dei valori nella mappa altezza alle spline:<br>- <i>spazio Texture</i>: i valori vengono applicati alle spline in cui si troverebbero se inseriti in una texture utilizzando le coordinate UV della texture. Questo applica efficacemente il valore alle spline &quot;in posizione&quot;;<br>- <i>Orizzontale lungo la spline</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;<br>- <i>Hor. lungo spline (rand. offset X)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento orizzontale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline);<br>- <i>Hor. lungo spline (rand. offset Y)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline). |
| <b>Opacità</b> <i>Mobile</i> | Un moltiplicatore per l’intensità del contributo dell’input della mappa dell’altezza al height della spline. |
| <b>Metodo fusione</b> <i>Numero intero</i> | Metodo di fusione dei dati della mappa dell&#39;altezza con il height della spline di input:<br>- <i>Copia</i>: ignorare il height della spline con i valori della mappa dell&#39;altezza;<br>- <i>Aggiungi</i>: aggiungere i valori della mappa dell&#39;altezza al height della spline;<br>- <i>Sottrai</i>: Sottrai dei valori della mappa dell&#39;altezza al height della spline;<br>- <i>Moltiplica</i>: moltiplicare i valori della mappa dell&#39;altezza rispetto al height della spline. |
| <b>Anteprima</b> |  |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.<br>Un valore più elevato determina una linea più fluida. |
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
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-After.jpg" alt="SplineSampleHeight-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-After3.jpg" alt="SplineSampleHeight-Variant1-After3">
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

![Esempio di nodo 1](spline-sample-height.resources/SplineSampleHeight-Variant1-After4.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-sample-height.resources/SplineSampleHeight-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>
