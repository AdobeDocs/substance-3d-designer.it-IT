---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Utilizzare il nodo PBR BaseColor Metallic Validate per convalidare e correggere i valori di base e metallici per i materiali PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convalida metallizzata PBR BaseColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR BaseColor/Metallic Validate

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di utilità che genera una &quot;Heatmap&quot; buona-cattiva in cui i valori sono corretti o errati in base agli standard PBR.

È molto utile come strumento di apprendimento per PBR, poiché fornisce un feedback visivo molto chiaro su quali sono gli errori e dove possono essere trovati.

Non utilizzare questo strumento come strumento finale, ma assicurati comunque di avere sempre una chiara comprensione del motivo per cui stai infrangendo le regole che questo strumento potrebbe evidenziare.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità di convalida</b> <i>Albedo, Metallo, Combinato</i> | Consente di impostare se controllare solo l’Albedo, Metal o entrambe combinate come modalità panoramica. |
| <b>Albedo soglia intervallo scuro</b> <i>50 sRGB, 30 sRGB</i> | Imposta il limite inferiore di Albedo su 50 o 30 sRGB. Può diminuire o aumentare la tolleranza per le aree rosse. |
| <b>Intervallo di riflessione Metal</b> <i>70-100% Riflettente, 60-100% Riflettente</i> | Modifica l&#39;intervallo metallico in modo che venga considerato corretto. Può diminuire o aumentare la tolleranza per le aree rosse. |
| <b>Sovrapposizione mappa</b> <i>Falso/Vero</i> | La modalità di debug rapido per sovrapporre le mappe di input consente di individuare più rapidamente le aree problematiche. |
