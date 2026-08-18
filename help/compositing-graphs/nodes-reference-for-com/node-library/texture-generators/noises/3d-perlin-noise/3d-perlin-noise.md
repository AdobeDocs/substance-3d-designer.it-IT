---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo di Perlin 3D per generare pattern di disturbo di Perlin uniformi in uno spazio 3D per creare texture volumetriche dall'aspetto naturale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Disturbo Perlin 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Disturbo Perlin 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**Ingresso:** *Generatori Di Texture**/Rumori*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Disturbo di Perlin 3D** genera un disturbo di Perlin nello spazio 3D in base all&#39;input **Mappa posizione**.

Questo nodo può essere testato con [Cubo 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con *motore GPU* (ad esempio **Direct3D** o **OpenGL**). Vai a **Strumenti > Cambia motore...** oppure premi il tasto **F9** per selezionare il motore desiderato.

</td>
</tr>
</table>

## Parametri

* **Inverti** *Booleano*\
  Inverte l’immagine di output.
* **Scala** *Mobile*\
  Controlla la scala del disturbo di Perlin 3D.
* **Dimensioni** *Float3*\
  Controlla la dimensione del disturbo di Perlin 3D sugli assi **X**, **Y** e **Z**. I valori non uniformi producono un effetto *allungamento o schiacciamento*.
* **Scostamento** *Float3*\
  Applica uno scostamento alla *posizione* del disturbo di Perlin 3D sugli assi **X**, **Y** e **Z**.
* **Intensità Distorsione** *Mobile*\
  Controlla l’intensità di un *effetto di alterazione* applicato al disturbo di Perlin 3D.
* **Moltiplicatore scala Distorsione** *Mobile*\
  Controlla la scala del *pattern di deformazione* utilizzato nell&#39;effetto di alterazione controllato dall&#39;**intensità della Distorsione**.
* **Previsione** *Mobile*\
  Applica un *offset* al valore di *luminanza* della linea di base per la distribuzione del valore di disturbo Perlin 3D.
* **Contrasto** *Mobile*\
  Regola il contrasto del disturbo 3D di Perlin.
* **Assoluto** *Booleano*\
  Usa valori assoluti nel disturbo di Perlin 3D. In questo modo *viene invertita* la distribuzione dei valori *inferiori a 0,5*.
* **Abilita Porzione** *Booleano*\
  Regola il disturbo di Perlin 3D in modo che il relativo pattern *si ripeta* sugli assi X, Y e Z.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
