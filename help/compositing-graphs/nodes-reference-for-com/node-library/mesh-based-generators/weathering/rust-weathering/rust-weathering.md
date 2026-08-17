---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rust-weathering.html"
breadcrumb-title: ''
description: Utilizzate il nodo Temperatura Ruggine per generare pattern di ruggine basati sulla geometria della trama per creare effetti di corrosione del metallo realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rust Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruggine meteorologia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---


# Ruggine meteorologia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rust-weathering.png){width="128px"}

## Ruggine meteorologia

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

## Parametri

### Input

* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Curvatura**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Posizione**: *Input colore*
* **Maschera** : *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;.

### Parametri

* **Canali**
  * Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Avanzate**
  * **Formato normale**: *DirectX, OpenGL*\
    Passa da un formato Normalmap a un altro (inverte il canale verde).
  * **Maschera**: *False/True*\
    Attiva o disattiva l’uso della mappa maschera.
* **Effetto**
  * **Ruggine diffusione**: *0.0 - 1.0*
  * **Smoothness di diffusione**: *0.0 - 1.0*
  * **Scala danni vernice**: *0,0 - 1,0*
  * **Intensità gocce**: *0,0 - 1,0*
  * **Quantità campioni gocce**: *0 - 32*
  * **Smoothness gocce**: *0.0 - 1.0*
* **Fusione**
  * **Intensità diffusione**: *0,0 - 1,0*\
    Intensità di fusione della Diffusione.
  * **Intensità colore di base**: *0,0 - 1,0*\
    Intensità di fusione del colore di base.
  * **Intensità normale**: *0,0 - 32,0*\
    Intensità di fusione del normale.
  * **Intensità Specular**: *0,0 - 1,0*\
    Forza di fusione dello Specular.
  * **Intensità lucidità**: *0,0 - 1,0*\
    Forza di fusione della lucidità.
  * **Intensità rugosità**: *0,0 - 1,0*\
    Forza di fusione della rugosità.
  * **Intensità metallica**: *0,0 - 1,0*\
    Intensità di fusione del metallizzato.
  * **Intensità Occlusione ambiente**: *0,0 - 1,0*\
    Intensità di fusione dell’Occlusione ambiente.
  * **Intensità Height**: *0,0 - 1,0*\
    Forza di fusione del Height.

## Immagini di esempio

![](../../../../../../assets/rust-ex.gif)

</td>
</tr>
</table>
