---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sfocatura anisotropa per applicare effetti di sfocatura direzionale per creare effetti di sfocatura movimento e striatura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura anisotropa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 1%

---


# Sfocatura anisotropa

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/anisotropic-blur-grayscale.png){width="128px"}

![](../../../../../../assets/anisotropic-blur.png){width="128px"}

## Sfocatura Anisotropa (Scala Di Grigi)

**Ingresso:** *Filtri/Sfocature*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Esegue una [sfocatura direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) di alta qualità, con alcune impostazioni per personalizzare l&#39;aspetto. Detto anche &quot;effetto movimento&quot;.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Sfocatura anisotropa&quot; per gli input di colore o &quot;Scala di grigi Sfocatura anisotropa&quot; per gli input di scala di grigi.

## Parametri

* **Intensità**: *0.0 - 16.0* Intensità (raggio) della sfocatura. Più alto è questo valore, maggiore sarà la sfocatura.
* **Anisotropia**: *0.0 - 1.0* Direzione della sfocatura. Impostare questo valore su 0,0 equivale a eseguire una sfocatura normale.
* **Angolo**: *0.0 - 1.0* Imposta l’angolo per la direzione di sfocatura.
* **Qualità**: *0 - 1* Consente di passare internamente da una sfocatura a [effetto box](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) a una sfocatura HQ. Scambia in velocità per qualità.

## Immagini di esempio

![](../../../../../../assets/aniso-blur-example.gif)

</td>
</tr>
</table>
