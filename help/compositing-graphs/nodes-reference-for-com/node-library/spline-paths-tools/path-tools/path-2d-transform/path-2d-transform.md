---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasforma tracciato 2D per Trasforma tracciati con operazioni di traslazione, rotazione e ridimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasforma 2D tracciato
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# Trasforma 2D tracciato

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/path-2d-transform-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Trasforma tracciati usando un gizmo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | I tracciati trasformati. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Matrice di trasformazione</b> <i>Float4</i> | Matrice di trasformazione applicata alle spline. Sono disponibili tre modalità di modifica dei parametri della matrice:<br>*- Gizmo Trasformazione:* modificare le maniglie del gizmo visualizzato in [vista 2D](../../../../../../interface/2d-view/2d-view.md) quando è selezionato il nodo di Trasforma 2D della spline;<br>*- Rotazione/Allungamento:* controllare singolarmente la rotazione e il allungamento delle spline. Si noti che i valori vengono sempre applicati relativamente alla trasformazione corrente. Ad esempio, se si applica due volte la larghezza del 50% si ottiene il 25% della larghezza;<br>*- Valori matrice:* Fare clic sul pulsante <b>Modifica valori matrice</b> per immettere direttamente i valori numerici non elaborati della matrice. |
| <b>Scostamento</b> <i>Float2</i> | Applica uno scostamento di posizione alle spline in X (orizzontale) e Y (verticale). |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
