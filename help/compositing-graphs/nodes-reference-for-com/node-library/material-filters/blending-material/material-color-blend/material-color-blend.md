---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione colore materiale per fondere i canali di colore tra i materiali per creare effetti di materiale composito.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione colore materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Fusione colore materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## Fusione colore materiale

**Ingresso:** *Filtri materiale/Fusione*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo consente di regolare un materiale completo multicanale fondendo i colori uniformi in alto. Questa è la differenza principale con [Material Adjustment Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), che consente solo regolazioni di tipo [Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) ai canali, mentre questo nodo utilizza regolazioni di tipo [Fusione](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) con un colore a tinta unita.

Questo nodo è particolarmente utile quando si desidera introdurre un suggerimento di colore piatto in Diffusione o Colore base, oppure quando si desidera &quot;appiattire&quot; altri canali utilizzando un valore di colore a tinta unita impostato.

## Parametri

### Input

* **ColorID**: *Input colore*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Maschera scala di grigi**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Canali**
  * Attivate e disattivate i canali di materiale in questo gruppo quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Diffusione**
  * **Colore**: *(valore colore)*Quale valore di colore fondere sopra il canale diffuso.
  * **Opacità**: *0,0 - 1,0*\
    Fusione dell’opacità tra primo piano e sfondo.
  * **Metodo fusione**: *Normale, Aggiungi, Sottrai, Moltiplica, Aggiungi/Sotto, Max, Min, Cambia* Metodo fusione da utilizzare nell&#39;operazione.
* **Colore di base**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Normale**
  * **Origine**: *Height, Maschera*
  * **Metodo fusione**: *Combina, Fusione*
  * **Intensità Height**: *0,0 - 1,0*
  * **Opacità Height**: *0,0 - 1,0*
  * **Formato**: *DirectX, OpenGL*
* **Specular**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Emissivo**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Lucentezza**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Rugosità**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Metallico**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Specular level**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Occlusione ambiente**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Height**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Opacità**
  * Consente di fondere un colore in tinta unita sulla parte superiore del canale con le opzioni del gruppo Diffusione.
* **Maschera ID colore**: *Falso/Vero* Usa Maschera ID colore invece di maschera in scala di grigio. Tieni presente che questo è solo per un colore!\
  Abilita tutte le opzioni seguenti.
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
