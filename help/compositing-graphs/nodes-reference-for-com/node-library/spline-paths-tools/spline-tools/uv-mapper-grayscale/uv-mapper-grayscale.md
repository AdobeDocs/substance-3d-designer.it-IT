---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilizzate il nodo Mappatura UV scala di grigi per mappare le texture in scala di grigi lungo le spline per la generazione procedurale delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura UV in scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Mappatura UV in scala di grigi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/uv-mapper-grayscale-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Mappa l’immagine in scala di grigio di input usando le coordinate fornite nell’input UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Vedere anche [Colore mappatore UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>UV</b> <i>Colore</i> | Coordinate immagine codificate nei canali rosso (U) e verde (V) di un’immagine a colori. |
| <b>Input</b> <i>Colore</i> | L&#39;immagine in scala di grigio che deve essere mappata alle coordinate fornite nell&#39;input UV. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Risultato della mappatura dell’immagine di input utilizzando le coordinate UV di input, come immagine in scala di grigio. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-After.jpg" alt="UVMapper-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Esempio di nodo 1](../../../../../../assets/UVMapper-Graph.jpg "Esempio di nodo 1")
