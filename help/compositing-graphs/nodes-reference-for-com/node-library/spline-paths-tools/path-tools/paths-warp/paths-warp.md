---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: Usate il nodo Alterazione tracciati per alterare le texture lungo le curve dei tracciati per creare pattern curvi e organici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterazione tracciati
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Alterazione tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](paths-warp.resources/paths-warp-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Deforma i percorsi di input in base all&#39;<b>input sfumatura</b>. Stesso effetto del nodo [Altera](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi. |
| <b>Input sfumatura</b> <i>Scala di grigi</i> | L’input di tipo height che controlla sia l’entità che la direzione dell’alterazione. Stesso effetto del nodo [Altera](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md). |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | I tracciati trasformati. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>Mobile</i> | Il parametro <b>Intensità</b> imposta l&#39;intensità dell&#39;alterazione. |
| <b>Numero di passaggi</b> <i>Numero intero</i> | Usate un valore più alto per alterare i tracciati di input di più piccoli incrementi.<br>Questo può impedire al percorso di intersecarsi, soprattutto quando si utilizzano valori di <b>intensità</b> elevati. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-warp.resources/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="paths-warp.resources/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
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

![Esempio di nodo 1](paths-warp.resources/PathsWarp-Demo1.gif "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
