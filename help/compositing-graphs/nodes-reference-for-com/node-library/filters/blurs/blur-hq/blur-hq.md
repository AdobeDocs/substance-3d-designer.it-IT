---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Usa il nodo Sfoca HQ per applicare effetti di sfocatura di alta qualità alle texture, per creare risultati di sfocatura uniformi e professionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# Sfocatura HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/blur-hq-1.png){width="128px"}

![](../../../../../../assets/blur-hq-grayscale.png){width="128px"}

## Sfocatura HQ (scala di grigi)

**Ingresso:** *Filtri/Sfocature*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Consente di eseguire una sfocatura gaussiana di alta qualità sul risultato. Qualità molto migliore rispetto a [la sfocatura standard della scatola atomica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)[.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Blur HQ&quot; per gli input di colore o &quot;Blur HQ Grayscale&quot; per gli input di scala di grigio.

## Parametri

* **Intensità**: *0,0 - 16,0*\
  Intensità (raggio) della sfocatura. Più alto è questo valore, maggiore sarà la sfocatura.
* **Qualità**: *0 - 1* Aumenta la quantità di campionamento interno per una qualità ancora maggiore, a velocità di calcolo ridotta.

## Immagini di esempio

![](../../../../../../assets/hqblur-example.gif)

</td>
</tr>
</table>
