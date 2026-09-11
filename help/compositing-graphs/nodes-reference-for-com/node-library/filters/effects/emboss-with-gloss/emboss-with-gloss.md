---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: Usa il nodo Effetto rilievo con lucentezza per creare effetti in rilievo con mappe di lucentezza per aggiungere profondità e lucentezza alle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Effetto rilievo con lucentezza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# Effetto rilievo con lucentezza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue un effetto rilievo con una maggiore lucentezza (riflesso specular) su un colore e un input height. In sostanza, aggiunge un’illuminazione falsa e eseguita i baking a un’immagine in base alle informazioni del height. Utile per alcuni stili di creazione di texture che richiedono illuminazione eseguita i baking nelle texture.

Per una versione con altre opzioni, consulta [Uber Effetti rilievi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md). Esiste anche la versione atomica più semplice di [Effetto rilievo](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Colore</b> <i>Input colore</i> |  |
| <b>Height</b> <i>Input scala di grigi</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Colore evidenziazione</b> <i>(valore colore)</i> | Colore della luce dello specular. |
| <b>Colore ombra</b> <i>(valore colore)</i> | Colore usato nelle aree in ombra o non illuminate. |
| <b>Lucentezza</b> <i>0.0 - 0.5</i> | Lucentezza dimensioni evidenziazione. |
| <b>Intensità</b> <i>0.0 - 10.0</i> | Intensità della luce. |
| <b>Angolo luce</b> <i>0.0 - 1.0</i> | Angolo di incidenza della luce (simulata). |
