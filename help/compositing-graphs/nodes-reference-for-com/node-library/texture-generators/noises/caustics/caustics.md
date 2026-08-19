---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilizzate il nodo Riflessioni caustiche per generare pattern di luce caustica per creare effetti di luce subacquea e rifrattiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Riflessioni caustiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Riflessioni caustiche

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

**Ingresso:** *Generatori Di Texture**/Rumori*

**Complesso**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Genera caustiche proiettate in base a una mappa del height e a una direzione della luce.Disponibile sia nella versione in scala di grigio che in quella a colori, le differenze sono lievi, ma la versione a colori aggiunge effetti di dispersione del colore. La luce viene proiettata da un singolo punto, non viene utilizzata alcuna mappa di ambiente.

</td>
</tr>
</table>

## Parametri

* **Spazio colore di output**: *Raw, sRGB*\
  Imposta lo spazio colore di output.
* **Dimensioni griglia Photon**: *Automatico, 512, 1024, 2048, 4096*\
  Imposta la qualità regolando le dimensioni della griglia, ma per impostazione predefinita corrisponde all’input. Può essere utilizzato per velocizzare i calcoli.
* **Scala Height Superficie**: *0,0 - 1,0*\
  Moltiplicatore per determinare come viene interpretato il height.
* **Posizione Height Superficie**: *0,0 - 1,0*\
  Impostate la distanza della superficie di rifrazione rispetto alla proiezione.
* **Superficie IOR**: *1,0 - 2,0*\
  Impostate l&#39;indice di rifrazione: nella versione a colori questa opzione aggiunge una maggiore dispersione di colore.
* **Dimensioni fotone**: *1,0 - 50,0*\
  La dimensione del fotone influisce sulla nitidezza dell’effetto.
* **Dispersione**: *0.0 - 0.01 (solo versione a colori)*\
  Modificate solo la dispersione dei colori. Non visibile quando lo IOR è basso.
* **Variazione**: *0.0 - 1.0*\
  Aggiungete la variazione irregolare alle particelle di fotoni proiettati.
* **Posizione chiara**:\
  Sposta la luce. Eseguito anche tramite un gizmo nella vista 2D.
* **Colore di sfondo**: *(valore colore) (solo versione colore)*\
  Modifica il colore di sfondo. Limitato al nero nella versione in scala di grigi.
* **Non square expansion**: *Falso/Vero*\
  Abilita la compensazione di schiaccia e allunga con rapporti non quadrati.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-caustics-grayscale-1.png" width="300px"/></div> |
| --- |
|  |
