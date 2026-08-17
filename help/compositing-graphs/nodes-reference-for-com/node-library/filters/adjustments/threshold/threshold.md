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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# Soglia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## Soglia

**Ingresso:** *Filtri/Regolazioni*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Restituisce bianco se i *criteri di confronto* impostati nel parametro **Mode** sono soddisfatti per il valore del pixel di input relativamente al valore **Threshold**.\
Simile a [Scansione istogramma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), ma con contrasto sempre al livello massimo. Funge da metodo più preciso e veloce per ottenere risultati simili a quelli ottenuti con la scansione dell’istogramma.

### Parametri

* **Soglia**: *0.0 - 1.0*\
  Valore di luminanza rispetto al quale viene confrontato il valore del pixel di input.
* **Modalità**:\
  Criterio in base al quale confrontare il valore del pixel di input con il valore **Soglia**:
  * *Maggiore*
  * *Maggiore o uguale*
  * *Inferiore*
  * *Inferiore o uguale*

## Immagini di esempio

</td>
</tr>
</table>
