---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Utilizzate il nodo Soglia per convertire le texture in scala di grigio in bianco e nero in base a un valore di soglia per la creazione di maschere.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Soglia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# Soglia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](threshold.resources/threshold-2.png){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Restituisce bianco se i *criteri di confronto* impostati nel parametro **Mode** sono soddisfatti per il valore del pixel di input relativamente al valore **Threshold**.\
Simile a [Scansione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), ma con contrasto sempre al livello massimo. Funge da metodo più preciso e veloce per ottenere risultati simili a quelli ottenuti con la scansione dell’istogramma.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Soglia</b> <i>0.0 - 1.0</i> | Valore di luminanza rispetto al quale viene confrontato il valore del pixel di input. |
| <b>Modalità</b> | Criterio in base al quale confrontare il valore del pixel di input con il valore **Soglia**:<br><br>- *Maggiore*<br>- *Maggiore o uguale*<br>- *Minore*<br>- *Minore o uguale* |
