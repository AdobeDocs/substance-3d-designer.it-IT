---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione materiale per fondere interi materiali utilizzando maschere per creare effetti di materiale composito.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Fusione materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>In:</b> Filtri materiali > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Material Blend è l&#39;equivalente materiale completo multicanale di [atomic Blend Node](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Si fonde tra due materiali completi (tutti i possibili canali) in base a una maschera in scala di grigio o facoltativamente in base a un singolo colore da una Maschera ID colore.

Questo nodo è utile se desideri unire due materiali e avere una mappa in scala di grigio ma senza una selezione completa di ID colore. Se disponi di un forno Color ID e desideri fondere più di due materiali, ti consigliamo di utilizzare [Fusione multismateriale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>ID colore</b> <i>Input colore</i> | Mappa ID colore al forno opzionale. |
| <b>Maschera scala di grigi</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali di materiale in questo gruppo quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Diffusione</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Colore di base</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Normale</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Specular</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Emissivo</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Lucentezza</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Rugosità</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Metallico</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Specular level</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Occlusione ambiente</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Height</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Opacità</b> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> |  |
| <b>Maschera ID colore</b> <i>Falso/Vero</i> | Usate la maschera Maschera ID colore invece di quella in scala di grigio. Tieni presente che questo è solo per un colore! |
| <b>Colore</b> <i>(valore colore)</i> | Colore da selezionare e convertire in bianco. |
| <b>Fuzziness</b> <i>0.01 - 1.0</i> | Misura in cui il colore scelto si fonde con i colori adiacenti. |
| <b>Spaziatura interna</b> <i>0.0 - 1.0</i> | Contrasto di transizione del colore selezionato. |
