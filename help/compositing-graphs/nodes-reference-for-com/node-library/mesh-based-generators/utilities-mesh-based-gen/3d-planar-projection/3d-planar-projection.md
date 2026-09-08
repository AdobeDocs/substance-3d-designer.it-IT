---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Utilizzare il nodo Proiezione Planari 3D per proiettare texture su superfici mesh utilizzando la proiezione planari per la mappatura texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proiezione planare 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# Proiezione planare 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

<b>In:</b> Generatori Basati Su Trama > Utility

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue una proiezione della planari basata su dati di trama eseguiti i baking (Mappa normale Posizione e Mondo). Consente di proiettare e posizionare decalcomanie tra giunture, indipendentemente dalla mappatura UV originale.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Mappa posizione</b> <i>Input colore</i> | Mappa posizione eseguita i baking |
| <b>Spazio globale normale</b> <i>Input colore</i> | Mappa Normale Spazio Mondiale eseguita i baking |
| <b>Texture prevista</b> <i>Input colore</i> | Texture di input da proiettare sulla destinazione. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Posizionamento</b> |  |
| <b>Input progetto</b> <i>Posizione UV, Posizione spazio globale</i> | Scegli se la posizione di proiezione è impostata in uno spazio 2D/UV o 3D/Mondo. |
| <b>Posizione UV di destinazione</b> | Solo con input posizione UV, ideale per selezionare un punto nel Vista 2D sulla mappa posizione. |
| <b>Posizione di destinazione</b> <i>(valore colore)</i> | Solo con l’input Posizione spazio mondo (World Space Position Input) è possibile definire una coordinata 3D esatta. |
| <b>Destinazione normale</b> <i>(valore colore)</i> |  |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota la texture proiettata lungo l&#39;asse normale. |
| <b>Scala</b> <i>0.0 - 1.0</i> | Impostate la scala globale per la texture proiettata. |
| <b>Dimensioni</b> <i>0.0 - 2.0</i> | Eseguire il ridimensionamento non uniforme sulla texture proiettata. |
| <b>Mascheratura</b> |  |
| <b>Profondità massima</b> <i>0.0 - 1.0</i> | Controlla la profondità con cui apparirà la texture proiettata, quando verrà tagliata. |
| <b>Profondità dissolvenza</b> <i>0.0 - 1.0</i> | Imposta la transizione affinché la profondità di taglio sia improvvisa o sbiadita. |
| <b>Soglia normale</b> <i>-1.0 - 1.0</i> | Impostate la soglia per le superfici non esattamente allineate con la normale di proiezione. |
| <b>Dissolvenza normale</b> <i>0.0 - 1.0</i> | Impostate la transizione per le superfici non allineate in modo da ottenere una dissolvenza improvvisa o graduale. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
