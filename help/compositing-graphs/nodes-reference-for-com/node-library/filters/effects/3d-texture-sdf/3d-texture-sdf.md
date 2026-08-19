---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Utilizza il nodo SDF Texture 3D per generare texture dei campi distanza con segno dai dati 3D per creare forme ed effetti uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SDF texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# SDF texture 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**Ingresso:** *Filtro/Effetto*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **SDF** della texture 3D genera il *campo distanza con segno* di una forma dalla maschera *texture 3D* dell&#39;input **&#x200B;**&#x200B;che rappresenta le sezioni del *volume* della forma.

</td>
</tr>
</table>

## Parametri

### Input

* **Input maschera** *Scala di grigi*\
  La maschera *texture 3D* che rappresenta le sezioni del *volume* di una forma.

### Parametri

* **Soglia** *Mobile*\
  Quando il volume della forma è descritto da una *sfumatura di dissolvenza*, imposta il valore della sfumatura in base al quale la *superficie* della forma viene *rilevata*.
* **Output** *Intero*\
  Tipo di campo distanza che deve essere generato:
  * *Campo distanza*: genera un campo distanza che descrive le distanze *esterne* della forma.
  * *Signed distance field*: genera un campo distanza che descrive le distanze *esterne* (positive) e *interne* (negative) della forma.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
