---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## Direzione non uniforme Altera (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Alterazione direzione non uniforme è una versione avanzata di [Alterazione direzione](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) che consente di impostare l’intensità e la direzione dell’alterazione in base all’input di un’immagine. Consente un maggiore controllo e può creare una distorsione dell’immagine molto utile e interessante, nello stesso vano di [Sfocatura Pendenza](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

Differisce da [Alterazione multidirezionale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md) in quanto consente il controllo dell’angolo tramite un input Mappa personalizzato, mentre Alterazione multidirezionale consente di controllare solo la direzione tramite parametri. Ciò significa che potete creare effetti di scia e curvatura avanzati che altrimenti non sarebbero possibili.

## Parametri

### Input

* **Input**: *Input scala di grigi*\
  Mappa di base a cui verrà applicata l’alterazione.
* **Input intensità**: *Input scala di grigi*\
  La mappa maschera obbligatoria che determina l’intensità dell’effetto di alterazione deve essere in scala di grigi.
* **Input angolo di alterazione**: *Input scala di grigi*\
  La mappa maschera obbligatoria che determina l’angolo dell’effetto di alterazione deve essere in scala di grigi.

### Parametri

* **Intensità**: *0,0 - 20,0*\
  Consente di impostare l’intensità dell’effetto di alterazione e l’ampiezza dell’allontanamento dei pixel.
* **Angolo di alterazione**: *0,0 - 1,0*\
  Consente di impostare l’angolo o la direzione in cui applicare l’effetto Altera.
* **Moltiplicatore input angolo di alterazione**: *0,0 - 1,0*\
  Imposta l’effetto della mappa di input dell’angolo di alterazione. La mappa di input dell’angolo di alterazione verrà utilizzata per interpolare da 0 al valore di questo parametro.
* **Modalità Trail**: *Min, Max, Media*\
  Consente di impostare il metodo di fusione delle tracce.
* **Lunghezza della traccia**: *0,0 - 1,0*\
  Imposta la lunghezza delle tracce.
* **Dissolvenza della traccia**: *0.0 - 1.0*\
  Imposta il valore di dissolvenza di ogni traccia
* **Curva di traccia**: *-1.0 - 1.0* Ha effetto solo se la dissolvenza della traccia non è 0. Imposta il comportamento dell’effetto di dissolvenza.

## Immagini di esempio

</td>
</tr>
</table>
