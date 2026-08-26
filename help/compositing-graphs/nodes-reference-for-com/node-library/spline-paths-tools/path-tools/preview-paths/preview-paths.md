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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Anteprima tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/preview-paths-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Traccia segmenti e vertici del tracciato sopra lo sfondo specificato. Un colore casuale per tracciato.

Otterrai un risultato simile all&#39;output <b>Anteprima</b> di [Maschera nei tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), ma con più opzioni.

</td>
</tr>
</table>

## Connettori di ingresso

<b>Sfondo</b> *Colore*\
Un&#39;immagine di sfondo sopra a con visualizza il tracciato. Controlla anche le dimensioni di rendering.

<b>Tracciati</b> *Colore*\
Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi.

## Parametri

<b>Mostra angoli</b> *Booleano*\
Visualizza un quadratino su ciascun vertice contrassegnato come angolo (fusione additiva).

<b>Mostra vertici</b> *Booleano*\
Visualizza una forma circolare su ciascun vertice (fusione additiva). Gli angoli vengono ancora visualizzati come quadrati.

<b>Thickness segmenti (px)</b> *Mobile*\
Regola il thickness di segmenti sottoposti a rendering in pixel.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "Esempio di nodo 2")

</td>
</tr>
</table>
