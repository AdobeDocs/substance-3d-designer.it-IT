---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Usa il nodo Effetto rilievo di Uber per creare effetti effetto rilievo avanzati con controlli personalizzabili per profondità, angolo e illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rilievo Uber
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Rilievo Uber

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione avanzata con numerose funzionalità di [Effetto rilievo](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Esegue un elaborato effetto di illuminazione 2D falso basato su una mappa di altezza.

È utile quando si crea un’illuminazione eseguita i baking per alcuni stili di texture quando è necessario un grande controllo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Colore</b> <i>Input colore</i> | Immagine di base da modificare. |
| <b>Height</b> <i>Input scala di grigi</i> | Heightmap utilizzata come driver per l’effetto. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Colore ambiente</b> <i>(valore colore)</i> | Colore usato nelle aree in ombra. |
| <b>Colore Diffusa</b> <i>(valore colore)</i> | Colore usato nelle aree illuminate. |
| <b>Colore Specular</b> <i>(valore colore)</i> | Colore usato per i riflessi degli specular |
| <b>Intensità luce</b> <i>0.0 - 1.0</i> | Intensità della luce (simulata). |
| <b>Angolo luce</b> <i>0.0 - 1.0</i> | Angolo di incidenza della luce (simulata) |
| <b>Intensità Specular</b> <i>0.0 - 1.0</i> | Intensità dei riflessi dello specular. |
| <b>Lucentezza Specular</b> <i>0.0 - 1.0</i> | Dimensione dell&#39;evidenziazione dello specular. |
| <b>Rugosità Diffusa</b> <i>0.0 - 1.0</i> | Rugosità utilizzata nel calcolo dell’illuminazione diffusa. |
| <b>Opacità ombre</b> <i>0.0 - 1.0</i> | Opacità di fusione delle aree in ombra. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uberemboss-ex.png" />
        </td>
    </tr>
</table>
