---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Utilizzate il nodo Arrotondamento curvatura (Curvature Smooth) per generare mappe di curvatura omogenee dalle mappe di height per l'estrazione dei dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# Curvatura uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo arrotondato curvatura](curvature-smooth.resources/CurvatureSmooth.png "Icona nodo arrotondato curvatura"){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Calcola la curvatura di una superficie descritta da una mappa normale.

Una mappa di curvatura rappresenta le aree concave e convesse di una superficie.\
Le aree piatte sono grigie al 50%. Le aree convesse sono più luminose, mentre quelle concave più scure.

</td>
</tr>
</table>

Anche le aree concave e convesse vengono suddivise nelle rispettive uscite, per una più semplice selezione o mascheratura delle aree in base a tali caratteristiche.

>[!TIP]
>
> Per una versione più nitida, osserva [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) oppure [Sobel curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) se hai bisogno di più opzioni.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Normale</b> <i>Colore</i> <b>PRIMARIO</b> | La mappa normale che descrive la superficie da calcolare per la curvatura. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Scala di grigi</i> | Mappa di curvatura calcolata a partire dalla mappa normale di input.   Le aree piatte sono grigie al 50%. Le aree convesse sono più luminose, mentre quelle concave più scure. |
| <b>Convessità</b> <i>Scala di grigi</i> | La mappa di convessità calcolata a partire dalla mappa normale di input.   Più convessa è un&#39;area, più luminosa è nella mappa.  Le aree piatte o concave sono nere. |
| <b>Concavità</b> <i>Scala di grigi</i> | Mappa di concavità calcolata a partire dalla mappa normale di input.   Più concava è un&#39;area, più luminosa è nella mappa.  Le aree piatte o convesse sono nere. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Formato normale</b> *Numero intero* | Formato della mappa normale di input. Inverte efficacemente il canale del verde.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> l&#39;asse Y punta in alto</li> <li data-preserve-html="true"><b style="">OpenGL:</b> l&#39;asse Y punta in basso</li> </ul> |

## Esempi

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_before.jpg" alt="curvature_smog_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_after.jpg" alt="curvature_smog_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura uniforme: Esempio 2](curvature-smooth.resources/curvature_smooth_example_2.jpg "Curvatura uniforme: Esempio 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura uniforme: Esempio 3](curvature-smooth.resources/curvature_smooth_example_3.jpg "Curvatura uniforme: Esempio 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_before.jpg" alt="curvature_smog_example_4_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_after.jpg" alt="curvature_smog_example_4_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura uniforme: Esempio 4](curvature-smooth.resources/curvature_smooth_example_5.jpg "Curvatura uniforme: Esempio 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura uniforme: Esempio 5](curvature-smooth.resources/curvature_smooth_example_6.jpg "Curvatura uniforme: Esempio 5"){zoomable="yes"}

</td>
</tr>
</table>
