---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# Scansione istogramma non uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## Scansione istogramma non uniforme

**Ingresso:** *Filtri/Regolazioni*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Versione avanzata di [Scansione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), con controlli e input aggiuntivi per guidare l&#39;effetto a livello di pixel, anziché in modo uniforme in tutta l&#39;immagine. Può essere utilizzata per ottenere contrasti e transizioni ancora più intricati nelle maschere.

L&#39;utilizzo è molto più complesso rispetto alla normale [scansione dell&#39;istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), quindi assicurati di averne familiarità prima di provare a utilizzare la versione non uniforme.

## Parametri

### Input

* **Input**: *Input in scala di grigi* Risultato di origine da modificare.
* **Mappa posizione**: *Input scala di grigi* Slot di input per l&#39;unità del parametro Posizione. Attivato quando &quot;Usa input posizione&quot; è impostato su True. L’intervallo di valori effettivi è ridotto e dipende dalle impostazioni e dalla mappa del contrasto.
* **Mappa contrasto**: *Input scala di grigi* Slot di input per attivare il parametro di contrasto. Attivato quando &quot;Usa input contrasto&quot; è impostato su True. L&#39;intervallo dei valori effettivi è ridotto.

### Parametri

* **Usa input posizione**: *False/True* Attiva/disattiva l&#39;uso dello slot di input della mappa posizione.
* **posizione**: *0.0 - 1.0* Controlla o modifica i risultati della mappa per controllare l&#39;impostazione della posizione.
* **Usa input contrasto**: *False/True* Attiva/disattiva l&#39;uso dello slot di input Mappa contrasto.
* **contrasto**: *0.0 - 1.0* Controlla o modifica i risultati della mappa per determinare l&#39;impostazione del contrasto.

## Immagini di esempio

</td>
</tr>
</table>
