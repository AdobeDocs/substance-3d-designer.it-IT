---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: Utilizzare il nodo BaseColor Metallic Roughness Converter per convertire diversi formati di materiale PBR e flussi di lavoro.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convertitore rugosità metallica BaseColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# Convertitore BaseColor/Metallico/Rugosità

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/pbr-convert.png){width="128px"}

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo converte le mappe di colore di base, metallizzato e rugosità in diversi output del modello PBR, ad esempio il modello Specular/lucido. Alcuni degli obiettivi di output inclusi sono noti motori di rendering come Vray, Corona, Redshift, Renderman e Arnold.

Ciò è utile se disponete di grafici o materiali realizzati con un solo modello di PBR, mentre la destinazione richiede un modello diverso.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Utilizza input SpecularLevel</b> <i>Falso/Vero</i> | Espone uno slot di input aggiuntivo all&#39;input SpecularLevel. Di ciò si tiene conto anche durante la conversione. |
| <b>Destinazione</b> <i>Diffusa/Specular/lucido PBR, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)</i> | Imposta il modello di destinazione della conversione. |
