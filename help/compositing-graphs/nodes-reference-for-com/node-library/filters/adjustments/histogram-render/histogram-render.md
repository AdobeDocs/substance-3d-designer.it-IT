---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rendering istogramma per visualizzare i dati dell’istogramma come texture per l’analisi e il debug.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Rendering istogramma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Anisotropica in scala di grigio Kuwahara](../../../../../../assets/histogram_render.png "Icona anisotropica in scala di grigio Kuwahara"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disegna l’istogramma di un’immagine in scala di grigio.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi</i> PRIMARIO | Immagine per la quale deve essere disegnato l&#39;istogramma. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Visualizzazione istogramma calcolata dall&#39;immagine di input. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Risoluzione istogramma</b> *Numero intero* | Larghezza dell’istogramma. Un valore più elevato consente una distribuzione più precisa.   Le risoluzioni disponibili sono, in pixel: 256, 512, 1024, 2048, 4096 |
| <b>Scala automatica</b> *Booleano* | Se è impostato su &quot;True&quot;, l&#39;istogramma viene rimappato in modo da utilizzare l&#39;intero height dell&#39;immagine.   Se è impostato su &#39;False&#39;, ogni colonna utilizzerà un numero di pixel nel height pari al numero di occorrenze di un valore nell&#39;immagine di input. |
| <b>Scala</b> *Virgola mobile* | Ridimensiona verticalmente l’istogramma, dove un valore pari a 1 rappresenta l’intero height dell’istogramma. |
| <b>Campionamento</b> *Numero intero* | Metodo di filtraggio dell’immagine dell’istogramma, che influisce sul risultato quando la risoluzione dell’istogramma e la risoluzione del rendering non corrispondono:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilineare:</b> applica un filtro bilineare all&#39;istogramma, creando punti interpolati</li> <li data-preserve-html="true"><b>Più vicino:</b> esegue un campionamento del pixel più vicino senza alcun filtro, ottenendo così passaggi piatti</li> </ul> |
| <b>Capovolgi asse Y</b> *Booleano* | Se è impostato su &#39;True&#39;, l&#39;istogramma viene riflesso verticalmente. |

## Esempi

![Rendering istogramma: esempio 1](../../../../../../assets/histogram_render_example_1.png "Rendering istogramma: esempio 1"){zoomable="yes"}

![Rendering istogramma: esempio 2](../../../../../../assets/histogram_render_example_2.png "Rendering istogramma: esempio 2"){zoomable="yes"}
