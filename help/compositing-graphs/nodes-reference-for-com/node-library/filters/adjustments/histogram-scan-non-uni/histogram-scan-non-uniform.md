---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Usa il nodo Istogramma non uniforme per eseguire la scansione istogramma non uniforme per la correzione avanzata del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scansione istogramma non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Scansione istogramma non uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione avanzata di [Scansione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), con controlli e input aggiuntivi per guidare l&#39;effetto a livello di pixel, anziché in modo uniforme in tutta l&#39;immagine. Può essere utilizzata per ottenere contrasti e transizioni ancora più intricati nelle maschere.

L&#39;utilizzo è molto più complesso rispetto alla normale [scansione dell&#39;istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), quindi assicurati di averne familiarità prima di provare a utilizzare la versione non uniforme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Input scala di grigi</i> | Risultato di origine da modificare. |
| <b>Mappa posizione</b> <i>Input scala di grigi</i> | Slot di input per guidare il parametro Posizione. Attivato quando &quot;Usa input posizione&quot; è impostato su True. L’intervallo di valori effettivi è ridotto e dipende dalle impostazioni e dalla mappa del contrasto. |
| <b>Mappa contrasto</b> <i>Input scala di grigi</i> | Slot di input per guidare il parametro di contrasto. Attivato quando &quot;Usa input contrasto&quot; è impostato su True. L&#39;intervallo dei valori effettivi è ridotto. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Usa input posizione</b> <i>Falso/Vero</i> | Attiva/disattiva l&#39;uso dello slot di input Mappa posizione. |
| <b>posizione</b> <i>0.0 - 1.0</i> | Controlla o modifica i risultati della mappa per determinare l&#39;impostazione della posizione. |
| <b>Usa input contrasto</b> <i>Falso/Vero</i> | Attiva/disattiva l&#39;uso dello slot di input Mappa contrasto. |
| <b>contrasto</b> <i>0.0 - 1.0</i> | Controlla o modifica i risultati della mappa per determinare l’impostazione del contrasto. |
