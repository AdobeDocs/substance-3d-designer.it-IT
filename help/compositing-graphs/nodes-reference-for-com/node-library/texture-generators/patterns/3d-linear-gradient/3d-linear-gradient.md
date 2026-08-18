---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Usa il nodo del 3D linear gradient per creare sfumature lineari basate sulla posizione del mondo 3D per effetti spaziali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D linear gradient

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Crea una sfumatura volumetrica in base alla mappa Posizione di input. Genera efficacemente una transizione dal nero al bianco tra 2 punti nello spazio 3D. Destinato all’uso esclusivo con il motore GPU.

Consultate anche [Maschera volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) per un effetto simile.

## Parametri

* **Modalità posizione punti**: *Posizioni UV, Posizioni nello spazio globale* Scegliete se i punti sfumatura funzionano nello spazio UV (funziona meglio quando li impostate nella vista 2D) o nelle coordinate 3D, se desiderate inserire manualmente una posizione esatta.
* **Punto 1**:\
  Punto iniziale della sfumatura. Può essere 2D o 3D Coordinate in base alla Modalità posizione.
* **Punto 2**:\
  Punto finale della sfumatura. Può essere 2D o 3D Coordinate in base alla Modalità posizione.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.

## Immagini di esempio

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
