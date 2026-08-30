---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione di regolazione materiale per fondere le regolazioni del materiale tra i materiali per ottimizzare gli effetti compositi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blend di regolazione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Blend di regolazione materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend.png){width="128px"}

<b>In:</b> Filtri materiali > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo consente la regolazione di tutti i canali di un materiale completo, in base a una maschera. ed è stato progettato per rendere più semplice e veloce l&#39;intero flusso di lavoro dei materiali.

È utile per regolare alcuni canali di un materiale (ad esempio, per rendere la diffusione più luminosa e la rugosità più scura) in base alla stessa maschera.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera ID colore</b> <i>Input colore</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Maschera scala di grigi</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attiva e disattiva i canali di materiale in questo gruppo, ad esempio quando si utilizzano mappe Specular/Lucentezza anziché Metallico/Rugosità.<br><br>In questo modo si attiva e disattiva anche l&#39;aspetto dei gruppi rilevanti del canale. |
| <b>Diffusione</b> | Esegue le operazioni di regolazione sul canale Diffusione, nelle aree definite dalla maschera. |
| <b>Colore di base</b> | Esegue le operazioni di regolazione sul canale Colore di base, nelle aree definite dalla maschera. |
| <b>Normale</b> |  |
| <b>Intensità</b> <i>0.0 - 1.0</i> | Riduce l&#39;intensità normale |
| <b>Specular</b> | Esegue le operazioni di regolazione sul canale dello Specular, nelle aree definite dalla maschera. |
| <b>Emissivo</b> | Esegue operazioni di regolazione sul canale di emissione, nelle aree definite dalla maschera. |
| <b>Lucentezza</b> | Esegue le operazioni di regolazione sul canale Lucentezza, nelle aree definite dalla maschera. |
| <b>Rugosità</b> | Esegue le operazioni di regolazione sul canale Rugosità, nelle aree definite dalla maschera. |
| <b>Metallico</b> | Esegue le operazioni di regolazione sul canale Metallico, nelle aree definite dalla maschera. |
| <b>Specular level</b> | Esegue le operazioni di regolazione sul canale di Specular level, nelle aree definite dalla maschera. |
| <b>Occlusione ambiente</b> | Esegue le operazioni di regolazione sul canale di Occlusione ambiente, nelle aree definite dalla maschera. |
| <b>Height</b> | Esegue le operazioni di regolazione sul canale del Height, nelle aree definite dalla maschera. |
| <b>Opacità</b> | Esegue le operazioni di regolazione sul canale Opacità, nelle aree definite dalla maschera. |
| <b>Maschera ID colore</b> <i>Falso/Vero</i> | Imposta per usare la maschera Maschera ID colore invece di scala di grigio. |
| <b>Fuzziness</b> <i>0.01 - 1.0</i> | Se Maschera ID colore è attivato, questa opzione determina la diffusione del colore di selezione ID colore. |
| <b>Colore</b> <i>(valore colore)</i> | Consente di impostare il colore da scegliere dalla mappa ID colore e dalla maschera. |
| <b>Spaziatura interna</b> <i>0.0 - 1.0</i> | Determina il contrasto/le transizioni di fusione della maschera Color ID. |
