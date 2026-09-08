---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Utilizzate il nodo Illuminazione Annulla alte frequenze per rimuovere i dettagli di illuminazione ad alta frequenza dalle texture per l'analisi del materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Illuminazione Annulla Alte Frequenze
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# Illuminazione Annulla Alte Frequenze

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/lighting-cancel-high-frequencies.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Simile a [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), ma più adatto per le immagini a colori pieni (non desatura il risultato), questo nodo tenta di annullare i dettagli luminosi piccoli e ad alta frequenza.

Consultate anche [Illuminazione - Annulla basse frequenze](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) e il [Highpass luminanza](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md) più avanzato consigliato.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 1.0</i> | Intensità dell’effetto di annullamento illuminazione. |
| <b>Raggio</b> <i>0.0 - 10.0</i> | Raggio o dimensione dei dettagli di illuminazione da annullare. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
