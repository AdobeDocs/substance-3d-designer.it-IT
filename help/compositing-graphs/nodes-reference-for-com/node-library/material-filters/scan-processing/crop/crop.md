---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# Ritaglia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il ritaglio è una versione parametrica e non distruttiva del noto strumento di ritaglio. Quando si seleziona un’area di un’immagine, il risultato viene restituito e le aree non selezionate vengono eliminate.

Può essere utile in molti modi, poiché eseguire un&#39;operazione di ritaglio con nodi atomici non è così semplice. Soprattutto per la conversione di immagini non quadrate, questo nodo è utile. In tal caso, assicurati di impostare correttamente la risoluzione di input.

Molto importante da capire è che per utilizzare questo nodo con facilità, è necessario fare buon uso della possibilità di visualizzare in anteprima un nodo diverso da quello di cui si stanno modificando i parametri!\
In breve: **fare doppio clic** sul nodo che si sta utilizzando come input per questo (l&#39;immagine originale non ritagliata), quindi **fare un solo clic** sul nodo di ritaglio che segue immediatamente. Puoi quindi modificare il gizmo Ritaglio per adattarlo all’area in cui desideri ritagliare.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Dimensione input</b> <i>0 - 8192</i> | Specificate la risoluzione e le proporzioni dell’immagine. Molto importante per immagini non quadrate. |
| <b>Sfondo</b> <i>(valore colore) / (valore scala di grigi)</i> | Valore uniforme dello sfondo per le superfici non coperte dalla funzione Ritaglio. |
| <b>Trasformazione</b> <i>(Matrice di trasformazione)</i> | Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Normale (solo per la versione a colori)</b> <i>Falso/Vero</i> | Indica se l&#39;input deve essere trattato come una Normalmap. |
