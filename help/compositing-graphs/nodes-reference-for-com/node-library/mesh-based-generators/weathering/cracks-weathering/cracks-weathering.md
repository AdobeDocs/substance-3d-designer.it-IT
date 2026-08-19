---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Usa il nodo Temperatura Crepe per aggiungere pattern di crepe ai materiali in base alla curvatura della trama e ai punti di sollecitazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crepe meteorologiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Crepe meteorologiche

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## Crepe meteorologiche

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Aggiunge un pattern di crepe casuale, con controllo sulle pagine affiancate e sulla profondità.

Assicurati di aver compreso correttamente le [modalità di creazione del collegamento](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) quando lavori con i materiali completi.

## Parametri

### Input

* **Curvatura**: *Input scala di grigi*\
  Mappe infornate o generate utilizzate per effetti interni e mascheratura.
* **Height**: *Input scala di grigi*\
  Mappe infornate o generate utilizzate per effetti interni e mascheratura.
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
  * **Propagazione Crepe**: *0.0 - 1.0* Distanza di diffusione delle crepe. Questo è il controllo principale di questo effetto.
  * **Profondità Crepe**: *0.0 - 1.0* Profondità dell&#39;effetto di crepa. Questo influisce principalmente sul height e leggermente sul thickness visivo.
* **Fusione**
  * Consente di controllare l’entità della fusione dell’effetto in ciascun canale risultante.

## Immagini di esempio

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
