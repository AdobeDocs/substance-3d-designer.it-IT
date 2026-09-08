---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Utilizzate il nodo Metallo meteorologico per aggiungere effetti di corrosione e ruggine realistici ai materiali metallici in base alla geometria della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metallo meteorologico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# Metallo meteorologico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Meteo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>WS normale</b> <i>Input colore</i> | Baked World Space Normalmap utilizzata per effetti interni e mascheratura. |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Avanzate</b> |  |
| <b>Formato Normale</b> <i>Direct X, Open GL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera. |
| <b>Effetto</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>Irritazione</b> <i>0.0 - 1.0</i> |  |
| <b>Indossamento bordi</b> <i>0.0 - 1.0</i> |  |
| <b>Pittura peeling</b> <i>0.0 - 1.0</i> |  |
| <b>Ruggine</b> <i>0.0 - 1.0</i> |  |
| <b>Ruggine peeling</b> <i>0.0 - 1.0</i> |  |
| <b>Ruggine verdigris</b> <i>Ruggine, Verdigris</i> |  |
| <b>Pittura scala Crepe</b> <i>1.0 - 16.0</i> |  |
| <b>Pittura intensità alterazione Crepe</b> <i>0.0 - 1.0</i> |  |
| <b>Scala Scratches bordi netti</b> <i>1.0 - 32.0</i> |  |
| <b>Intensità alterazione Scratches bordi netti</b> <i>0.0 - 1.0</i> |  |
| <b>Colore metallo grezzo</b> <i>(valore colore)</i> |  |
| <b>Colore Specular metallo grezzo</b> <i>(valore colore)</i> |  |
| <b>Valore Lucentezza Raw Metal</b> <i>(valore scala di grigi)</i> |  |
| <b>Valore rugosità metallo grezzo</b> <i>(valore scala di grigi)</i> |  |
| <b>Fusione</b> |  |
| <b>Intensità Diffusa</b> <i>0.0 - 1.0</i> | Intensità di fusione della Diffusione. |
| <b>Intensità Colore di base</b> <i>0.0 - 1.0</i> | Intensità di fusione del colore di base. |
| <b>Intensità normale</b> <i>0.0 - 64.0</i> | Intensità di fusione del normale. |
| <b>Intensità Specular</b> <i>0.0 - 1.0</i> | Forza di fusione dello Specular. |
| <b>Intensità Lucentezza</b> <i>0.0 - 1.0</i> | Forza di fusione della lucidità. |
| <b>Intensità rugosità</b> <i>0.0 - 1.0</i> | Forza di fusione della rugosità. |
| <b>Intensità metallica</b> <i>0.0 - 1.0</i> | Intensità di fusione del metallizzato. |
| <b>Intensità Occlusione ambientale</b> <i>0.0 - 1.0</i> | Intensità di fusione dell’Occlusione ambiente. |
| <b>Intensità Height</b> <i>0.0 - 1.0</i> | Forza di fusione del Height. |
