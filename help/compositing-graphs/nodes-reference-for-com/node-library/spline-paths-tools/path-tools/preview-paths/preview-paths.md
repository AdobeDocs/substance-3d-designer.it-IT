---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: Utilizzare il nodo Anteprima percorsi per visualizzare i dati dei percorsi nella vista 2D per il debug e la verifica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anteprima tracciati
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Anteprima tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](preview-paths.resources/preview-paths-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Traccia segmenti e vertici del tracciato sopra lo sfondo specificato. Un colore casuale per tracciato.

Otterrai un risultato simile all&#39;output <b>Anteprima</b> di [Maschera nei tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), ma con più opzioni.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Sfondo</b> <i>Colore</i> | Un&#39;immagine di sfondo sopra a con visualizza il tracciato. Controlla anche le dimensioni di rendering. |
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Mostra angoli</b> <i>Booleano</i> | Visualizza un quadratino su ciascun vertice contrassegnato come angolo (fusione additiva). |
| <b>Mostra vertici</b> <i>Booleano</i> | Visualizza una forma circolare su ciascun vertice (fusione additiva). Gli angoli vengono ancora visualizzati come quadrati. |
| <b>Thickness segmenti (px)</b> <i>Mobile</i> | Regola il thickness di segmenti sottoposti a rendering in pixel. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](preview-paths.resources/PathsToSpline-Variant2-Before_1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](preview-paths.resources/PathsToSpline-Variant1-Before_1.jpg "Esempio di nodo 2")

</td>
</tr>
</table>
