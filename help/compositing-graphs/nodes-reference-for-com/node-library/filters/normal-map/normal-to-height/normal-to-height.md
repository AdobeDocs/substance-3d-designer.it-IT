---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilizzare il nodo Normale a Height per convertire le mappe normali in mappe height per estrarre le informazioni sulle profondità di superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale al Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Normale al Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Normale al Height

**Ingresso:** *Filtri/Mappa Normale*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo di conversione inversa che tenta di riconvertire una Normalmap dello spazio tangente in una Heightmap. Questa è la versione leggermente più semplice; [Normale alla sede centrale del Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) dispone di più opzioni.

Utile per quando si dispone solo di una sorgente Normalmap, ma si desidera comunque eseguire operazioni combinandole con una Heightmap. Tenete presente che questo non sarà mai in grado di fornire un risultato corretto al 100%, poiché le informazioni vengono perse per natura del processo quando il Height viene convertito in Normale. Se regoli le impostazioni di conseguenza, questa versione non-HQ esegue un buon lavoro di conversione dei dettagli semplici.

## Parametri

* **Bilanciamento Rilievi**: *0,0 - 1,0* Regolate la misura in cui le diverse frequenze influenzano il risultato finale. Ciò dipende in larga misura dalla mappa di input e richiede un po&#39; di modifica.
* **Formato normale**: *DirectX, OpenGL*\
  Passa da un formato Normalmap a un altro (inverte il canale verde).
* **Opacità globale**: *0.0 - 1.0* Regola l&#39;opacità globale dell&#39;effetto.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
