---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Usa il nodo Morphing vettoriale per morfologia delle texture tra due input, utilizzando campi vettoriali per transizioni graduali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Morphing vettoriale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# Morphing vettoriale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## Morphing vettoriale (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Distorce un’immagine di input mediante una mappa vettoriale. L’effetto è simile alla distorsione UV con una mappa normale o con una mappa di flusso nei dispositivi di ombreggiatura dei videogiochi. I pixel di input vengono spostati dai vettori definiti nei valori Rosso e Verde della mappa vettoriale.

Questo nodo di per sé non è il più difficile da utilizzare, ma la creazione di una mappa vettoriale appropriata richiede attenzione. Si consiglia di lavorare con le profondità di bit più alte per garantire precisione durante il morphing.

La morphing vettoriale è molto simile a [Alterazione vettoriale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md): la differenza principale è che questo nodo morphing non &quot;ripete&quot; o &quot;affianca&quot; il risultato quando viene spinto al di fuori dei limiti dell&#39;area di lavoro. Al contrario, blocca e ripete i bordi.

## Parametri

### Input

* **Input**: *Input a colori/scala di grigi* L&#39;input di origine che deve essere la destinazione per l&#39;alterazione.
* **Campo vettoriale**: *Input colore* La mappa vettoriale utilizzata per guidare l&#39;alterazione.

### Parametri

* **Quantità**: *0.0 - 1.0* Imposta l&#39;intensità dell&#39;effetto di alterazione e funziona come moltiplicatore per la mappa vettoriale.

## Immagini di esempio

</td>
</tr>
</table>
