---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: Usa le funzioni hash nei grafici delle funzioni per generare valori casuali deterministici basati sulle coordinate di input.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Funzioni Hash
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Funzioni Hash

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo hash: icon](../../../../../assets/hash-icon.png "Nodo hash: icon"){width="200px"}

<b>In:</b> Funzioni > Casuale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Calcola un valore pseudo-casuale compreso tra 0 e 1, in base a un valore di input utilizzato come valore di inizializzazione.

Il numero nel titolo mostra il tipo di valore in entrata e in uscita. Esempio: Hash 23 prende un valore float2 come input e genera un valore float3.

</td>
</tr>
</table>

Quando un nodo Hash genera un valore di più componenti, ogni componente ha un valore pseudo-casuale diverso.

Versioni disponibili, con tipo di input e tipo di output:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Hash 11:</b> Mobile → Mobile

<b>Hash 14:</b> Mobile → Float4

<b>Hash 21:</b> Mobile2 → Mobile

<b>Hash 22:</b> Float2 → Float2

</td>
<td style="border: 0;" valign="top">

<b>Hash 24:</b> Float2 → Float4

<b>Hash31:</b> Mobile3 → Mobile

<b>Hash 32:</b> Float3 → Float2

</td>
</tr>
</table>

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> | Valore utilizzato come valore di inizializzazione per calcolare l&#39;output pseudo-casuale. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di hash 14](../../../../../assets/hash14-example.png "Esempio di hash 14"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Esempio di hash 32](../../../../../assets/hash32-example.png "Esempio di hash 32"){zoomable="yes"}

</td>
</tr>
</table>
