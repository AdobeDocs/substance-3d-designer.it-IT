---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Usa il nodo Sfocatura Pendenza per applicare effetti di sfocatura direzionale basati sulle pendenze delle mappe del height per creare l’effetto movimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pendenza sfocatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# Pendenza sfocatura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/slope-blur.png){width="128px"}

![](../../../../../../assets/slope-blur-grayscale.png){width="128px"}

## Pendenza sfocatura (scala di grigi)

**Ingresso:** *Filtri/Sfocature*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Effettua una sfocatura avanzata di alta qualità quando l’Anisotropia/direzione è guidata da una &quot;Mappa Pendenza&quot; in scala di grigi. Immaginalo come l’effetto Sfocatura Pendenza che segue le pendenze della Mappa Pendenza come se fosse una Heightmap, simile a [Alterazione direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (su cui si basa internamente).

Questa è una delle sfocature più interessanti e potenti di Designer. Può essere utilizzato per ottenere alcuni effetti molto interessanti e inaspettati, come scheggiatura e bordi di tempo o spalmatura e perdita di dirt o ruggine.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Pendenza sfocatura&quot; per gli input di colore o &quot;Pendenza sfocatura scala di grigi&quot; per gli input di scala di grigi.

## Parametri

### Input

* **Pendenza**: *Input in scala di grigi* Mappa Pendenza per l&#39;angolo di unità dell&#39;anisotropia. Dovrebbero idealmente contenere sfumature inclinate; transizioni dure e nitide non funzioneranno bene!

### Parametri

* **Campioni**: *0 - 32* La quantità di campioni influisce sulla qualità a scapito della velocità.
* **Intensità**: *0,0 - 16,0*\
  Entità o intensità della sfocatura.
* **Modalità**: *Sfocatura, Min, Max*|\
  Metodo di fusione per le passate di sfocatura successive. &quot;Sfocatura&quot; si comporta in modo più simile a una [Sfocatura anisotropa](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) standard, mentre Min &quot;mangia via&quot; le aree esistenti e Max &quot;macchia&quot; le aree bianche.

## Immagini di esempio

![](../../../../../../assets/slopeblur01.gif)

![](../../../../../../assets/slopeblur02.gif)

</td>
</tr>
</table>
