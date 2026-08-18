---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Utilizzare il nodo QG Normale al Height per convertire le mappe normali in mappe di height di alta qualità per l'estrazione dei dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale alla sede centrale del Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Normale alla sede centrale del Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## Normale alla sede centrale del Height

**Ingresso:** *Filtri/Mappa Normale*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo di conversione inversa che tenta di riconvertire una Normalmap dello spazio tangente in una Heightmap. Questo è il nodo più avanzato; [Normale al Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) ha meno opzioni e utilizza calcoli diversi.

Utile per quando si dispone solo di una sorgente Normalmap, ma si desidera comunque eseguire operazioni combinandole con una Heightmap. Tenete presente che questo non sarà mai in grado di fornire un risultato corretto al 100%, poiché le informazioni vengono perse per natura del processo quando il Height viene convertito in Normale. Non può mai sostituire una mappa dell&#39;altezza generata correttamente.

## Parametri

* **Formato normale**: *DirectX, OpenGL*\
  Passa da un formato Normalmap a un altro (inverte il canale verde).
* **Bilanciamento Rilievi**: *0,0 - 1,0* Fusioni tra distorsione a bassa e alta frequenza.
* **Intensità Height**: *0,0 - 1,0* Intensità o moltiplicatore per Heightmap, funziona un po&#39; come l&#39;opacità globale.
* **Normalizzazione Height**: *False/True* Ridimensiona automaticamente l&#39;intervallo della mappa altezza per utilizzare il contrasto completo, ad esempio un [livello automatico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md).
* **Qualità**: *Normale, Alta* Alterna velocità o qualità.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
