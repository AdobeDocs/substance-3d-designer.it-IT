---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione materiale per fondere interi materiali utilizzando maschere per creare effetti di materiale composito.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Fusione materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## Fusione materiale

**Ingresso:** *Filtri materiale/Fusione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Material Blend è l&#39;equivalente materiale completo multicanale di [atomic Blend Node](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Si fonde tra due materiali completi (tutti i possibili canali) in base a una maschera in scala di grigio o facoltativamente in base a un singolo colore da una Maschera ID colore.

Questo nodo è utile se desideri unire due materiali e avere una mappa in scala di grigio ma senza una selezione completa di ID colore. Se disponi di un forno Color ID e desideri fondere più di due materiali, ti consigliamo di utilizzare [Fusione multismateriale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

## Parametri

### Input

* **ColorID**: *Input colore*\
  Mappa ID colore al forno opzionale.
* **Maschera scala di grigi**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Canali**
  * Attivate e disattivate i canali di materiale in questo gruppo quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Diffusione**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Colore di base**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Normale**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
* **Specular**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Emissivo**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Lucentezza**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Rugosità**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Metallico**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Specular level**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Occlusione ambiente**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Height**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Opacità**
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo
  * **Metodo Di Fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Scambia*
* **Maschera ID colore**: *Falso/Vero* Usa Maschera ID colore invece di maschera in scala di grigio. Tieni presente che questo è solo per un colore!
* **Colore**: *(valore colore)*Quale colore scegliere e convertire in bianco.
* **Sfocatura**: *0.01 - 1.0* La misura in cui il colore scelto si fonde con le aree adiacenti.
* **Spaziatura interna**: *0.0 - 1.0* Contrasto di transizione del colore selezionato.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
