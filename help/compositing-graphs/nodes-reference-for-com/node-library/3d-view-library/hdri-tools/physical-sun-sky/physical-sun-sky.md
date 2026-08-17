---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Utilizza il nodo SunSky fisico per generare ambienti di illuminazione del sole e del cielo fisicamente accurati per un'anteprima realistica del materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SunSky fisico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Sole fisico/Cielo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## Sole fisico/Cielo

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Implementazione fisica di Sole e Cielo basata sul modello Hosek-Wikie skylight. Fornisce una base eccellente per un HDRI artificiale.

## Parametri

* **Posizione Sole**:\
  intervallo = [0,1]x[0,1] (angoli longitudine-latitudine)
* **Turbidità**: *1.0 - 10.0*\
  La torbidità varia da 1 a 10
* **Albedo**: *0.0 - 1.0*\
  L’Albedo varia da 0 a 1.
* **Colore terreno**: *(valore colore)*\
  Colore del piano terreno.
* **Esposizione (EV)**: *-1,0 - 4,0*\
  Valore di esposizione dell’output risultante.
* **Dimensioni Sun**: *0,0 - 4,0*\
  Scala del Sole, qualsiasi valore diverso da 1 non è fisicamente corretto. Il valore ha effetti sottili.
* **Intensità sole**: *0,0 - 1,0*\
  Intensità del disco solare. Il disco Sun è piuttosto piccolo, quindi l&#39;effetto non è immediatamente visibile.
* **Intensità cielo**: *0,0 - 1,0* Intensità cielo. Influisce anche sulla luce del sole nel cielo, non sul disco stesso.

## Immagini di esempio

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
