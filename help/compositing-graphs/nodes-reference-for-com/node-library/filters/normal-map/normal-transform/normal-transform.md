---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Utilizza il nodo Trasforma normale per applicare le trasformazioni alla mappa normale mantenendo correttamente le direzioni vettoriali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Trasformazione normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Simile al nodo 2D della Trasforma atomica, questo permette la trasformazione di Normalmaps senza rompere lo spazio Tangente, invece viene ricalcolato al volo, risultando sempre in Normalmaps corretti.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Matrice2x2</b> <i>(matrice di trasformazione):</i> | Ruota o ridimensiona l&#39;input. |
| <b>Scostamento</b> <i>-0.5 - 0.5</i> | Sposta o converte il risultato. Quando è presente il controllo Trasformazione, il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passare da un Formato mappa normale a un altro (inverte il canale verde) |
