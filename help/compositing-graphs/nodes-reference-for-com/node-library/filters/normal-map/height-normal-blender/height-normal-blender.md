---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione normale Height (Normal Blender) per fondere le mappe di height e normale per combinare le informazioni dettagliate sulla superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione normale height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Fusione normale height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Fusione normale height

**Ingresso:** *Filtri/Mappa Normale*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo di scelta rapida che fonde una mappa di altezza in scala di grigio su una mappa normale. L&#39;input di Height viene convertito internamente in una mappa normale e quindi mescolato correttamente con l&#39;input normale.

Si tratta di un metodo più rapido per fondere i dettagli rispetto a quello manuale con nodi separati, ma potrebbe non essere sufficientemente controllato e perfezionato per determinate esigenze.

## Parametri

### Input

* **Height**: *Input scala di grigi*\
  Heightmap scala di grigi con cui fondersi.
* **Normale**: *Input colore*\
  Base Normalmap su cui fondere.

### Parametri

* **Intensità normale**: *0,0 - 16,0* Intensità della conversione normale dell&#39;input di Height.
* **Formato normale**: *DirectX, OpenGL*\
  Passa da un formato Normalmap a un altro (inverte il canale verde).

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
