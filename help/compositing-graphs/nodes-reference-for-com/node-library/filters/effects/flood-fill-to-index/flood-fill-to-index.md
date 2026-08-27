---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Utilizzare il nodo Flood Fill a indice per riempire le aree con valori di indice per la creazione di pattern numerati ed etichettati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da Flood Fill a indice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# Da Flood Fill a indice

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## Da Flood Fill a indice

**Ingresso:** *Filtri/Effetti*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Da Flood Fill a indice converte ogni cella del Flood Fill in un valore in base al numero di indice, iniziando con 0 nell&#39;angolo superiore sinistro. Può essere usato per restituire tinte in scala di grigio in forma normalizzata (da 0,0 a 1,0, divise per il numero di celle trovato dal Flood Fill) o come valore sbloccato HDR (da 0 a n dove n è il numero di celle).

Inoltre, Flood Fill to Index utilizza [valori](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), restituendo la quantità di forme trovate e la tabella dati interna facoltativa.

### Input

* **Casella Di Testo Flood Fill**: *Input Colore* Mappa Di Input Flood Fill Standard. Obbligatorio.
* **Informazioni speciali sulla forma**: *Input colore* Mappa di Flood Fill aggiuntiva, deve essere esplicitamente abilitata sul nodo del Flood Fill precedente ed essere connessa.

### Parametri

* **Output**: *Normalizzato, Integer* Determinare se l&#39;uscita è compresa nell&#39;intervallo LDR 0-1 o nell&#39;intervallo HDR 0-n.
* **Ignora forma più piccola di**: *0.0 - 1.0* Valore di tolleranza per ignorare le forme piccole.
* **Mostra tabella dati di Flood Fill**: *False/True* Restituisce dati aggiuntivi (di debug) per un utilizzo avanzato.

## Esempi

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
