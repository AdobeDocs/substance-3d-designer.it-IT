---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rilievo di Uber per creare effetti di rilievo avanzati con controlli personalizzabili per profondità, angolo e illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rilievo Uber
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Rilievo Uber

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Rilievo Uber

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Versione avanzata con numerose funzionalità di [Rilievo](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Esegue un elaborato effetto di illuminazione 2D falso basato su una mappa di altezza.

È utile quando si crea un’illuminazione incorporata per alcuni stili di texture quando è necessario un grande controllo.

## Parametri

### Input

* **Colore**: *Input colore*\
  Immagine di base da modificare.
* **Height**: *Input scala di grigi*\
  Heightmap utilizzata come driver per l’effetto.

### Parametri

* **Colore ambiente**: *(Valore cromatico)*Colore utilizzato nelle aree in ombra.
* **Colore diffuso**: *(Valore colore)*Colore utilizzato nelle aree illuminate.
* **Colore Specular**: *(Valore colore)*Colore utilizzato per i riflessi degli specular
* **Intensità luce**: *0,0 - 1,0*\
  Intensità della luce (simulata).
* **Angolo luce**: *0,0 - 1,0*\
  Angolo di incidenza della luce (simulata)
* **Intensità Specular**: *0,0 - 1,0* Intensità dei riflessi degli specular.
* **Lucidità Specular**: *0,0 - 1,0* Dimensioni dell&#39;evidenziazione dello specular.
* **Rugosità diffusa**: *0.0 - 1.0* Rugosità utilizzata nel calcolo della luce diffusa.
* **Opacità ombre**: *0.0 - 1.0* Opacità di fusione delle aree in ombra.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
