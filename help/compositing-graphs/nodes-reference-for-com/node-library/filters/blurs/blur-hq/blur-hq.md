---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Usa il nodo Sfoca HQ per applicare effetti di sfocatura di alta qualità alle texture, per creare risultati di sfocatura uniformi e professionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# Sfocatura HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-1.png){width="128px"}

![](blur-hq.resources/blur-hq-grayscale.png){width="128px"}

<b>Ingresso:</b> Filtri > Sfocature

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Consente di eseguire una sfocatura gaussiana di alta qualità sul risultato. Qualità molto migliore rispetto a [la sfocatura standard della scatola atomica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Blur HQ&quot; per gli input di colore o &quot;Blur HQ Grayscale&quot; per gli input di scala di grigio.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 16.0</i> | Intensità (raggio) della sfocatura. Più alto è questo valore, maggiore sarà la sfocatura. |
| <b>Qualità</b> <i>0 - 1</i> | Aumenta la quantità di campionamento interno per una qualità ancora più elevata, a velocità di calcolo ridotta. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/hqblur-example.gif" />
        </td>
    </tr>
</table>
