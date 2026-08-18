---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Utilizza il nodo Generatore Scratches per creare modelli di graffi procedurali per aggiungere usura e danni ai materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore Scratches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Generatore Scratches

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Generatore Scratches (Normale)

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

In questo modo si creano graffi casuali con molte opzioni di personalizzazione, ad esempio per impostare direzione, pagine affiancate e distorsione.

Esiste una versione speciale di Generatore di Scratches, Normale di Generatore di Scratches, che genera Normalmap basate sulla profondità di questi graffi. La maggior parte delle opzioni è esattamente la stessa, ma ha alcuni parametri aggiuntivi chiaramente contrassegnati per le impostazioni Normale (vedi di seguito).

## Parametri

* **Numero spline**: *1 - 512* Quantità di graffi (spline) da inserire.
* **Numero massimo di segmenti per spline**: *2 - 256* Quantità di segmenti/suddivisioni sulla lunghezza di un graffio. Porta a curve e distorsioni più uniformi. L’effetto è più evidente con valori di Distorsione più alti.
* **Rotazione spline**: *0.0 - 1.0* Rotazione uniforme di tutte le spline per orientarle in una direzione.
* **Rotazione spline casuale**: *0.0 - 1.0* Variazione dell&#39;angolo, ruota casualmente ogni spline.
* **Scala spline**: *0.0 - 1.0* Ridimensiona in modo uniforme tutte le spline.
* **Scala spline casuale**: *0,0 - 1,0* Ridimensiona ogni spline in modo casuale singolarmente.
* **Distorsione spline**: *0.0 - 1.0* Livello distorsione uniforme su tutte le spline.
* **Distorsione spline casuale**: *0.0 - 1.0* Rende casuale il livello di distorsione di ogni spline singolarmente.
* **Frequenza Distorsione spline**: *0.0 - 1.0* Imposta la frequenza della distorsione e controlla la scala dei dettagli della distorsione.
* **Larghezza spline**: *0.0 - 2.0* Imposta la larghezza di tutte le spline in modo uniforme.
* **Larghezza spline casuale**: *0.0 - 1.0* Rende casuale la larghezza della spline di ogni spline singolarmente.
* **Posizione spline casuale**: *0,0 - 1,0* Rende casuale la posizione di ogni spline singolarmente. Più è basso questo valore, più spline si raggrupperanno al centro dell&#39;area di lavoro. Può essere utilizzato per creare macchie di graffi.
* **Imposta larghezza spline in px**: *False/True* Determina le unità utilizzate per le impostazioni di larghezza spline.
* **Luminanza casuale (solo versione in scala di grigio)**: *0.0 - 1.0* Rende casuale la luminanza di ogni spline singolarmente.
* **Intensità normale (solo versione normale)**: *0.0 - 1.0* Imposta l&#39;intensità dell&#39;effetto Normale per ogni spline a livello globale.
* **&#x200B; Intensità normale &#x200B;** casuale (solo versione normale)**&#x200B;**: *0.0 - 1.0*Rende casuale l&#39;intensità normale per ogni spline singolarmente.
* **&#x200B; Formato normale &#x200B;**(solo versione normale)**&#x200B;**: *DirectX, OpenGL*\
  Passa da un formato Normalmap a un altro (inverte il canale verde).
* **Modalità dissolvenza**: *Nessuna, Inizio, Fine, Inizio + Fine* Determina se e in quale direzione le spline vengono dissolte.
* **Lunghezza dissolvenza**: *0.0 - 1.0* Imposta la lunghezza dell&#39;effetto di dissolvenza, se abilitato sopra.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
