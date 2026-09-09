---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Utilizza il nodo da Flood Fill a sfumatura per riempire le aree con valori di sfumatura per creare transizioni di colore uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da Flood Fill a Sfumatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Da Flood Fill a Sfumatura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/floodfill-to-gradient.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Trasforma una base di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) in sfumature (orientate casualmente). Molto utile per creare una mappa altezza in cui le porzioni vengono inclinate e inclinate in modo casuale.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Input colore</i> | Dati del Flood Fill di base. |
| <b>Input angolo</b> <i>Input scala di grigi</i> | Mappa facoltativa per determinare l&#39;angolo per cella con una mappa esterna. |
| <b>Input Pendenza</b> <i>Input scala di grigi</i> | Mappa facoltativa per determinare l’intensità della pendenza sfumatura per cella. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Angolo</b> <i>0.0 - 1.0</i> | Imposta l’angolo/direzione globale uniforme per tutte le porzioni. |
| <b>Variazione angolo</b> <i>0.0 - 1.0</i> | Rende casuale l’angolo di ogni porzione singolarmente. Questo è il parametro più utile e potente! |
| <b>Moltiplica per dimensione rettangolo di selezione</b> <i>0.0 - 1.0</i> | Ridimensiona l’intero effetto lineare in base alla dimensione del rettangolo di selezione individuale della porzione. Ciò significa che le porzioni più piccole risulteranno più scure di quelle più grandi. |
| <b>Moltiplicatore input immagine angolare</b> <i>0.0 - 1.0</i> | Imposta l’influenza della mappa opzionale di input angolo sulle direzioni della sfumatura generata |
| <b>Moltiplicatore di input immagine Pendenza</b> <i>0.0 - 1.0</i> | Imposta l’influenza della mappa di input Pendenza opzionale sull’intensità della pendenza con gradiente generato. |
| <b>Moltiplica per intensità Pendenza</b> <i>0.0 - 1.0</i> |  |
| <b>Colore Pendenza Piatta</b> <i>(valore scala di grigi)</i> | Consente di impostare un valore solido per le pendenze piatte. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
