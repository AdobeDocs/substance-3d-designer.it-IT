---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilizzate il nodo Colore mappatore UV per mappare le texture di colore lungo le spline per la generazione di texture procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore mappatore UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Colore mappatore UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](uv-mapper-color.resources/uv-mapper-color-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue la mappatura dell&#39;immagine a colori di input usando le coordinate fornite nell&#39;input UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Consultate anche [Grafica con mappatura UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>UV</b> <i>Colore</i> | Coordinate immagine codificate nei canali rosso (U) e verde (V) di un’immagine a colori. |
| <b>Input</b> <i>Colore</i> | L&#39;immagine a colori che deve essere mappata alle coordinate fornite nell&#39;input UV. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Risultato della mappatura dell&#39;immagine di input utilizzando le coordinate UV di input come immagine a colori. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Colore di sfondo</b> <i>Float4</i> | Colore di sfondo dell&#39;immagine di output.<br>Lo sfondo è visibile nelle aree dell&#39;immagine in cui gli UV non sono definiti (ovvero il valore è (0, 0, 0, 0)). |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nodo nel grafico](uv-mapper-color.resources/UVMapperColor-Graph.jpg "Nodo nel grafico")
