---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sostituisci intervallo colori per sostituire i colori all’interno di un intervallo specificato con nuovi colori per la correzione del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sostituisci intervallo colore
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Sostituisci intervallo colore

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](replace-color-range.resources/replace-color-range.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Sostituisce il colore di origine con il colore di destinazione, con controlli aggiuntivi. Può essere utilizzato, ad esempio, per ricolorare parti di una mappa ID materiale (bake).

Per una versione più avanzata, vedere [Corrispondenza colori.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Colore di origine</b> <i>(valore colore)</i> | Colore da sostituire. |
| <b>Colore di destinazione</b> <i>(valore colore)</i> | Colore con cui sostituire. |
| <b>Intervallo di origine</b> <i>0.0 - 1.0</i> | Intervallo o tolleranza dell&#39;origine selezionata. Possono essere aumentati in modo da modificare anche i colori adiacenti. |
| <b>Soglia</b> <i>0.0 - 1.0</i> | Decadimento/contrasto per l’intervallo. Imposta bassa per sostituire solo il colore sorgente e alta per sostituire anche la fusione dei colori in Sorgente. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="replace-color-range.resources/replace-color-range-example.png" />
        </td>
    </tr>
</table>
