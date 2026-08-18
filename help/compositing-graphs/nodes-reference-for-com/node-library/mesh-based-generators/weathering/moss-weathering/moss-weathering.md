---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: Usa il nodo Meteorizzazione Moss per aggiungere pattern di crescita del muschio ai materiali in base alla curvatura e alla posizione della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Moss Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---


# Moss Weathering

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/moss-weathering.png){width="128px"}

## Moss Weathering

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Genera un effetto muschio ingrandito, con un singolo controllo per Propagazione.

Questo effetto funziona meglio con una mappa di posizione dello spazio mondiale e una mappa dell&#39;altezza aggiuntiva. Anche se questo non è un requisito esatto, conferisce all&#39;effetto un posizionamento più credibile.

Assicurati di aver compreso correttamente le [modalità di creazione del collegamento](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) quando lavori con i materiali completi.

## Parametri

### Input

* **Posizione**: *Input colore*\
  Posizione dello spazio mondiale baked.
* **Height**: *Input scala di grigi*\
  Input aggiuntivo Heightmap.
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
  * **Propagazione Moss**: *0.0 - 1.0* Imposta la diffusione del muschio. Cresce a intervalli che vanno da una leggera copertura a muschio spesso e scuro.
* **Fusione**
  * **Intensità diffusione**: *0,0 - 1,0*\
    Intensità di fusione della Diffusione.
  * **Intensità colore di base**: *0,0 - 1,0*\
    Intensità di fusione del colore di base.
  * **Intensità normale**: *0,0 - 1,0*\
    Intensità di fusione del normale.
  * **Intensità Specular**: *0,0 - 1,0*\
    Forza di fusione dello Specular.
  * **Intensità lucidità**: *0,0 - 1,0*\
    Forza di fusione della lucidità.
  * **Intensità rugosità**: *0,0 - 1,0*\
    Forza di fusione della rugosità.
  * **Intensità Occlusione ambiente**: *0,0 - 1,0*\
    Intensità di fusione dell’Occlusione ambiente.
  * **Intensità Height**: *0,0 - 1,0*\
    Forza di fusione del Height.

## Immagini di esempio

![](../../../../../../assets/moss-ex.gif)

</td>
</tr>
</table>
