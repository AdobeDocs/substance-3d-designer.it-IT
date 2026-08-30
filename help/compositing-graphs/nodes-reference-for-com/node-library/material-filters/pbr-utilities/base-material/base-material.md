---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: Utilizzare il nodo Materiale di base per creare le proprietà del materiale di base per la creazione di materiali basati fisicamente da zero.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Materiale base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# Materiale base

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/pbr-base-material.png){width="128px"}

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il modo più facile e veloce per creare un materiale multicanale in [Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html). Questo nodo restituisce un materiale completo aggregato in base alle impostazioni e ai valori di colori semplici e uniformi. Questo può quindi essere utilizzato come segnaposto o per rifinire in un materiale complesso.

Il nodo è molto utile quando si creano texture di prop completi e si fondono più materiali. In effetti, si potrebbe iniziare ogni singolo materiale da questo nodo, senza mai aver bisogno di una base di materiale complessa.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
|  | Ingressi opzionali per ogni canale che può essere commutato con gli interruttori in &quot;User Defined Inputs&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Flusso di lavoro PBR</b> <i>Metallo - Rugosità, Specular - Lucentezza</i> | Imposta il modello PBR utilizzato. |
| <b>Predefinito di materiale</b> <i>Personalizzato, Dielettrico, Oro, Argento, Alluminio, Ferro, Rame, Titanio, Nichel, Cobalto, Platino</i> | Scelta rapida da tastiera rapida per la creazione di determinati metalli. Disattiva le opzioni irrilevanti. |
| <b>Colore di base</b> <i>(valore colore)</i> | Tinta unita utilizzata per il Colore di base. |
| <b>Metallico</b> <i>(valore scala di grigi)</i> | Valore solido utilizzato per Metallico. |
| <b>Colore Diffusa</b> <i>(valore colore)</i> | Tinta unita utilizzata per le Diffuse. |
| <b>Specular</b> <i>(valore colore)</i> | Tinta unita utilizzata per lo Specular. |
| <b>Predefiniti Specular</b> <i>Plastica, Legno, Pietra, Mattone, Sabbia, Cemento, Tessuto, Metallo Arrostito, Acqua, Ghiaccio, Vetro</i> | Predefiniti rapidi opzionali per impostare i valori di Specular corretti per PBR. |
| <b>Intervallo Specular</b> <i>0.0 - 1.0</i> | Regola l’intervallo di Specular. |
| <b>Rugosità - Lucidità</b> |  |
| <b>Valore rugosità</b> <i>(valore scala di grigi)</i> | Impostate il valore globale di rugosità di base, se il canale è attivo. |
| <b>Valore Lucentezza</b> <i>(valore scala di grigi)</i> | Tinta unita utilizzata per la Lucentezza, se il canale è attivo. |
| <b>Importo Grungi</b> <i>0.0 - 1.0</i> | Misura in cui l’input opzionale della mappa della Grunge è miscelato a Lucido o Rugosità. |
| <b>Affiancamento Grunge</b> <i>1 - 16</i> | Estendere per affiancare la mappa Grunge facoltativa. |
| <b>Input Grunge personalizzato</b> <i>Falso/Vero</i> | Attiva o disattiva la mappa Grunge personalizzata facoltativa. |
| <b>Normale</b> |  |
| <b>Normale da intensità Height</b> <i>0.0 - 16.0</i> | Facoltativamente, converte la mappa altezza personalizzata in normale e la restituisce come mappa normale del materiale. |
| <b>Height</b> |  |
| <b>Posizione Height</b> <i>0.0 - 1.0</i> | Valore solido utilizzato per l&#39;output del Height. |
| <b>Intervallo Height</b> <i>0.0 - 1.0</i> | Consente di impostare l’influenza della mappa altezza definita dall’utente, se attivata. |
| <b>Mappe definite dall&#39;utente</b> | Attiva o disattiva tutte le mappe definite dall&#39;utente, restituendole invece di qualsiasi valore solido. |
