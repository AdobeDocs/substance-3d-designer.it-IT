---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: Utilizzare il nodo Trasformazione 2D spline per trasformare le spline con le operazioni di traslazione, rotazione e ridimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline 2D Transform
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---


# Spline 2D Transform

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-2d-transform.resources/spline-2d-transform-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica una trasformazione globale a tutte le spline di input, inclusa l&#39;inversione della direzione.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |

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
| <b>Direzione capovolgimento</b> <i>Booleano</i> | Inverte la direzione della spline. |
| <b>Matrice di trasformazione</b> <i>Float4</i> | Matrice di trasformazione applicata alle spline.<br>Sono disponibili tre modalità di modifica dei parametri della matrice:<br><br>- <i>Gizmo di trasformazione</i>: modificare le maniglie del gizmo visualizzato nel vista 2D quando è selezionato il nodo di Trasforma 2D della spline;<br>- <i>Rotazione/Allungamento</i>: controllare singolarmente la rotazione e il allungamento delle spline. Si noti che i valori vengono sempre applicati relativamente alla trasformazione corrente. Ad esempio, se si applica due volte la larghezza del 50% si ottiene il 25% della larghezza;<br>- <i>Valori matrice</i>: fare clic sul pulsante Modifica valori matrice per immettere direttamente i valori numerici non elaborati della matrice. |
| <b>Scostamento</b> <i>Float2</i> | Applica uno scostamento di posizione alle spline in X (orizzontale) e Y (verticale). |
| <b>Anteprima</b> |  |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Mostra busta Thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima. Un valore più alto genera una linea più morbida. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant2-After.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-Before.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/Spline2DTransform-Variant1-After.jpg" alt="Spline2DTransform-Variant1-After">
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

![Esempio di nodo 1](spline-2d-transform.resources/Spline2DTransform-Demo1.gif "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
