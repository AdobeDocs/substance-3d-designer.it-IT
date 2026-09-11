---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione colore materiale per fondere i canali di colore tra i materiali per creare effetti di materiale composito.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione colore materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Fusione colore materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>In:</b> Filtri materiali > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo consente di regolare un materiale completo multicanale fondendo i colori uniformi in alto. Questa è la differenza principale con [Fusione di regolazione materiale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), che consente solo regolazioni di tipo [Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) ai canali, mentre questo nodo utilizza regolazioni di tipo [Fusione](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) con un colore a tinta unita.

Questo nodo è particolarmente utile se desiderate introdurre un suggerimento di colore piatto nelle Diffuse o nei Colori di base, oppure se desiderate &quot;appiattire&quot; altri canali utilizzando un valore di colore a tinta unita impostato.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>ID colore</b> <i>Input colore</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Maschera scala di grigi</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali di materiale in questo gruppo quando utilizzate mappe Specular/Lucentezza invece di Metallico/Rugosità. |
| <b>Diffusa</b> |  |
| <b>Colore</b> <i>(valore colore)</i> | Quale valore di colore fondere sopra il canale della Diffusa? |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo. |
| <b>Metodo fusione</b> <i>Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Switch</i> | Modalità Fusione da utilizzare nell&#39;operazione. |
| <b>Colore di base</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Normale</b> |  |
| <b>Origine</b> <i>Height, maschera</i> |  |
| <b>Metodo fusione</b> <i>Combina, Fusione</i> |  |
| <b>Intensità Height</b> <i>0.0 - 1.0</i> |  |
| <b>Opacità Height</b> <i>0.0 - 1.0</i> |  |
| <b>Formato</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Emissivo</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Lucentezza</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Rugosità</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Metallico</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Specular level</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Occlusione ambientale</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Height</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Opacità</b> | Fusione un colore in tinta unita sopra questo canale con le opzioni come nel gruppo di Diffuse. |
| <b>Maschera ID colore</b> <i>Falso/Vero</i> | Usate la maschera Maschera ID colore invece di quella in scala di grigio. Tieni presente che questa opzione è valida solo per un colore.<br><br>Consente di attivare tutte le opzioni seguenti. |
| <b>Colore</b> <i>(valore colore)</i> | Colore da selezionare e convertire in bianco. |
| <b>Fuzziness</b> <i>0.01 - 1.0</i> | Misura in cui il colore scelto si fonde con i colori adiacenti. |
| <b>Spaziatura interna</b> <i>0.0 - 1.0</i> | Contrasto di transizione del colore selezionato. |
