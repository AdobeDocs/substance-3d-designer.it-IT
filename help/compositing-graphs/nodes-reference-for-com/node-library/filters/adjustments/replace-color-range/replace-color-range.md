---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sostituisci intervallo colori per sostituire i colori all’interno di un intervallo specificato con nuovi colori per la correzione del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sostituisci intervallo colore
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# Sostituisci intervallo colore

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## Sostituisci intervallo colore

**Ingresso:** *Filtri/Regolazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Sostituisce il colore di origine con il colore di destinazione, con controlli aggiuntivi. Può essere utilizzato, ad esempio, per ricolorare parti di una mappa ID materiale (bake).

Per una versione più avanzata, vedere [Corrispondenza colori.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## Parametri

* **Colore di origine**: *(valore colore)*Colore da sostituire.
* **Colore di destinazione**: *(valore colore)*Colore da sostituire con.
* **Intervallo di origine**: *0.0 -* 1.0\
  Intervallo o tolleranza dell&#39;origine selezionata. Possono essere aumentati in modo da modificare anche i colori adiacenti.
* **Soglia**: *0.0 - 1.0* Decadimento/contrasto per l&#39;intervallo. Imposta bassa per sostituire solo il colore sorgente e alta per sostituire anche la fusione dei colori in Sorgente.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
