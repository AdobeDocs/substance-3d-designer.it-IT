---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo di Worley 3D per generare il disturbo di Worley in base alla posizione 3D per creare effetti di texture volumetrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Disturbo di Worley 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Disturbo di Worley 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## Disturbo di Worley 3D

**Ingresso:** *Generatori Di Texture**/Rumori*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Uno dei rumori più versatili e avanzati della libreria, genera un disturbo di Worley in uno spazio 3D, basato su una mappa di posizione di input. Offre numerose opzioni che lo rendono molto più potente dei rumori standard basati su [Celle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)o [Distanza](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

## Parametri

* **Scala**: *1 - 64*\
  Impostate la scala globale per l’effetto.
* **Dimensioni**: *0,0 - 1,0* Eseguire separatamente il ridimensionamento non uniforme sugli assi X, Y e Z.
* **Modalità**: *Euclidean, Manhattan, Chebyshev, Minkowski\
  Modificate la metrica della distanza. Consente tipi di rumore molto diversi.*
* **Numero di Minkowski**: *0.0 - 20.0* Solo con metrica della distanza di Minkowski. Fusioni tra diversi tipi di metriche.
* **Stile**: *F1, F2, F2-F1, Bordo, Colore casuale* Impostare la combinazione di metriche. Consente molte più combinazioni.
* **Larghezza bordo**: *0.0 - 1.0* Quando la combinazione di bordi è attiva, controlla la larghezza del bordo.
* **Arrotondamenti**: *0.0 - 1.0* Disponibile solo con le modalità F1, F2 e F2-F1. Imposta la posizione intermedia del livello.
* **Inverti**: *Falso/Vero*\
  Inverte il risultato.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
