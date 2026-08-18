---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: Utilizzate il nodo Calcolo istogramma per calcolare i dati istogramma dalle texture per l’analisi e l’elaborazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Calcolo istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---


# Calcolo istogramma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Calcolo istogramma: icon](../../../../../../assets/histogram_compute.png "Calcolo istogramma: icon"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Calcola l’istogramma di un’immagine in scala di grigio.

L’istogramma è codificato come una riga di pixel in un’immagine, dove ogni valore di pixel è pari alla *popolazione* del valore di colore corrispondente alla posizione dei pixel sull’asse X.\
Ad esempio, un valore di pixel di 75 a (0,25, 0) significa che ci sono 75 pixel che hanno il valore di colore 0,25 nell’immagine.

</td>
</tr>
</table>

Il nodo genera anche la *funzione di distribuzione cumulativa* (CDF) calcolata per l&#39;immagine.

Gli strumenti personalizzati possono essere creati utilizzando i dati calcolati dal nodo, ad esempio le maschere personalizzate, come illustrato di seguito nella sezione &quot;Esempi&quot;.

>[!IMPORTANT]
>
> Tutti i valori al di fuori dell’intervallo [0,1] vengono bloccati, pertanto l’istogramma potrebbe non essere accurato per le immagini HDR.

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
| <b>Input</b> *Scala di grigi* PRIMARIO | Immagine per la quale deve essere calcolato l&#39;istogramma. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Istogramma</b> *Scala di grigi* | Istogramma calcolato per l&#39;immagine di input, codificato come una riga di pixel in cui ogni valore di pixel corrisponde alla *popolazione* del valore di colore corrispondente alla posizione dei pixel sull&#39;asse X.   Ad esempio, un valore di pixel di 75 a (0,25, 0) significa che ci sono 75 pixel che hanno il valore di colore 0,25 nell’immagine. |
| <b>CDF</b> *Scala di grigi* | Risultato della *funzione di distribuzione cumulativa* (CDF) calcolata per l&#39;immagine, codificata in una riga di pixel in cui ogni pixel è la somma di tutti i valori di pixel alla sua sinistra.   La somma viene quindi *normalizzata* rispetto al numero totale di pixel nell&#39;immagine. |

## Parametri

|  |  |
| --- | --- |
| <b>Risoluzione istogramma</b> *Numero intero* | Larghezza dell’istogramma. Un valore più elevato consente una distribuzione più precisa.   Le risoluzioni disponibili sono, in pixel: 256, 512, 1024, 2048, 4096 |

## Esempi

![Calcolo istogramma: esempio 1](../../../../../../assets/histogram_compute_example_1.jpg "Calcolo istogramma: esempio 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
