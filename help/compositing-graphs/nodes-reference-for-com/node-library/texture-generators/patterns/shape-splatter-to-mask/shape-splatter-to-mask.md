---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
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
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# Divisione forme in maschera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter-to-mask.resources/shape-splatter-to-mask.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Converte i dati di [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) in una maschera in bianco e nero in base all&#39;ID pattern. Consente, ad esempio, di creare una maschera contenente solo un determinato tipo di motivo. Include opzioni aggiuntive per la selezione di un intervallo di ID pattern e per nascondere casualmente alcune forme.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intervallo iniziale ID modello</b> <i>1 - 8</i> | Impostare il primo ID pattern nell&#39;intervallo da selezionare. |
| <b>Intervallo finale ID modello</b> <i>1 - 8</i> | Impostare l&#39;ultimo ID pattern nell&#39;intervallo da selezionare. |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | Imposta la proporzione dei Pattern da mascherare in modo casuale. |
| <b>Output</b> <i>Maschera binaria, Maschera Intera, Valori In Scala Di Grigio</i> | Determinare il tipo di valori di output. La Maschera binaria restituisce solo i valori in bianco e nero, 0-o-1. La Maschera con valori interi codificherà i valori più alti fino a 8 per ogni Pattern in formato HDR. I Valori in scala di grigi diffonderanno l&#39;intervallo proporzionalmente tra 0 e 1. |
