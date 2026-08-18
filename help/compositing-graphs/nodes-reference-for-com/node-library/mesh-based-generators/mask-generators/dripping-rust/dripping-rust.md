---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilizzate il nodo Ruggine di gocciolamento (Dripping) per generare serie di gocce di ruggine in base alla geometria della trama e alla direzione della gravità.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruggine gocciolante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 1%

---


# Ruggine gocciolante

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

## Ruggine gocciolante

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta scaglie e chiazze di ruggine, con perdite che scorrono.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappa generata o al forno per facilitare il posizionamento della ruggine.
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa generata o al forno per facilitare il posizionamento della ruggine.
* **Posizione**: *Input scala di grigi*\
  Mappa cotta o generata per le direzioni di goccia.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Diffusione Ruggine**: *0.0 - 1.0* Controllo principale per la quantità di ruggine.
* **Contrasto Ruggine**: *0.0 - 1.0* Imposta la quantità di contrasto nelle macchie di ruggine generate (non influisce sulle gocce).
* **Smoothness di diffusione**: *0,0 - 1,0* Quantità di effetto di sfocatura/macchie da applicare alle ruggine.
* **Intensità gocce**: *0.0 - 1.0* Imposta l&#39;intensità e la lunghezza delle gocce dai frammenti.
* **Smoothness gocce**: *0,0 - 1,0* Quantità di sfocatura e attenuazione da applicare alle gocce.
* **Quantità campioni gocce**: *0 - 32* Imposta il livello di qualità (passaggi) per l&#39;effetto gocce. Ha un leggero effetto sulla velocità.

## Immagini di esempio

![](../../../../../../assets/dripping-rust-ex3.gif)

</td>
</tr>
</table>
