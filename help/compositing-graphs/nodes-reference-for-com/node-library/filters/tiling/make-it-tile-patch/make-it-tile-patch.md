---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Utilizzate il nodo Crea patch per porzioni per applicare patch e creare texture di porzioni uniformi dalle immagini di input.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Imposta come patch porzione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# Imposta come patch porzione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch-01.png)

![](make-it-tile-patch.resources/make-it-tile-patch-02.png)

<b>In:</b> Filtri > Affiancamento

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo è un tiler semi-casuale basato su griglia. Prende una patch di input e la timbra, tentando di trasformarla in un&#39;immagine in porzioni senza troppe ripetizioni, in base alle tue impostazioni.

Utile per quando avete una piccola porzione di texture e desiderate creare una texture in porzioni più grande da essa.

Tieni presente che questo è diverso da [Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), che corregge principalmente i bordi.

Per eseguire questa operazione con un intero materiale, vedere [Affianca automatica avanzata](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Dimensioni maschera</b> <i>0.0 - 1.0</i> | Dimensioni della maschera rotonda usata per applicare il cerotto. |
| <b>Precisione maschera</b> <i>0.0 - 1.0</i> | Precisione di decadimento/smoothness della maschera. |
| <b>Alterazione maschera</b> <i>-100.0 - 100.0</i> | Introduce alterazioni sui bordi della maschera. Ideale per evitare transizioni omogenee e indefinite tra le patch. |
| <b>Larghezza motivo</b> <i>0.0 - 1000.0</i> | Cambia la larghezza del cerotto in modo non uniforme. |
| <b>height dimensioni pattern</b> <i>0.0 - 1000.0</i> | Cambia il height del cerotto in modo non uniforme. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Introduce la casualità di traduzione, spostando leggermente le patch. |
| <b>Variazione dimensioni</b> <i>0.0 - 100.0</i> | Introduce variazioni di dimensione per la maschera. |
| <b>Ottava</b> <i>0 - 6</i> | Questo è il controllo principale che determina le dimensioni complessive. |
| <b>Rotazione</b> <i>-360.0 - 360.0</i> | Pre-ruota il cerotto. |
| <b>Variazione rotazione</b> <i>0.0 - 360.0</i> | Introduce una rotazione casuale per ogni timbro patch. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Consente di impostare il colore di sfondo per le aree in cui non viene visualizzata alcuna patch. |
| <b>Variazione colore</b> <i>0.0 - 1.0 (Solo Versione A Colori)</i> | Introduce variazioni di colore per patch. |
| <b>Variazione luminosità</b> <i>(solo versione in scala di grigio)</i> | Introduce la variazione di luminosità per patch. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/make-it-tile-patch-03.gif" />
        </td>
    </tr>
</table>
