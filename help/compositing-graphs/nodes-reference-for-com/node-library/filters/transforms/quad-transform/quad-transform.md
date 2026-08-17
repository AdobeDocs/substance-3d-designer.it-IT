---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasformazione quadrupla per applicare trasformazioni quadrilaterali alle texture per la correzione prospettica e l’alterazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione quadrupla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---


# Trasformazione quadrupla

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/quad-transform-grayscale.png){width="128px"}

![](../../../../../../assets/quad-transform.png){width="128px"}

## Trasformazione quadrupla (scala di grigi)

**Entrata:** *Filtri/Trasformazioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo di trasformazione speciale che consente la trasformazione di una forma quadrupla attraverso l&#39;interazione con i relativi punti d&#39;angolo. Consente trasformazioni molto specifiche in modo pratico.

## Parametri

* **p00**: punto in alto a sinistra.
* **p01**: Punto in basso a sinistra
* **p10**: punto superiore destro.
* **p11**: in basso a destra.
* **Soffocamento**: *Solo anteriore, Solo posteriore, Davanti e Indietro e Davanti* Sposta la forma quando i punti si intersecano.
* **Abilita Porzione**: *False/True*
* **Colore sfondo**: *(valore scala di grigio)*Colore di sfondo uniforme se la suddivisione in porzioni è disattivata.
* **Campionamento**: *Bilineare, Più Vicino* Impostate la qualità di campionamento.

## Immagini di esempio

![](../../../../../../assets/quad-example.gif)

</td>
</tr>
</table>
