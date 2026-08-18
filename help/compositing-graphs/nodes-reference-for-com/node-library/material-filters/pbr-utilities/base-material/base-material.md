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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# Materiale base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## Materiale base

**Ingresso:** *Filtri materiale/Utility PBR*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Il modo più facile e veloce per creare un materiale multicanale in [Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html). Questo nodo restituisce un materiale completo aggregato in base alle impostazioni e ai valori di colori semplici e uniformi. Questo può quindi essere utilizzato come segnaposto o per rifinire in un materiale complesso.

Il nodo è molto utile quando si creano texture di prop completi e si fondono più materiali. In effetti, si potrebbe iniziare ogni singolo materiale da questo nodo, senza mai aver bisogno di una base di materiale complessa.

## Parametri

### Input

* Ingressi opzionali per ogni canale che può essere commutato con gli interruttori in &quot;User Defined Inputs&quot;.

### Parametri

* **Flusso di lavoro PBR**: *Metallo - Rugosità, Specular - Lucidità* Imposta il modello PBR utilizzato.
* **Predefinito materiale**: *Personalizzato, Dielettrico, Oro, Argento, Alluminio, Ferro, Rame, Titanio, Nichel, Cobalto, Platino* Scelta rapida per creare determinati metalli. Disattiva le opzioni irrilevanti.
* **Colore di base**: *(valore colore)*Colore tinta unita utilizzato per il colore di base.
* **Metallico**: *(valore scala di grigio)*Valore solido utilizzato per Metallico.
* **Colore diffuso**: *(Valore colore)*Colore solido usato per Diffusione.
* **Specular**: *(valore colore)*Tinta unita utilizzata per lo Specular.
* **Predefiniti Specular**: *Plastica, Legno, Pietra, Mattone, Sabbia, Cemento, Tessuto, Rusted Metal, Acqua, Ghiaccio, Vetro* Predefiniti rapidi opzionali per impostare i valori di Specular corretti per PBR.
* **Intervallo Specular**: *0.0 - 1.0* Regola l&#39;intervallo di Specular.
* **Rugosità - Lucidità**
  * **Valore rugosità**: *(valore scala di grigi)*Impostare il valore globale di rugosità di base, se il canale è attivo.
  * **Valore di lucidità**: *(valore in scala di grigio)*Colore tinta unita utilizzato per la lucidità, se il canale è attivo.
  * **Quantità di Grungi**: *0,0 - 1,0* Misura in cui l&#39;input facoltativo della mappa delle Grungi viene miscelato a lucido o rugosità.
  * **Affiancatura Grungi**: *1 - 16* Estendere per affiancare la mappa Grungi facoltativa.
  * **Input Grunge personalizzato**: *False/True* Abilita o disabilita la mappa Grunge personalizzata facoltativa.
* **Normale**
  * **Normale da intensità Height**: *0.0 - 16.0* Converte facoltativamente la mappa altezza personalizzata in normale e la restituisce come mappa normale materiale.
* **Height**
  * **Posizione Height**: *0.0 - 1.0* Valore solido utilizzato per l&#39;output del Height.
  * **Intervallo Height**: *0.0 - 1.0* Imposta l&#39;influenza della mappa di altezza definita dall&#39;utente, se abilitata.
* **Mappe definite dall&#39;utente**
  * Attiva o disattiva tutte le mappe definite dall&#39;utente, restituendole invece di qualsiasi valore solido.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
