---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: Utilizza il nodo Ritaglio per ritagliare gli output del materiale in aree specifiche per l’elaborazione di materiali e texture scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Ritaglia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

## Ritaglio (scala di grigi)

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Il ritaglio è una versione parametrica e non distruttiva del noto strumento di ritaglio. Quando si seleziona un’area di un’immagine, il risultato viene restituito e le aree non selezionate vengono eliminate.

Può essere utile in molti modi, poiché eseguire un&#39;operazione di ritaglio con nodi atomici non è così semplice. Soprattutto per la conversione di immagini non quadrate, questo nodo è utile. In tal caso, assicurati di impostare correttamente la risoluzione di input.

Molto importante da capire è che per utilizzare questo nodo con facilità, è necessario fare buon uso della possibilità di visualizzare in anteprima un nodo diverso da quello di cui si stanno modificando i parametri!\
In breve: **fare doppio clic** sul nodo che si sta utilizzando come input per questo (l&#39;immagine originale non ritagliata), quindi **fare un solo clic** sul nodo di ritaglio che segue immediatamente. Puoi quindi modificare il gizmo Ritaglio per adattarlo all’area in cui desideri ritagliare.

## Parametri

* **Dimensione input**: *0 - 8192* Risoluzione e proporzioni dell&#39;immagine di input. Molto importante per immagini non quadrate.
* **Sfondo**: *(Valore colore) / (Valore scala di grigi)*Valore uniforme dello sfondo per le aree non coperte dal ritaglio.
* **Trasformazione**: *(Matrice Di Trasformazione)*\
  Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Scostamento**: *0,0 - 1,0*\
  Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Normale (solo per la versione a colori)**: *Falso/Vero* Indica se l&#39;input deve essere trattato come una mappa normale.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
