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
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Maschera volume 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

<b>Ingresso:</b> Generatore > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Maschera volume 3D** genera una rappresentazione di una *forma primitiva* basata sulla mappa di input **Posizione**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Posizione</b> <i>Colore</i> | La mappa che descrive le *coordinate dello spazio 3D* in cui è rappresentata la primitiva.<br><br>Le coordinate **X/Y/Z** sono mappate rispettivamente ai canali **R/G/B**. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Forma</b> <i>Numero intero</i> | Forma primitiva che deve essere rappresentata:<br><br>- *Cubo*<br>- *Cilindro*<br>- *Sfera* |
| <b>Scala</b> <i>Virgola mobile</i> | Definisce la scala *globale* del primitivo, applicata *in modo uniforme* su tutti gli assi. |
| <b>Dimensioni</b> <i>Virgola mobile 3</i> | Definisce le dimensioni della forma su ciascun asse. |
| <b>Input posizione</b> <i>Numero intero</i> | Metodo di *rappresentazione dello spazio* tramite l&#39;input **Posizione**:<br><br>- *Posizione UV*: utilizzare una *mappa UV*. Le coordinate X/Y (U/V) sono associate rispettivamente ai canali R/G. Si presume che l&#39;asse Z sia il vettore *ortogonale in avanti*.<br>- *Posizione spazio globale*: utilizzare una *mappa di posizione* per mappare l&#39;elemento di base nello spazio 3D. Le coordinate X/Y/Z sono associate rispettivamente ai canali R/G/B. |
| <b>Posizione UV</b> <i>Virgola mobile 2</i> | Posizione della primitiva nello spazio UV.<br><br>*Nota*: questo parametro è disponibile solo quando **Input posizione** è impostato su *Posizione UV*. |
| <b>Posizione</b> <i>Virgola mobile 3</i> | Posizione dell&#39;elemento di base nello spazio globale.<br><br>*Nota*: questo parametro è disponibile solo quando **Input posizione** è impostato su *Posizione spazio globale*. |
| <b>Rotazione</b> <i>Virgola mobile 3</i> | Definisce la rotazione della forma nello spazio mondo. |
| <b>Larghezza sfumatura</b> <i>Virgola mobile</i> | Regola la larghezza della *sfumatura di dissolvenza* dalla superficie del primitivo verso l&#39;interno. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>
