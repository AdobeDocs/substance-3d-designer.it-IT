---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Utilizza il nodo Disturbo simplex 3D per generare pattern di disturbo simplex 3D per creare texture volumetriche uniformi e naturali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Disturbo simplex 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Disturbo simplex 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## Disturbo simplex 3D

**Ingresso:** *Generatori Di Texture**/Rumori*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera un disturbo procedurale quando una mappa di posizione al forno è collegata allo slot di input. È destinato all’uso solo con il motore GPU.\
Simile a [Disturbo Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), ma più semplice e veloce, nei casi in cui le prestazioni e la velocità contano.

Questo disturbo può essere testato con [Cubo 3D GBuffer](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

## Parametri

* **Scala**: *0,0 - 64,0*\
  Impostate la scala globale per l’effetto.
* **Dimensioni**: *0,0 - 2,0* Eseguire separatamente il ridimensionamento non uniforme sugli assi X, Y e Z.

## Immagini di esempio

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
