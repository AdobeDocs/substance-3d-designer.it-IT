---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Annullamento AO

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## Annullamento AO

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo tenta di rimuovere qualsiasi informazione di illuminazione dell&#39;Occlusione ambiente dalla mappa dell&#39;Albedo (Colore base), in base a un input mappa AO separato. Può essere utilizzato per garantire che le informazioni di Albedo siano PBR corrette e per lo più prive di (forti) informazioni di illuminazione.

Un nodo utile per quando si dispone di una mappa dell&#39;operatore aereo cotta da una trama scansionata o in alternativa anche una mappa dell&#39;operatore aereo generata da informazioni di Height o Normale.

## Parametri

* **Annullamento AO**: *0.0 - 1.0* Intensità con cui rimuovere le informazioni di illuminazione.
* **Saturazione AO**: *0,0 - 1,0*(De)Compensazione della saturazione per le aree in cui viene rimossa l&#39;illuminazione. Questo può essere utilizzato per restituire qualsiasi perdita di colore nelle aree più scure.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
