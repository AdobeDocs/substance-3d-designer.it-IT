---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: Utilizzate il nodo Applica tavolozza colori per ridefinire le texture utilizzando una tavolozza di colori per ottenere effetti di colore stilizzati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Applica tavolozza colori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Applica tavolozza colori

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Quantizza colore](apply-color-palette.resources/ApplyColorPalette.png "Icona Quantizza colore"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica i colori di una tavolozza ordinata a un&#39;immagine utilizzando una mappa ID.

I colori vengono distribuiti confrontando gli indici della mappa ID con gli indici dei colori della tavolozza.

Ad esempio, i #2 di colore nella tavolozza verranno applicati a tutti i pixel nella mappa ID con un valore ID pari a 2.

Questo nodo può essere utilizzato in combinazione con i seguenti nodi: [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crea tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modifica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Visualizza tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>ID</b> <i>Scala di grigi</i> PRIMARIO | Mapping ID di input utilizzato per distribuire i colori nella tavolozza di input.   Una mappa ID è un’immagine in cui i pixel che fanno parte di un intero (ad esempio, una forma) mantengono tutti lo stesso valore di identificazione univoco. In questo caso, il valore è un numero intero.   È possibile produrre una mappa ID utilizzando un nodo [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Tavolozza</b> <i>Colore</i> | Un elenco ordinato di colori RGB codificati come una riga di pixel. La tavolozza può contenere un massimo di 256 colori. Tavolozza mappata dal nodo agli indici della mappa ID.   Le tavolozze possono essere prodotte con un nodo [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) e modificate con un nodo [Modifica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md). |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Risultato della mappatura dei colori della tavolozza agli indici della mappa ID. |

## Esempi

![Applica tavolozza colori: esempio 1](apply-color-palette.resources/apply_color_palette_example_2.png "Applica tavolozza colori: esempio 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_1_before.jpg" alt="apply_color_palette_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_1_after.jpg" alt="apply_color_palette_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Applica tavolozza colori: esempio 3](apply-color-palette.resources/apply_color_palette_example_4.png "Applica tavolozza colori: esempio 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_3_before.jpg" alt="apply_color_palette_example_3_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply_color_palette_example_3_after.jpg" alt="apply_color_palette_example_3_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
