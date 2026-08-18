---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione normale (Normal Blend) per fondere insieme le mappe normali e creare transizioni omogenee tra i dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# Fusione normale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## Fusione normale

**Ingresso:** *Filtri/Mappa Normale*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Fusione normale consente di fondere due mappe normali con una maschera opzionale, assicurandosi che tutti i valori rimangano normalizzati. Non differisce molto da un [nodo di fusione atomica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), ma ha aggiunto calcoli interni per Normalmaps.

Fusione normale non consente di combinare (sovrapporre) le mappe normali, in cui la mappa superiore aggiunge dettagli alla mappa inferiore. A tale scopo, utilizzare [Combinazione normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

## Parametri

### Input

* **NormalFG**: *Input colore*\
  Mappa Normale Primo Piano/Superiore.
* **NormalBG**: *Input colore*\
  Normalmap sfondo/inferiore.
* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivata/disattivata con il parametro &quot;Usa maschera&quot;.

### Parametri

* **Opacità**: *0,0 - 1,0*\
  Fusione dell’opacità tra primo piano e sfondo
* **Usa maschera**: *False/True*\
  Attiva o disattiva l’uso della mappa maschera.

## Immagini di esempio

![](../../../../../../assets/normalblend-ex.gif)

*(.gif introduce il dithering, ad esempio, i risultati nell&#39;applicazione sono uniformi)*

</td>
</tr>
</table>
