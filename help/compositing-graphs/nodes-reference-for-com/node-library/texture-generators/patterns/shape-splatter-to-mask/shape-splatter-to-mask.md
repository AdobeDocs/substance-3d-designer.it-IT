---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Usa il nodo Splatter forma a maschera per convertire i motivi di splatter forma in maschere per la fusione di materiali ed effetti.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Divisione forme in maschera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Divisione forme in maschera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## Divisione forme in maschera

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Converte i dati di [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) in una maschera in bianco e nero in base all&#39;ID pattern. Consente, ad esempio, di creare una maschera contenente solo un determinato tipo di motivo. Include opzioni aggiuntive per la selezione di un intervallo di ID pattern e per nascondere casualmente alcune forme.

## Parametri

### Parametri

* **Intervallo iniziale ID pattern**: *1 - 8* Impostare il primo ID pattern nell&#39;intervallo da selezionare.
* **Intervallo finale ID pattern**: *1 - 8* Impostare l&#39;ultimo ID pattern nell&#39;intervallo da selezionare.
* **Maschera casuale**: *0.0 - 1.0* Impostate la proporzione dei pattern in modo da mascherarli in modo casuale.
* **Output**: *Maschera binaria, Maschera intera, Valori scala di grigi* Determina il tipo di valori di output. La Maschera binaria restituisce solo i valori in bianco e nero, 0-o-1. La Maschera con valori interi codificherà i valori più alti fino a 8 per ogni Pattern in formato HDR. I Valori in scala di grigi diffonderanno l&#39;intervallo proporzionalmente tra 0 e 1.

</td>
</tr>
</table>
