---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
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
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---


# Disturbo Perlin 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo <b>Disturbo di Perlin 3D</b> genera un disturbo di Perlin nello spazio 3D in base all&#39;input <b>Mappa posizione</b>.

Questo nodo può essere testato con [Cubo 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

</td>
</tr>
</table>

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con <i>motore GPU</i> (ad esempio <b>Direct3D</b> o <b>OpenGL</b>). Vai a <b>Strumenti > Cambia motore...</b> oppure premi il tasto <b>F9</b> per selezionare il motore desiderato.

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti</b> <i>Booleano</i> | Inverte l’immagine di output. |
| <b>Scala</b> <i>Mobile</i> | Controlla la scala del disturbo di Perlin 3D. |
| <b>Dimensioni</b> <i>Float3</i> | Controlla la dimensione del disturbo di Perlin 3D sugli assi <b>X</b>, <b>Y</b> e <b>Z</b>. I valori non uniformi producono un effetto <i>allungamento o schiacciamento</i>. |
| <b>Scostamento</b> <i>Float3</i> | Applica uno scostamento alla <i>posizione</i> del disturbo di Perlin 3D sugli assi <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensità Distorsione</b> <i>Mobile</i> | Controlla l’intensità di un <i>effetto di alterazione</i> applicato al disturbo di Perlin 3D. |
| <b>Moltiplicatore scala Distorsione</b> <i>Mobile</i> | Controlla la scala del <i>pattern di deformazione</i> utilizzato nell&#39;effetto di alterazione controllato dall&#39;<b>intensità della Distorsione</b>. |
| <b>Previsione</b> <i>Mobile</i> | Applica un <i>offset</i> al valore di <i>luminanza</i> della linea di base per la distribuzione del valore di disturbo Perlin 3D. |
| <b>Contrasto</b> <i>Mobile</i> | Regola il contrasto del disturbo 3D di Perlin. |
| <b>Assoluto</b> <i>Booleano</i> | Usa valori assoluti nel disturbo di Perlin 3D. In questo modo <i>viene invertita</i> la distribuzione dei valori <i>inferiori a 0,5</i>. |
| <b>Abilita Affiancamento</b> <i>Booleano</i> | Regola il disturbo di Perlin 3D in modo che il relativo pattern <i>si ripeta</i> sugli assi X, Y e Z. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dperlin.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dperlinnoise-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dperlinnoise-variant.jpg" />
        </td>
    </tr>
</table>
