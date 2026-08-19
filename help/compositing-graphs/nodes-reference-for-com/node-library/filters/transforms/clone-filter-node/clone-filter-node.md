---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilizzate il nodo del filtro Clona per duplicare e scostare le aree della texture e creare pattern ed effetti di affiancamento uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clona (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Clona (nodo filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## Clona

**Entrata:** *Filtri/Trasformazioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Clona l&#39;immagine di input una volta in una posizione specificata. Può funzionare come uno strumento &quot;timbro clone&quot; grezzo.

È necessario prestare particolare attenzione per ottenere i risultati desiderati:

* Idealmente, l’immagine di input avrà un canale alfa (come una decalcomania), poiché la fusione è solo una copia semplice.
* Poiché la maschera è impostata per impostazione predefinita sul nero, per visualizzare i risultati è necessario collegare almeno un valore di scala di grigi bianca uniforme.
* Lo scostamento consente di ritagliare facilmente l’esterno dell’immagine, quindi utilizzate valori piccoli.

## Parametri

### Input

* **Origine**: *Input colore*\
  Immagine da clonare. Importante: l’ideale sarebbe che l’immagine avesse un canale alfa.
* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Il valore predefinito è nero.

### Parametri

* **Scostamento**: *-*\
  Sposta o converte il risultato. Positivo è Sinistro e Su, Negativo è Destro e Giù. Usate valori piccoli: 1.0 e superiori lo spostano all’esterno dell’immagine.
* **Maschera sfocatura**: *0,0 - 10,0\
  Applica un filtro di sfocatura alla maschera per sfumare i bordi.*

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
