---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione multimateriale per fondere più materiali insieme per creare combinazioni di materiali complesse.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione multimateriale
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# Fusione multimateriale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend.png){width="128px"}

<b>In:</b> Filtri materiali > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo combina più materiali in base a una mappa ID materiale/ID colore, uno che può essere eseguito i baking da una trama. Sono necessari fino a 16 materiali completi diversi, con qualsiasi tipo di canale attivato nel gruppo Canali.

Il nodo è molto utile quando si creano texture di prop completi, in quanto consente la parametrizzazione completa dei materiali combinandoli dinamicamente. Perfetto per applicare texture da semplici a complesse con esegue i baking ID appropriati, o anche per creare Substance &quot;modello&quot; completamente pipeline che rispettano pienamente gli standard del team.

Tenete presente che, quando utilizzate questa opzione, Materiale 1, Slot 1 è sempre il materiale di default e apparirà in qualsiasi punto in cui nessun altro materiale verrà visualizzato. Ecco perché non potete impostare un colore per esso. Se si desidera eseguire questa operazione, è possibile, ad esempio, collegare un [Materiale di base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) impostato su nero di prova.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>1-16 slot di materiale completo</b> | La quantità di slot è determinata dal menu a discesa <b>Materiali</b>. |
| <b>ID colore</b> <i>Input colore</i> | Mappa ID colore eseguita i baking. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Materiali</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | Imposta la quantità massima di materiali diversi da unire. |
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/Lucentezza invece di Metallo/Rugosità. |
| <b>Materiale 2-16</b> | Viene visualizzato un gruppo per ogni materiale abilitato. |
| <b>Colore</b> <i>(valore colore)</i> | Colore da selezionare dalla mappa ID corrispondente a questo slot di materiale. |
| <b>Fuzziness</b> <i>0.01 - 1.0</i> | Sanguina nei colori vicini. |
| <b>Spaziatura interna</b> <i>0.0 - 1.0</i> | Durezza delle transizioni: contrasto della maschera. |
