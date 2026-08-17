---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Utilizza il nodo da Flood Fill a sfumatura per riempire le aree con valori di sfumatura per creare transizioni di colore uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da Flood Fill a Sfumatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Da Flood Fill a Sfumatura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## Da Flood Fill a Sfumatura

**Ingresso:** *Filtri/Effetti*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Trasforma una base di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) in sfumature (orientate casualmente). Molto utile per creare una mappa altezza in cui le porzioni vengono inclinate e inclinate in modo casuale.

## Parametri

### Input

* **Flood Fill**: *Input colore* Dati del Flood Fill di base.
* **Input angolo**: *Input scala di grigi*\
  Mappa facoltativa per determinare l&#39;angolo per cella con una mappa esterna.
* **Input Pendenza**: *Input in scala di grigi* Mappa facoltativa per determinare l&#39;intensità di pendenza della sfumatura per cella.

### *Parametri*

* **Angolo**: *0.0 - 1.0* Imposta l&#39;angolo/direzione globale uniforme per tutte le porzioni.
* **Variazione angolo**: *0.0 - 1.0* Rende casuale l&#39;angolo di ogni porzione singolarmente. Questo è il parametro più utile e potente!
* **Moltiplica per dimensioni rettangolo di selezione**: *0.0 - 1.0* Ridimensiona l&#39;intero effetto lineare in base alle dimensioni del rettangolo di selezione individuale della porzione. Ciò significa che le porzioni più piccole risulteranno più scure di quelle più grandi.
* **Moltiplicatore input immagine angolare**: *0.0 - 1.0* Imposta l&#39;influenza della mappa input angolo opzionale sulle direzioni sfumatura generate
* **Moltiplicatore di input immagine Pendenza**: *0.0 - 1.0*\
  Imposta l’influenza della mappa di input Pendenza opzionale sull’intensità della pendenza con gradiente generato.
* **Moltiplica per intensità Pendenza**: *0.0 - 1.0*
* **Colore Pendenza piatta**: *(valore scala di grigi)*Consente di impostare un valore uniforme per le pendenze piatte.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
