---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Utilizzare il nodo Copertina Snow per aggiungere effetti di accumulo di neve ai materiali in base all'angolo e alla posizione della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Copertina Snow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Copertina Snow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Copertina Snow

**Ingresso:** *Filtri/Effetti Materiale*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Effetto all-in-one per aggiungere un accumulo di neve su un materiale completo. Si affida fortemente a una buona mappa di altezza di alta qualità, come ad esempio da una fotoscan. Il risultato deve essere corretto per PBR.

## Parametri

### Input

* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Canali**\
  Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Snow fresco**: *0.0 - 1.0* Imposta la quantità di neve nelle aree in rilievo. Il risultato è legato al parametro Snow fuso.
* **Snow sciolto**: *0.0 - 1.0* Imposta la quantità di neve sciolta negli angoli inferiori.
* **Compilazione**: *0.0 - 1.0* Influisce principalmente sull&#39;output del Height e determina l&#39;effetto di accumulo del height.
* **Smoothness**: *0.0 - 1.0* Imposta l&#39;attenuazione dei dettagli del height tramite l&#39;accumulo di neve.
* **Intensità fiocchi**: *0.0 - 1.0* Influisce principalmente su Normalmap, l&#39;intensità dei dettagli del fiocco.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
