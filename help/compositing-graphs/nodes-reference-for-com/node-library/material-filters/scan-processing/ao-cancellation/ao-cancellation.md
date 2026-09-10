---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Utilizza il nodo Annullamento OA per rimuovere l’occlusione ambientale dai materiali scansionati per un’elaborazione pulita delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annullamento AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# Annullamento AO

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancel.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo tenta di rimuovere qualsiasi informazione relativa all&#39;illuminazione dell&#39;Occlusione ambientale dalla mappa di Albedo (Colore di base), in base a un input di mappa AO separato. Può essere utilizzato per garantire che le informazioni di Albedo siano PBR corrette e per lo più prive di (forti) informazioni di illuminazione.

Un nodo utile per quando si dispone di una mappa AO eseguita i baking da una trama scansionata o in alternativa anche una mappa AO generata da informazioni di Height o Normale.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Annullamento AO</b> <i>0.0 - 1.0</i> | Intensità con cui rimuovere le informazioni di illuminazione. |
| <b>Saturazione AO</b> <i>0.0 - 1.0</i> | Compensazione della saturazione per le aree in cui viene rimossa l&#39;illuminazione. Questo può essere utilizzato per restituire qualsiasi perdita di colore nelle aree più scure. |
