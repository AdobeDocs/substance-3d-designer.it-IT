---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Utilizzate il nodo Crea foto in porzioni per convertire le fotografie in texture di porzioni uniformi per la creazione di materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crea foto in piastrelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Crea foto in piastrelle

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>In:</b> Filtri > Affiancamento

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo fornisce la funzionalità di correzione dei bordi per qualsiasi immagine che potrebbe non essere affiancata a causa di bordi non continui. ma solo sui bordi dell&#39;immagine di input. Se desiderate regolare la scala o il riquadro in diversi modi, osservate [Crea un riquadro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Alterazione maschera H</b> <i>-100.0 - 100.0</i> | Introduce alterazioni sull’asse orizzontale per evitare transizioni indefinite. |
| <b>Alterazione maschera V</b> <i>-100.0 - 100.0</i> | Introduce alterazioni sull’asse verticale per evitare transizioni indefinite. |
| <b>Dimensione maschera H</b> <i>0.0 - 1.0</i> | Consente di impostare il valore di distanza orizzontale raggiunto dal bordo della transizione. |
| <b>Dimensione maschera V</b> <i>0.0 - 1.0</i> | Consente di impostare la distanza verticale del bordo di transizione. |
| <b>Precisione maschera H</b> <i>0.0 - 1.0</i> | Consente di impostare il grado di transizione orizzontale. |
| <b>Precisione maschera V</b> <i>0.0 - 1.0</i> | Consente di impostare l’attenuazione verticale della transizione. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>
