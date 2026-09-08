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
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# Da Flood Fill a indice

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Da Flood Fill a indice converte ogni cella del Flood Fill in un valore in base al numero di indice, iniziando con 0 nell&#39;angolo superiore sinistro. Può essere usato per restituire tinte in scala di grigio in forma normalizzata (da 0,0 a 1,0, divise per il numero di celle trovato dal Flood Fill) o come valore sbloccato HDR (da 0 a n dove n è il numero di celle).

Inoltre, Flood Fill to Index utilizza [valori](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), restituendo la quantità di forme trovate e la tabella dati interna facoltativa.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Casella Di Testo Flood Fill</b> <i>Input colore</i> | Mappa di input del Flood Fill standard. Obbligatorio. |
| <b>Informazioni sulla forma speciale</b> <i>Input colore</i> | La mappa di Flood Fill aggiuntiva deve essere esplicitamente abilitata sul nodo di Flood Fill precedente ed è necessario che sia connessa. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Output</b> <i>Normalizzato, Intero</i> | Determinare se l’uscita è compresa nell’intervallo LDR 0-1 o nell’intervallo HDR 0-n. |
| <b>Ignora forma più piccola di</b> <i>0.0 - 1.0</i> | Valore di tolleranza per ignorare le forme piccole. |
| <b>Mostra tabella dati di Flood Fill</b> <i>Falso/Vero</i> | Restituisce dati aggiuntivi (di debug) per un utilizzo avanzato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/flood-fill-ex02.jpg" />
        </td>
    </tr>
</table>
