---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilizzate il nodo Selettore materiale per selezionare i materiali in base ai dati della trama per creare effetti di texture multimateriali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selettore materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Selettore materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## Selettore materiale

**Ingresso:** *Generatori Basati Su Trama**/Utility*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Converte una mappa ID a colori in una maschera binaria in bianco e nero. Consente di fondere e combinare colori diversi in una maschera.

Questa funzione è utile se non desideri utilizzare [Fusione multimateriale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) e preferisci utilizzare la maschera manualmente oppure se desideri utilizzare manualmente le stesse maschere in altre posizioni.

## Parametri

* **Materiali**: 1 - 16\
  Imposta il numero di materiali per cui è abilitata la combinazione.
* **Abilita #1-16 Materiale**: False/True\
  Attiva o disattiva la fusione e la combinazione di colori nella maschera di output finale. Può essere attivato per tutti i colori che desideri combinare.
* **#1-16 materiale**: (valore colore)\
  Selettore colore per il colore dei materiali che verrà convertito in bianco e nero.
* **Parametri Selettore colore**\
  Modifica la fusione e la conversione del colore in bianco e nero.
  * **Sfocature**: 0,01 - 1,0\
    Quanto miscelare con i colori adiacenti.
  * **Spaziatura interna**: 0,0 - 1,0\
    Nitidezza della transizione, ad esempio Contrasto.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
