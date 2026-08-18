---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilizza il nodo Trasformazione normale per applicare le trasformazioni alle mappe normali mantenendo correttamente le direzioni vettoriali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Trasformazione normale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## Trasformazione normale

**Ingresso:** *Filtri/Mappa Normale*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Simile al nodo 2D di trasformazione atomica, questo permette la trasformazione di Normalmaps senza interrompere lo spazio tangente, ma viene ricalcolato al volo, risultando sempre in Normalmaps corretti.

## Parametri

* **Matrice2x2**: *(Matrice di trasformazione):*\
  Ruota o ridimensiona l&#39;input.
* **Scostamento**: *-0,5 - 0,5*\
  Sposta o converte il risultato. Quando è presente il controllo Trasformazione, il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Formato normale**: *DirectX, OpenGL*\
  Passare da un Formato mappa normale a un altro (inverte il canale verde)

</td>
</tr>
</table>
