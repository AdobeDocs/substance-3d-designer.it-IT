---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Usa il nodo Trasforma quadrupla per applicare trasformazioni quadrilaterali alle texture per la correzione e l'alterazione delle Prospettive.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasforma quadruplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# Trasforma quadruplo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-grayscale.png){width="128px"}

![](quad-transform.resources/quad-transform.png){width="128px"}

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di Trasforma speciale che consente la trasformazione di una forma quadrupla attraverso l&#39;interazione con i relativi punti d&#39;angolo. Consente Trasforma molto specifici in modo pratico.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>p00</b> | Punto in alto a sinistra. |
| <b>p01</b> | Punto in basso a sinistra |
| <b>p10</b> | Punto in alto a destra. |
| <b>p11</b> | In basso a destra. |
| <b>Annullamento</b> <i>Solo anteriore, Solo posteriore, Fronte e Fronte</i> | Impostate l’effetto di taglio/nascondere la forma quando i punti si incrociano. |
| <b>Abilita Affiancamento</b> <i>Falso/Vero</i> |  |
| <b>Colore di sfondo</b> <i>(valore scala di grigi)</i> | Colore di sfondo in tinta unita se Affiancamento è disattivato. |
| <b>Campionamento</b> <i>Bilineare, Più Vicino</i> | Impostate la qualità di campionamento. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-example.gif" />
        </td>
    </tr>
</table>
