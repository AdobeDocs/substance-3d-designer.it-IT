---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-select.html"
breadcrumb-title: ''
description: Utilizzate il nodo Selezione istogramma per selezionare ed estrarre intervalli specifici dagli istogrammi delle texture per le regolazioni di destinazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selezione istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---


# Selezione istogramma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-select.resources/histogram-select.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Simile a [Scansione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), questo effetto imposta una posizione del valore in scala di grigi, con un intervallo attorno al quale si dissolve. Il contrasto può essere regolato per rendere la gamma più nitida.

[Fai clic qui per guardare un video dell’Accademia di Substance su Histogram Select.](https://youtu.be/p9wcmJBFyGA?t=535)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Posizione</b> <i>0.0 - 1.0</i> | Imposta la posizione centrale in cui avviene la selezione dell’intervallo. |
| <b>Intervallo</b> <i>0.0 - 1.0</i> | Imposta la larghezza dell&#39;intervallo di selezione. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto/decadimento del risultato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-select.resources/histoselect-ex.gif" />
        </td>
    </tr>
</table>
