---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasformazione tracciato 2D per trasformare i tracciati con le operazioni di traslazione, rotazione e ridimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione 2D tracciato
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Trasformazione 2D tracciato

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/path-2d-transform-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Trasforma i tracciati utilizzando un gizmo.

</td>
</tr>
</table>

## Connettori di ingresso

<b>Tracciati</b> *Colore*\
Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi.

## Connettori di uscita

<b>Tracciati</b> *Colore*\
I tracciati trasformati. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline.

## Parametri

<b>Matrice di trasformazione</b> *Float4*\
Matrice di trasformazione applicata alle spline. Sono disponibili tre modalità di modifica dei parametri della matrice:\
*- Gizmo Trasformazione:* modificare le maniglie del gizmo visualizzato nella [vista 2D](../../../../../../interface/2d-view/2d-view.md) quando è selezionato il nodo Trasformazione 2D spline;\
*- Rotazione/Dilatazione:* Controlla singolarmente la rotazione e l&#39;allungamento delle spline. Si noti che i valori vengono sempre applicati relativamente alla trasformazione corrente. Ad esempio, se si applica due volte la larghezza del 50% si ottiene una larghezza del 25%;\
*- Valori matrice:* Fare clic sul pulsante <b>Modifica valori matrice</b> per immettere direttamente i valori numerici non elaborati della matrice.

<b>Scostamento</b> *Float2*\
Applica uno scostamento di posizione alle spline in X (orizzontale) e Y (verticale).

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
