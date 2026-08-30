---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Utilizza il nodo Annullamento OA per rimuovere l’occlusione dell’ambiente dai materiali scansionati per un’elaborazione pulita delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annullamento AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
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

Questo nodo tenta di rimuovere qualsiasi informazione di illuminazione dell&#39;Occlusione ambiente dalla mappa dell&#39;Albedo (Colore base), in base a un input mappa AO separato. Può essere utilizzato per garantire che le informazioni di Albedo siano PBR corrette e per lo più prive di (forti) informazioni di illuminazione.

Un nodo utile per quando si dispone di una mappa dell&#39;operatore aereo cotta da una trama scansionata o in alternativa anche una mappa dell&#39;operatore aereo generata da informazioni di Height o Normale.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Annullamento AO</b> <i>0.0 - 1.0</i> | Intensità con cui rimuovere le informazioni di illuminazione. |
| <b>Saturazione AO</b> <i>0.0 - 1.0</i> | Compensazione della saturazione per le aree in cui viene rimossa l&#39;illuminazione. Questo può essere utilizzato per restituire qualsiasi perdita di colore nelle aree più scure. |
