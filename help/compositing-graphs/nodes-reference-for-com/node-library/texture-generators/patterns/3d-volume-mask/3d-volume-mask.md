---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Utilizzate il nodo Maschera volume 3D per creare maschere volumetriche basate sulla posizione 3D per effetti di materiale avanzati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maschera volume 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# Maschera volume 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**Ingresso:** Generator*/Pattern*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Maschera volume 3D** genera una rappresentazione di una *forma primitiva* basata sulla mappa di input **Posizione**.

</td>
</tr>
</table>

## Parametri

### Input

* **Posizione** *Colore*\
  La mappa che descrive le *coordinate dello spazio 3D* in cui è rappresentata la primitiva.\
  Le coordinate **X/Y/Z** sono mappate rispettivamente ai canali **R/G/B**.

### Parametri

* **Forma** *Intero*\
  La forma primitiva che dovrebbe essere rappresentata:
  * *Cubo*- *Cilindro*- *Sfera*
* **Scala** *Mobile*\
  Definisce la scala *globale* del primitivo, applicata *in modo uniforme* su tutti gli assi.
* **Dimensioni** *Float3*\
  Definisce le dimensioni della forma su ciascun asse.
* **Input posizione** *Numero intero*\
  Metodo di *rappresentazione dello spazio* tramite l&#39;input **Posizione**:
  * *Posizione UV*: utilizzate una *mappa UV*. Le coordinate X/Y (U/V) sono associate rispettivamente ai canali R/G. Si presume che l&#39;asse Z sia il vettore *ortogonale in avanti*.
  * *Posizione nello spazio globale*: utilizzate una *mappa di posizione* per mappare l&#39;elemento di base nello spazio 3D. Le coordinate X/Y/Z sono associate rispettivamente ai canali R/G/B.
* **Posizione UV** *Float2*\
  Posizione del primitivo nello spazio UV.\
  *Nota*: questo parametro è disponibile solo quando **Input posizione** è impostato su *Posizione UV*.
* **Posizione** *Float3*\
  La posizione del primitivo nello spazio mondiale.\
  *Nota*: questo parametro è disponibile solo quando **Position Input** è impostato su *World Space Position*.
* **Rotazione** *Float3*\
  Definisce la rotazione della forma nello spazio mondo.
* **Larghezza sfumatura** *Mobile*\
  Regola la larghezza della *sfumatura di dissolvenza* dalla superficie del primitivo verso l&#39;interno.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>
