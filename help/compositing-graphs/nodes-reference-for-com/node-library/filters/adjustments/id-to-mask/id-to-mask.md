---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: Utilizza il nodo ID da mascherare in scala di grigio per convertire i valori della mappa ID in maschere in scala di grigio per la selezione del materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da ID a maschera in scala di grigio
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# Da ID a maschera in scala di grigio

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona ID per maschera in scala di grigio](../../../../../../assets/IDToMask.png "Icona ID per maschera in scala di grigio"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Crea una maschera a partire da una mappa ID in cui i pixel con i valori di pixel selezionati sono bianchi.

Una mappa ID è un’immagine in cui i pixel che fanno parte di un intero (ad esempio, una forma) mantengono tutti lo stesso valore di identificazione univoco. In questo caso, il valore è un numero intero.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Parametri

</td>
</tr>
</table>

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>ID</b> *Scala di grigi* PRIMARIO | Mapping ID di input da cui estrarre una maschera. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | Maschera binaria estratta dalla mappa ID di input. |

## Parametri

|  |  |
| --- | --- |
| <b>Modalità di selezione</b> *Numero intero* | Metodo di selezione dei valori dei pixel nella mappa ID che devono essere bianchi nella maschera:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Solo:</b> selezionare un valore di pixel singolo</li> <li data-preserve-html="true"><b>Intervallo:</b> Selezionare un intervallo di valori di pixel</li> </ul> |
| <b>ID intero</b> *Intero* *Disponibile quando &#39;Modalità selezione&#39; è impostato su &#39;Solo&#39;* | Il valore in pixel nella mappa ID che dovrebbe essere bianco nella maschera di output. |
| <b>Intervallo ID</b> *Intero2* *Disponibile quando &#39;Modalità selezione&#39; è impostato su &#39;Intervallo&#39;* | Intervallo di valori dei pixel nella mappa ID, dall’inizio alla fine, che dovrebbe essere bianco nella maschera di output. |

## Esempi

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ID da mascherare: Esempio 2](../../../../../../assets/id_to_mask_example_2.gif "ID da mascherare: Esempio 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ID da mascherare: Esempio 3](../../../../../../assets/id_to_mask_example_3.png "ID da mascherare: Esempio 3"){zoomable="yes"}

</td>
</tr>
</table>
