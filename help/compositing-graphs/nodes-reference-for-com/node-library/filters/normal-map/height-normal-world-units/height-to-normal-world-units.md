---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: Utilizzare il nodo Height a unità di misura normali per convertire le mappe di height in mappe normali utilizzando la scala dell'unità di misura mondiale per dettagli accurati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height a unità mondiali normali
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Height a unità mondiali normali

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-to-normal-world-units.resources/normal-hq.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo avanzato di conversione da Height a Normale che utilizza unità reali durante la conversione.

Utile per quando si conoscono le dimensioni della Heightmap sorgente e si desidera eseguire la conversione più accurata, ad esempio quando si lavora con materiale scansionato.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Dimensioni superficie (cm)</b> <i>0.0 - 1000.0</i> | Dimension della mappa altezza di input. |
| <b>Profondità Height (cm)</b> <i>0.0 - 100.0</i> | Profondità massima dei dettagli di Heightmap. |
| <b>Formato Normale</b> <i>OpenGL, DirectX</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Campionamento</b> <i>Standard, Sobel</i> | Passa da una modalità di campionamento all’altra per determinare la precisione. |
