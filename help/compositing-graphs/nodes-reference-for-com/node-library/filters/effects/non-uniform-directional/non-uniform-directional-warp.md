---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Usate il nodo Non Uniform Directional Warp per applicare l’alterazione direzionale non uniforme per la creazione di vari effetti di distorsione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 5%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-uniform-directional-warp.resources/non-uniform-directional-warp-color.png)![](non-uniform-directional-warp.resources/non-uniform-directional-warp-grayscale.png)

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Alterazione direzione non uniforme è una versione avanzata di [Alterazione direzione](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) che consente di impostare l’intensità e la direzione dell’alterazione in base all’input di un’immagine. Consente un maggiore controllo e può creare una distorsione dell’immagine molto utile e interessante, nello stesso vano di [Sfocatura Pendenza](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Differisce da [Alterazione multidirezionale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) in quanto consente il controllo dell’angolo tramite un input Mappa personalizzato, mentre Alterazione multidirezionale consente di controllare solo la direzione tramite parametri. Ciò significa che potete creare effetti di scia e curvatura avanzati che altrimenti non sarebbero possibili.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Input scala di grigi</i> | Mappa di base a cui verrà applicata l’alterazione. |
| <b>Input intensità</b> <i>Input scala di grigi</i> | La mappa maschera obbligatoria che determina l’intensità dell’effetto di alterazione deve essere in scala di grigi. |
| <b>Input angolo di alterazione</b> <i>Input scala di grigi</i> | La mappa maschera obbligatoria che determina l’angolo dell’effetto di alterazione deve essere in scala di grigi. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 20.0</i> | Consente di impostare l’intensità dell’effetto di alterazione e l’ampiezza dell’allontanamento dei pixel. |
| <b>Angolo di alterazione</b> <i>0.0 - 1.0</i> | Consente di impostare l’angolo o la direzione in cui applicare l’effetto Altera. |
| <b>Moltiplicatore input angolo di alterazione</b> <i>0.0 - 1.0</i> | Imposta l’effetto della mappa di input dell’angolo di alterazione. La mappa di input dell’angolo di alterazione verrà utilizzata per interpolare da 0 al valore di questo parametro. |
| <b>Modalità traccia</b> <i>Min, Max, Media</i> | Consente di impostare il metodo di fusione delle tracce. |
| <b>Lunghezza della traccia</b> <i>0.0 - 1.0</i> | Imposta la lunghezza delle tracce. |
| <b>Dissolvenza traccia</b> <i>0.0 - 1.0</i> | Imposta il valore di dissolvenza di ogni traccia |
| <b>Curva di avanzamento</b> <i>-1.0 - 1.0</i> | Ha effetto solo se la dissolvenza della traccia è diversa da 0. Imposta il comportamento dell’effetto di dissolvenza. |
