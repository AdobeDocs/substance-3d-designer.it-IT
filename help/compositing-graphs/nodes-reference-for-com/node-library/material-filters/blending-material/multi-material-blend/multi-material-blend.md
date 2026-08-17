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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Fusione multimateriale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## Fusione multimateriale

**Ingresso:** *Filtri materiale/Fusione*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo combina più materiali in base a una mappa ID materiale/ID colore, uno che può essere preparato da una trama. Sono necessari fino a 16 materiali completi diversi, con qualsiasi tipo di canale attivato nel gruppo Canali.

Il nodo è molto utile quando si creano texture di prop completi, in quanto consente la parametrizzazione completa dei materiali combinandoli dinamicamente. Perfetto per applicare texture di prop semplici o complessi con i corretti colori ID, o anche per creare Substance &quot;template&quot; completamente pipeline che rispettano pienamente gli standard del team.

Tenete presente che, quando utilizzate questa opzione, Materiale 1, Slot 1 è sempre il materiale di default e apparirà in qualsiasi punto in cui nessun altro materiale verrà visualizzato. Ecco perché non potete impostare un colore per esso. Se si desidera eseguire questa operazione, è possibile, ad esempio, collegare un [Materiale di base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) impostato su nero di prova.

## Parametri

### Input

* **1-16 Slot di materiale completo** La quantità di slot è determinata dal menu a discesa **Materiali**.
* **ID colore**: *Input colore*\
  Mappa ID colore al forno.

### Parametri

* **Materiali**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16* Imposta la quantità massima di materiali diversi da unire.
* **Canali**\
  Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Materiale 2-16** Viene visualizzato un gruppo per ogni materiale abilitato.
  * **Colore**: *(valore colore)*Colore da scegliere dalla mappa ID corrispondente a questo slot di materiale.
  * **Sfocatura**: *0.01 - 1.0* Smarginatura nei colori adiacenti.
  * **Spaziatura interna**: *0.0 - 1.0* Durezza transizioni: contrasto maschera.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
