---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: Usa il nodo Trasformazione quadrata su tracciato per applicare trasformazioni quadratiche agli elementi lungo le curve del tracciato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quad Transform on Path
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Quad Transform on Path

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](quad-transform-on-path.resources/quad-transform-on-path-01.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Deforma un tracciato usando 4 maniglie.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione *percorso*. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | I tracciati trasformati. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>p00</b> <i>Float2</i> | Posizione della maniglia superiore sinistra. |
| <b>p01</b> <i>Float2</i> | Posizione della maniglia superiore destra. |
| <b>p02</b> <i>Float2</i> | Posizione della maniglia inferiore sinistra. |
| <b>p03</b> <i>Float2</i> | Posizione della maniglia inferiore destra. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-02.jpg" alt="PathsPolygon_Variant1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-03.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-02.jpg" alt="PathsPolygon_Variant1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/quad-transform-on-path-04.jpg" alt="QuadTransformOnPaths-Variant2-After">
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

![Esempio di nodo 1](quad-transform-on-path.resources/quad-transform-on-path-05.gif "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](quad-transform-on-path.resources/quad-transform-on-path-06.gif "Esempio di nodo 2")

</td>
</tr>
</table>
