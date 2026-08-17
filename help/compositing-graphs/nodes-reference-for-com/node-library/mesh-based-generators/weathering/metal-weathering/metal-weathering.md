---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Utilizzate il nodo Metallo meteorologico per aggiungere effetti di corrosione e ruggine realistici ai materiali metallici in base alla geometria della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metallo meteorologico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---


# Metallo meteorologico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

## Metallo meteorologico

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

## Parametri

### Input

* **WS normale**: *Input colore*\
  Baked World Space Normalmap utilizzata per effetti interni e mascheratura.
* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Maschera** : *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;.

### Parametri

* **Canali**
  * Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Avanzate**
  * **Formato normale**: *Direct X, Open GL*\
    Passa da un formato Normalmap a un altro (inverte il canale verde).
  * **Maschera**: *False/True*\
    Attiva o disattiva l’uso della mappa maschera.
* **Effetto**
  * **Dust**: *0.0 - 1.0*
  * **Irritazione**: *0,0 - 1,0*
  * **Indossamento bordi**: *0.0 - 1.0*
  * **Sfumatura pittura**: *0,0 - 1,0*
  * **Ruggine**: *0.0 - 1.0*
  * **Ruggine peeling**: *0,0 - 1,0*
  * **Ruggine verdigris**: *Ruggine, verdigris*
  * **Scala Crepe pittura**: *1.0 - 16.0*
  * **Intensità alterazione Crepe pittura**: *0.0 - 1.0*
  * **Scala Scratches bordi netti**: *1.0 - 32.0*
  * **Intensità alterazione bordi netti**: *0,0 - 1,0* Scratches
  * **Colore metallo grezzo**: *(valore colore)*
  * **Colore Specular metallo grezzo**: *(valore colore)*
  * **Valore lucidità metallo grezzo**: *(valore scala di grigi)*
  * **Valore rugosità metallo grezzo**: *(valore scala di grigi)*
* **Fusione**
  * **Intensità diffusione**: *0,0 - 1,0*\
    Intensità di fusione della Diffusione.
  * **Intensità colore di base**: *0,0 - 1,0*\
    Intensità di fusione del colore di base.
  * **Intensità normale**: *0,0 - 64,0*\
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

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
