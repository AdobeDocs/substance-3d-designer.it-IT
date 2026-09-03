---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilizzare il nodo Spline Bridge Mapper Scala di grigio per collegare le texture tra due spline con la mappatura in scala di grigio.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura ponti spline in scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# Mappatura ponti spline in scala di grigi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-01.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Mappa un&#39;immagine in scala di grigio su un elenco di spline di input in modo che l&#39;immagine attraversi le spline in ordine.

</td>
</tr>
</table>

>[!TIP]
>
> La mappatura va dalla prima spline dell&#39;elenco all&#39;ultima e attraversa le spline intermedie seguendo rigorosamente l&#39;ordine di queste spline nell&#39;elenco.
> 
> Pertanto, dovete prestare attenzione all’ordine in cui aggiungete le spline in anticipo.

>[!NOTE]
>
> Vedere anche [Colore mappatore ponte spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-col/spline-bridge-mapper-color.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |
| <b>Mappa colori</b> <i>Scala di grigi</i> | Immagine in scala di grigio di input da mappare sulle spline di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Colore</b> <i>Scala di grigi</i> | Risultato della mappatura dell&#39;immagine a colori di input sulle spline, come immagine in scala di grigio. |
| <b>Height</b> <i>Scala di grigi</i> | Height delle spline mappato sulle spline, come immagine in scala di grigio. |
| <b>UV</b> <i>Colore</i> | Gli UV (coordinate) dell’immagine mappata, codificati nei canali rosso (U) e verde (V) di un’immagine a colori. |
| <b>Maschera</b> <i>Scala di grigi</i> | Maschera della mappatura sulle spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Importo segmenti</b> <i>Numero intero</i> | Le spline vengono semplificate in segmenti prima che le coordinate dell&#39;immagine le attraversino. Una maggiore quantità di segmenti determina una mappatura più uniforme lungo le curve. |
| <b>Riduci dilatazione UV</b> <i>Booleano</i> | Regola il metodo utilizzato per interpolare le coordinate dell&#39;immagine da una spline all&#39;altra per ridurre al minimo il allungamento quando la distanza tra le spline è irregolare. |
| <b>Scala UV</b> <i>Float2</i> | Regola la scala delle coordinate dell’immagine. Più alti sono i valori, maggiore sarà la densità delle immagini. |
| <b>Rotazione UV</b> <i>Mobile</i> | Ruota le coordinate dell’immagine attorno al loro centro. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-02.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-03.jpg" alt="SplineBridgeMapperGrayscale-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-04.gif "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-05.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-06.jpg "Esempio di nodo 2")

</td>
</tr>
</table>
