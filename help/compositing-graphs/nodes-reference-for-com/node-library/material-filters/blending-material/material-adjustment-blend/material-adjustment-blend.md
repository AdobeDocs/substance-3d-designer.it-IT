---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione di regolazione materiale per fondere le regolazioni del materiale tra i materiali per ottimizzare gli effetti compositi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Blend di regolazione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Blend di regolazione materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## Blend di regolazione materiale

**Ingresso:** *Filtri materiale/Fusione*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo consente la regolazione di tutti i canali di un materiale completo, in base a una maschera. ed è stato progettato per rendere più semplice e veloce l&#39;intero flusso di lavoro dei materiali.

È utile per regolare alcuni canali di un materiale (ad esempio, per rendere la diffusione più luminosa e la rugosità più scura) in base alla stessa maschera.

## Parametri

### Input

* **Maschera ID colore**: *Input colore*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Maschera scala di grigi**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Canali**\
  Attiva e disattiva i canali di materiale in questo gruppo, ad esempio quando si utilizzano mappe Specular/lucidità anziché Metallico/Rugosità.\
  Questo attiva e disattiva anche l&#39;aspetto dei gruppi rilevanti del canale.
* **Diffusione**\
  Esegue le operazioni di regolazione sul canale Diffusione, nelle aree definite dalla maschera.
* **Colore di base**\
  Esegue le operazioni di regolazione sul canale Colore di base, nelle aree definite dalla maschera.
* **Normale**
  * **Intensità**: *0,0 - 1,0* Toni più bassi dell&#39;intensità normale
* **Specular**\
  Esegue le operazioni di regolazione sul canale dello Specular, nelle aree definite dalla maschera.
* **Emissivo**\
  Esegue operazioni di regolazione sul canale di emissione, nelle aree definite dalla maschera.
* **Lucentezza**\
  Esegue le operazioni di regolazione sul canale Lucentezza, nelle aree definite dalla maschera.
* **Rugosità**\
  Esegue le operazioni di regolazione sul canale Rugosità, nelle aree definite dalla maschera.
* **Metallico**\
  Esegue le operazioni di regolazione sul canale Metallico, nelle aree definite dalla maschera.
* **Specular level**\
  Esegue le operazioni di regolazione sul canale di Specular level, nelle aree definite dalla maschera.
* **Occlusione ambiente**\
  Esegue le operazioni di regolazione sul canale di Occlusione ambiente, nelle aree definite dalla maschera.
* **Height**\
  Esegue le operazioni di regolazione sul canale del Height, nelle aree definite dalla maschera.
* **Opacità**\
  Esegue le operazioni di regolazione sul canale Opacità, nelle aree definite dalla maschera.
* **Maschera ID colore**: *Falso/Vero* Impostato per utilizzare la Maschera ID colore invece della maschera in scala di grigio.
* **Fuzziness**: *0.01 - 1.0* Se la Maschera ID colore è abilitata, questa impostazione determina la diffusione del colore di selezione dell&#39;ID colore.
* **Colore**: *(valore colore)*Imposta il colore da scegliere dalla mappa ID colore e dalla maschera.
* **Spaziatura interna**: *0.0 - 1.0* Determina il contrasto/le transizioni di fusione della maschera Color ID.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
