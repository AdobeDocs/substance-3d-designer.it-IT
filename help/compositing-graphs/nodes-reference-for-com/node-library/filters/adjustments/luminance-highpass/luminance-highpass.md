---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Utilizzate il nodo Superficie luminanza (Luminance Highpass) per estrarre i dettagli della luminanza ad alta frequenza dalle texture per migliorare i dettagli delle superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passa luminanza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Passa luminanza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Consente di annullare le informazioni di illuminazione eseguendo un [highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)sul valore Luminanza dell&#39;input. Utile per fissare texture fotografata con informazioni sull’illuminazione. Può essere combinato in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) con più passaggi per rimuovere diverse frequenze di dettagli di illuminazione.

Mantenere i colori è un&#39;operazione leggermente migliore rispetto a [Illuminazione Annulla basse frequenze.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Raggio</b> <i>0.0 - 64.0</i> | Raggio dell’effetto passa-alto. Un raggio più piccolo annulla un’illuminazione più piccola e si regola in base alle immagini di input. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
