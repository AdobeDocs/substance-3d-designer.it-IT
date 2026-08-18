---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Utilizzate il nodo Miscelatore dati mesh materiale (Material Mesh Data Blender) per fondere i dati della mesh del materiale e creare transizioni uniformi tra le diverse zone materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Miscelatore dati mesh materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Miscelatore dati mesh materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## Miscelatore dati mesh materiale

**Ingresso:** *Generatori Basati Su Trama**/Utility*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo ha lo scopo di semplificare notevolmente l&#39;aggiunta di dettagli in base ai dati elaborati. Viene fornito con molti cursori per modificare un materiale completo di input, basato su qualsiasi e tutte le mappe con baking come input. Sperimenta, dato che ci sono molte opzioni.

È utile ad esempio per aggiungere l’evidenziazione dei bordi in base alla curvatura o ad altre mappe, eseguire la fusione in alcuni oggetti AO con Diffusione/Colore di base, aggiungere Occlusioni di Specular basate su Curvatura e/o AO, ecc.

## Parametri

### Input

* **Input materiale completo (gruppo &quot;Materiale&quot;):** set completo di mappe materiale.\
  Questi elementi vengono modificati da questo nodo e quindi restituiti come output.
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Height**: *Input scala di grigi*
* **Normale**: *Input colore*
* **Colore vertice**: *Input colore*
* **Spazio Mondiale Normale**: *Input Colore*

### Parametri

* **Canali**
  * Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. Influisce sulla disponibilità dei parametri seguenti.
* **Mappe con baking**
  * Indica se utilizzare o meno le mappe con baking elencate per i calcoli. Influisce sulla disponibilità dei parametri seguenti.
* **Diffusione AO**: *0.0 - 1.0* Quantità di Occlusione ambiente da fondere nella diffusione.
* **Bordi Netti Diffusi**: 0,0 - 1,0\
  Quantità della mappa di curvatura da fondere con Diffusione.
* **Colore Diffuso Dal Colore Vertice**: 0,0 - 1,0\
  Quantità del Color Bake Vertice da fondere con Diffusione.
* **Pre-illuminazione diffusa**: 0,0 - 1,0\
  Quantità di (falsa) pre-illuminazione, in base ai World Space Normals.
* **Bilanciamento Diffusione Illuminazione Cartone Animato**: 0,0 - 1,0\
  Si sposta tra un’illuminazione realistica e in stile cartone animato per Diffusione.
* **Livelli di pre-illuminazione per cartoni animati diffusi**: 0 - 10\
  Controlla l’aspetto dei calcoli di illuminazione per i cartoni animati.
* **Profili fumetto diffusi**: 0,0 - 1,0\
  Controlla l’aspetto dei calcoli di illuminazione per i cartoni animati.
* **Colore base AO**: 0,0 - 1,0\
  Quantità di Occlusione ambiente da fondere con il colore di base.
* **Bordi netti colore di base**: 0,0 - 1,0\
  Quantità della mappa di curvatura da fondere con il colore di base.
* **Colore Di Base Da Colore Vertice**: 0,0 - 1,0\
  Quantità del colore Vertice da unire al colore di base.
* **Intensità materiale normale**: 0,0 - 1,0\
  Intensità di fusione della Normalmap cotta (tangente).
* **SpecularAO**: 0,0 - 1,0\
  Forza di fusione dell’AO nello Specular.
* **Bordi netti con Specular chiaro**: 0,0 - 1,0\
  Intensità di fusione della curvatura nello Specular.
* **Contorni di Specular animato**: 0,0 - 1,0\
  Intensità di fusione di un effetto Specular bordo-contorno, in base alla curvatura.
* **Lucentezza Bordi Netti Scuri**: 0,0 - 1,0\
  Intensità di fusione della curvatura nel livello di lucidità.
* **Rugosità Bordi Netti E Luminosi**: 0,0 - 1,0\
  Forza di fusione della curvatura nella rugosità.
* **Contorni fumetto rugosità**: 0,0 - 1,0\
  Intensità di fusione di un effetto bordo rugosità fumetto, in base alla curvatura.
* **Bordi Netti Luminosi Metallici**: 0,0 - 1,0\
  Intensità di fusione della curvatura nel metallizzato.
* **Contorni metallizzati dei cartoni animati**: 0,0 - 1,0\
  Intensità di fusione di un effetto bordo metallico del cartone animato, in base alla curvatura.
* **Intensità materiale AO**: 0,0 - 1,0\
  Intensità di fusione di mappa con baking AO con AO generato dal materiale, in che misura combinare entrambe le mappe AO.
* **Intensità materiale Height**: 0,0 - 1,0\
  Intensità di fusione del Height mappa con baking con il Height generato dal materiale, in che misura combinare entrambe le mappe altezza.
* **Tipo di fusione materiale Height**: rinforza, interpolazione\
  Metodo fusione per combinare entrambe le mappe di altezza.

## Immagini di esempio

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
