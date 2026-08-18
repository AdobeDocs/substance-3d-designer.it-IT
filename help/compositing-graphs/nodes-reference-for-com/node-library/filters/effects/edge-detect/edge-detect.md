---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rilevamento bordi per rilevare i bordi nelle texture e creare così profili ed effetti maschera basati sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rilevamento bordo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Rilevamento bordo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## Rilevamento bordo

**Ingresso:** *Filtri/Effetti*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Rileva il contrasto nelle immagini in bianco e nero, quindi crea una maschera in bianco e nero che evidenzia il contrasto.

Utile in molti casi in cui è necessaria una maschera per i bordi. Tieni presente che funziona meglio con input ad alto contrasto; se necessario, regola il contrasto prima di passare qualcosa in questo nodo.

## Parametri

* **Larghezza bordo**: *1.0 - 16.0* Larghezza delle aree rilevate attorno ai bordi.
* **Rotondità bordo**: *0.0 - 16.0* Arrotonda, sfoca e smussa la maschera generata.
* **Inverti**: *Falso/Vero*\
  Inverte il risultato.
* **Tolleranza**: *0.0 - 1.0* Fattore soglia tolleranza per la posizione in cui devono apparire i bordi.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
