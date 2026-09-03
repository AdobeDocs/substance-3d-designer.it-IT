---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Utilizza il nodo Colore sicuro di Albedo PBR per garantire che i colori di albedo rientrino negli intervalli fisicamente plausibili per i materiali PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore sicuro Albedo PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Colore sicuro Albedo PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color-01.png){width="128px"}

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Si tratta di un nodo di utilità che corregge se i valori di Colore di base o Diffusa non rientrano in un intervallo accettabile e corretto per PBR. Quando è impostato su Metallico, il nodo tenta inoltre di correggere i valori di Colore di base in base all&#39;intensità del metallizzato.

Consultate anche [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) per il feedback visivo sulle aree che potrebbero essere errate.

Ciò è utile come strumento di correzione rapida, specialmente quando si sta ancora imparando la PBR, ma non inteso come una misura assoluta che si suppone sempre corretta.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Flusso di lavoro PBR</b> <i>Colore di base - Metallico, Diffusa - Specular</i> | Consente di passare da un flusso di lavoro PBR a un altro. |
| <b>Tolleranza</b> <i>0.0 - 1.0</i> | Quantità di tolleranza per valori che non rientrano nell&#39;intervallo consentito. |
