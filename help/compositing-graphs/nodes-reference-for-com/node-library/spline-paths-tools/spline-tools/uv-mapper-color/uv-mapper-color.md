---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Utilizzate il nodo Colore mappatura UV per mappare le texture di colore lungo le spline per la generazione procedurale delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore mappatore UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Colore mappatore UV

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/uv-mapper-color-icon.png "Icona nodo")

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

## Connettori di ingresso

<b>UV</b> *Colore* Coordinate dell’immagine codificate nei canali rosso (U) e verde (V) di un’immagine a colori.

<b>Input</b> *Colore* Immagine a colori da mappare alle coordinate fornite nell&#39;input UV.

## Connettori di uscita

<b>Output</b> *Colore* Risultato della mappatura dell&#39;immagine di input utilizzando le coordinate UV di input, come immagine a colori.

## Parametri

<b>Colore di sfondo</b> *Float4* Colore di sfondo dell&#39;immagine di output.\
Lo sfondo è visibile nelle aree dell’immagine in cui gli UV non sono definiti (ovvero il valore è (0, 0, 0, 0)).

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
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
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
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nodo nel grafico](../../../../../../assets/UVMapperColor-Graph.jpg "Nodo nel grafico")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
