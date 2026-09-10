---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilizza il nodo Filtro stagione per applicare effetti stagionali ai materiali per creare variazioni in primavera, estate, autunno e inverno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtro stagione
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# Filtro stagione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>Tra:</b> Filtri materiali > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo aggiunge effetti come livello dell&#39;acqua animato, neve, ghiaccio e/o muschio.

Tenete presente che si tratta di un filtro meno recente che non deve essere completamente corretto da PBR. Viene conservato principalmente per motivi preesistenti/di compatibilità, anche se in alcuni casi può ancora essere utile. Le versioni più recenti corrette per PBR sono disponibili in [Copertina Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e [Livello acqua](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Il nodo richiede un corretto insieme di input di materiale, principalmente con una Heightmap o Normalmap decentemente dettagliata.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Avanzate</b> |  |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera. |
| <b>Intensità luce</b> <i>0.0 - 1.0</i> | Intensità della luce (simulata). |
| <b>Angolo luce</b> <i>0.0 - 1.0</i> | Angolo di incidenza della luce (simulata) |
| <b>Effetto</b> |  |
| <b>Effetto dal Height o normale</b> <i>Height, Normale</i> | Consente di scegliere la mappa di input che determina gli effetti. |
| <b>Livello dell&#39;acqua</b> <i>0.0 - 1.0</i> | Aumenta o riduce il livello dell’acqua in base alle informazioni di Height/Normale. |
| <b>Dettagli acqua</b> <i>0.0 - 1.0</i> | Imposta la quantità di dettagli nell&#39;acqua. |
| <b>Rifrazione</b> <i>0.0 - 1.0</i> | Imposta la quantità di rifrazione falsa nell’effetto. |
| <b>Riflessione</b> <i>0.0 - 1.0</i> | Imposta la quantità di riflesso falso nell’effetto. |
| <b>Distanza di riflessione</b> <i>0.0 - 1.0</i> | Controlla gli elementi visivi di riflesso. |
| <b>Angolo di riflessione</b> <i>0.0 - 1.0</i> | Controlla gli elementi visivi di riflesso. |
| <b>Direzione flusso</b> <i>0.0 - 1.0</i> | Controlla il flusso dell’animazione (usa la Substance Player per visualizzare). |
| <b>Ghiaccio</b> <i>0.0 - 1.0</i> | Imposta il grado di congelamento dell’acqua. |
| <b>Dettagli ghiaccio</b> <i>0.0 - 1.0</i> | Imposta la quantità di dettagli nel ghiaccio. |
| <b>Snow</b> <i>0.0 - 1.0</i> | Imposta la quantità di copertura innevata. |
| <b>Moss</b> <i>0.0 - 1.0</i> | Imposta la quantità di copertura del muschio. |
| <b>Scala Moss</b> <i>1 - 4</i> | Imposta la scala della texture del muschio generata. |
| <b>Colore Moss</b> <i>(valore colore)</i> | Imposta il colore del muschio. |
| <b>Colore dell&#39;acqua</b> <i>(valore colore)</i> | Imposta il colore dell’acqua, inclusi canale alfa/opacità. |
| <b>Fusione</b> |  |
| <b>Intensità Diffusa</b> <i>0.0 - 1.0</i> | Intensità di fusione della Diffusione. |
| <b>Intensità Colore di base</b> <i>0.0 - 1.0</i> | Intensità di fusione del colore di base. |
| <b>Intensità normale</b> <i>0.0 - 1.0</i> | Intensità di fusione del normale. |
| <b>Intensità Specular</b> <i>0.0 - 1.0</i> | Forza di fusione dello Specular. |
| <b>Intensità Lucentezza</b> <i>0.0 - 1.0</i> | Forza di fusione della lucidità. |
| <b>Intensità rugosità</b> <i>0.0 - 1.0</i> | Forza di fusione della rugosità. |
| <b>Intensità Occlusione ambientale</b> <i>0.0 - 1.0</i> | Intensità di fusione dell’Occlusione ambiente. |
| <b>Intensità Height</b> <i>0.0 - 1.0</i> | Forza di fusione del Height. |
