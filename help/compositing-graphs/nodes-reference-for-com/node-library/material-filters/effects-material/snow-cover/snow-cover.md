---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Utilizzare il nodo Copertina Snow per aggiungere effetti di accumulo di neve ai materiali in base all'angolo e alla posizione della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Copertina Snow
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Copertina Snow

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

<b>Tra:</b> Filtri materiali > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Effetto all-in-one per aggiungere un accumulo di neve su un materiale completo. Si affida fortemente a una buona mappa di altezza di alta qualità, come ad esempio da una fotoscan. Il risultato deve essere corretto per PBR.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Snow fresco</b> <i>0.0 - 1.0</i> | Imposta la quantità di neve nelle aree in rilievo. Il risultato è legato al parametro Snow fuso. |
| <b>Snow fuso</b> <i>0.0 - 1.0</i> | Imposta la quantità di neve sciolta negli angoli in basso. |
| <b>Compilazione</b> <i>0.0 - 1.0</i> | La maggior parte influisce sull’output del Height e determina l’effetto di accumulo del height. |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | Consente di impostare l’attenuazione dei dettagli del height in base all’accumulo di neve. |
| <b>Intensità fiocchi</b> <i>0.0 - 1.0</i> | Colpisce principalmente Normalmap, l&#39;intensità dei dettagli della scaglia. |
