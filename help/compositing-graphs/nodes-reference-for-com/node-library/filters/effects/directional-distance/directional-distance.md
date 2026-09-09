---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/directional-distance.html"
breadcrumb-title: ''
description: Utilizzare il nodo Distanza direzionale per calcolare i campi distanza in direzioni specifiche per gli effetti procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Directional distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distanza direzionale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Distanza direzionale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Anisotropica in scala di grigio Kuwahara](directional-distance.resources/directional_distance.png "Icona anisotropica in scala di grigio Kuwahara"){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Traccia una sfumatura di distanza dai bordi di una maschera in una direzione specificata.

Le sfumature sovrapposte vengono ordinate in base alla distanza normalizzata invertita, in modo da tracciare la distanza dal bordo più vicino.

La distanza della sfumatura può essere regolata dinamicamente lungo il bordo utilizzando una mappa di distanza.

</td>
</tr>
</table>

>[!TIP]
>
> Il nodo [Smusso uniforme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md) offre funzionalità simili, in cui la dilatazione viene eseguita in tutte le direzioni.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi</i> PRIMARIO | Immagine da cui estrarre la maschera.   Tutti i valori superiori a 0,5 sono bianchi nella maschera. |
| <b>Mappa di distanza</b> <i>Scala di grigi</i> | Input facoltativo utilizzato quando il valore del parametro &#39;Moltiplicatore Mappa di distanza&#39; è maggiore di 0.   Viene utilizzato per regolare la distanza di smussatura/dilatazione lungo i bordi della maschera, dove un valore più scuro determina una distanza più breve. |
| <b>Mappa angolo</b> <i>Scala di grigi</i> | Input facoltativo utilizzato quando il valore del parametro &#39;Angle Map Multiplier&#39; è maggiore di 0.   Viene utilizzato per regolare la direzione della sfumatura distanza aggiungendo il suo valore all’angolo di direzione, in numero di giri.   Il parametro &#39;Scostamento mappa angolo&#39; consente di rimappare i valori specificando il valore 0. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine del risultato in base alla modalità di output selezionata. |
| <b>UV</b> <i>Colore</i> | Una mappa UV in cui gli UV sono dilatati dai bordi della maschera lungo la direzione specificata.   Questo può essere collegato a un nodo [UV Mapper](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) per mappare qualsiasi altra immagine utilizzando questi UV dilatati. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità output</b> *Numero intero* | Metodo per disegnare la sfumatura di distanza dai bordi della maschera:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Distanza normalizzata invertita:</b> una sfumatura da 1 a 0 dove 0 viene raggiunto alla &#39;Distanza massima&#39;, moltiplicata per la &#39;Mappa di distanza&#39; se collegata</li> <li data-preserve-html="true"><b>Distanza:</b> una sfumatura con valori di distanza non elaborati dal bordo della maschera, dove 1 rappresenta la lunghezza del lato più corto dell&#39;immagine di input</li> </ul> |
| <b>Distanza massima</b> *Mobile* | La distanza percorsa dalla sfumatura di distanza, nello spazio dell&#39;immagine normalizzato in cui 1 è la lunghezza del lato più corto dell&#39;immagine di input. |
| <b>Angolo</b> *Mobile* | La direzione della sfumatura distanza in numero di giri, dove 0 è orizzontale e a destra, ovvero un vettore (1,0). |
| <b>Moltiplicatore Mappa di distanza</b> *Mobile* | Regola l’impatto della &quot;Mappa di distanza&quot; sulla &quot;Distanza massima&quot;.   Nota: questo parametro non ha effetto quando l&#39;input &#39;Mappa di distanza&#39; non è connesso. |
| <b>Moltiplicatore mappa angolare</b> *Mobile* | Regola l’impatto della &quot;Mappa angolo&quot; sull’angolo. |
| <b>Offset mappa angolo</b> *Mobile* | Modifica i valori della &#39;Mappa angolo&#39; specificando il valore della mappa che deve essere 0.   Ad esempio, uno scostamento di 0,5 significa che un valore di 0,75 è pari a 0,25 giri, mentre un valore di 0,3 è pari a -0,2 giri. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_before.jpg" alt="directional_distance_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_after.jpg" alt="directional_distance_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_before.jpg" alt="directional_distance_example_3_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_after.jpg" alt="directional_distance_example_3_after">
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

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_before.jpg" alt="directional_distance_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_after.jpg" alt="directional_distance_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_before.jpg" alt="directional_distance_example_5_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_after.jpg" alt="directional_distance_example_5_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_before.jpg" alt="directional_distance_example_4_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_after.jpg" alt="directional_distance_example_4_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
