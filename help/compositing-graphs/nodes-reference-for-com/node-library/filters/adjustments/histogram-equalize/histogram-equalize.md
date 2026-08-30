---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: Utilizzate il nodo Equalizza dell’istogramma per ridistribuire l’intensità dei pixel per migliorare il contrasto e la luminosità.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Istogramma equalizza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# Istogramma equalizza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Equalizzazione istogramma: icona](histogram-equalize.resources/histogram_equalize.png "Equalizzazione istogramma: icona"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Equalizza l’istogramma di un’immagine in scala di grigio, regolando efficacemente i valori della scala di grigio per ottenere una distribuzione uniforme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi</i> PRIMARIO | Immagine per la quale deve essere equalizzato l&#39;istogramma. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine del risultato con equalizzazione istogramma applicata. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Risoluzione istogramma</b> *Numero intero* | Larghezza dell’istogramma. Un valore più elevato consente una distribuzione più precisa.   Le risoluzioni disponibili sono, in pixel: 256, 512, 1024, 2048, 4096 |
| <b>Uniformità istogramma</b> *Mobile* | L&#39;istogramma può essere smussato ridistribuendo i valori in scala di grigio nell&#39;immagine per equalizzare la *differenza* tra ciascun valore.   Questo parametro regola l’intensità dell’arrotondamento. |

## Esempi

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Equalizzazione istogramma: esempio 1](histogram-equalize.resources/histogram_equalize_example_3.png "Equalizzazione istogramma: esempio 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Equalizzazione istogramma: esempio 2](histogram-equalize.resources/histogram_equalize_example_5.png "Equalizzazione istogramma: esempio 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Equalizzazione istogramma: esempio 3](histogram-equalize.resources/histogram_equalize_example_6.png "Equalizzazione istogramma: esempio 3"){zoomable="yes"}
