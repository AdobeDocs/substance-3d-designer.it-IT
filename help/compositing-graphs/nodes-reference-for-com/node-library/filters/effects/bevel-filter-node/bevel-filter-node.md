---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Utilizzare il nodo del filtro Smusso per creare bordi smussati su forme e motivi per aggiungere profondità e dimensione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Smussato (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# Smussato (nodo filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## Smusso

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue un effetto di smussatura dei bordi su una mappa di altezza in scala di grigi di input. Restituisce sia Heightmap smussato che Normalmap in base a tale Heightmap.

Questo è un nodo utile per applicare profili di curve esatti su una Heightmap di base idealmente binaria (bianco/nero con elevato contratto).

## Parametri

### Input

* **input**: *Input scala di grigi*\
  Heightmap da convertire.
* **Curva personalizzata**: *Input scala di grigi*\
  Sfumatura che determina la curva/pendenza esatta. Idealmente è un nodo lineare sfumatura, su cui è possibile eseguire qualsiasi tipo di regolazione, ad esempio [Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) o [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Attivo solo quando &quot;Usa curva personalizzata&quot; è True.

### Parametri

* **Distanza**: *-1,0 - 1,0* Distanza oltre la quale deve estendersi l&#39;effetto smussato.
* **Tipo angolo**: *Arrotondato, Angular* Se il profilo di smussatura deve essere arrotondato o diritto.
* **Attenuazione**: *0.0 - 5.0* Quantità di attenuazione aggiuntiva (sfocatura) da eseguire dopo la smussatura.
* **Usa sfocatura non uniforme**: *False/True* Indica se l&#39;arrotondamento deve essere eseguito in modo non uniforme.
* **Usa curva personalizzata**: *False/True* Attiva/disattiva l&#39;utilizzo della curva di height personalizzata. Vedi sopra per maggiori informazioni.
* **Intensità normale**: *0,0 - 50,0* Intensità della mappa normale generata.
* **Formato normale**: *DirectX, OpenGL*\
  Consente di passare da un formato Normalmap a un altro (inverte il canale Verde).

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
