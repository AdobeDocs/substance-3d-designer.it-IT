---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/create-color-palette-16.html"
breadcrumb-title: ''
description: Utilizzate il nodo Crea tavolozza colori per estrarre una tavolozza di 16 colori dalle texture per ottenere effetti stilizzati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Create Color Palette (16)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crea tavolozza colori (16)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Crea tavolozza colori (16)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Quantizza colore](../../../../../../assets/CreateColorPalette16.png "Icona Quantizza colore"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Crea un elenco ordinato di colori ed esegue l&#39;output come tavolozza, con un massimo di 16 colori.

Il nodo può accodare nuovi colori a una tavolozza esistente, utilizzando il set di input &#39;Tavolozza&#39;.

Questo nodo può essere utilizzato in combinazione con i seguenti nodi: [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Applica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Modifica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Visualizza tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

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
| <b>Tavolozza</b> *Colore* PRIMARIO | Un elenco ordinato di colori RGB codificati come una riga di pixel. La tavolozza può contenere un massimo di 256 colori.   Questo input è opzionale. Se utilizzati, i colori impostati dal nodo vengono aggiunti a questa tavolozza.   È possibile visualizzare la tavolozza con il nodo [Visualizza tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |
| <b>Quantità colore tavolozza</b> *Numero intero* | Quantità di colori memorizzati nella tavolozza.   Se tale numero non corrisponde alla quantità effettiva di colori nell&#39;input dell&#39;immagine &quot;Palette&quot;, la visualizzazione potrebbe essere incompleta o disporre di più spazi vuoti del necessario. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Tavolozza</b> *Colore* | Tavolozza aggiornata con i colori specificati aggiunti. |
| <b>Quantità colore tavolozza</b> *Numero intero* | La quantità aggiornata di colori memorizzati nella tavolozza, con la quantità specificata di colori aggiunti. |

## Parametri

|  |  |
| --- | --- |
| <b>Quantità colore</b> *Numero intero* | Quantità di colori da aggiungere alla tavolozza. |
| <b>Colore n. </b> *Float3* *Numero di parametri disponibili corrispondente al valore &#39;Quantità colore&#39;* | Un colore da aggiungere alla tavolozza.   I colori vengono aggiunti alla tavolozza nello stesso ordine dell&#39;elenco numerato. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Creare una tavolozza di colori: esempio 1](../../../../../../assets/create_color_palette_example_1.png "Creare una tavolozza di colori: esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Creare una tavolozza di colori: esempio 2](../../../../../../assets/create_color_palette_example_2.png "Creare una tavolozza di colori: esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

![Creare una tavolozza di colori: esempio 3](../../../../../../assets/create_color_palette_example_3.png "Creare una tavolozza di colori: esempio 3"){zoomable="yes"}
