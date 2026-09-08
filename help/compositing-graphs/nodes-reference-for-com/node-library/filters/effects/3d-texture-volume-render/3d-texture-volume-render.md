---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Utilizza il nodo Rendering volume texture 3D per eseguire il rendering delle texture volumetriche dai dati 3D per creare effetti cloud e nebbia.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering volume texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# Rendering volume texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

<b>Ingresso:</b> Filtro > Effetto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rendering volume texture 3D** esegue il rendering del volume di una forma descritta da una *texture 3D*, utilizzando il corrispondente *campo distanza con segno* dall&#39;input dell&#39;immagine **3D Signed distance field**.

Il volume è rappresentato entro i limiti di un *cubo di unità*. L&#39;illuminazione viene calcolata utilizzando *luce direzionale* e un *lucernario emisferico*.

>[!NOTE]
>
> Il campo distanza con segno deve essere una texture **4096x4096** che descrive la forma con una griglia **16x16** di 256 sezioni.\
> È possibile utilizzare il nodo [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) per calcolare il campo distanza con segno per una texture 3D di 256 sezioni.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Signed distance field 3D</b> <i>Scala di grigi</i> | Immagine 4096x4096 che rappresenta le 256 <i>sezioni</i> di un <i>campo distanza con segno</i> di una forma, disposta in una griglia 16x16.<br>È possibile utilizzare il nodo [SDF Texture 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) per calcolare il campo distanza firmato per una texture 3D di 256 sezioni. |
| <b>Densità</b> <i>Scala di grigi</i> | Immagine 4096x4096 che rappresenta le 256 <i>sezioni</i> della <i>densità</i> di una forma, disposta in una griglia 16x16. La densità viene mappata utilizzando valori in scala di grigio da 0 (completamente trasparente) a 1 (completamente opaco).<br>È possibile utilizzare [maschere di volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) o nodi di disturbo 3D ([disturbo di Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [frattale disturbo con dorso 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) ecc.), combinati con un nodo [Posizione Texture 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) come input di posizione, per generare una maschera di volume come texture 3D di 256 sezioni. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Risoluzione output</b> <i>Intero2</i> | La risoluzione dell&#39;immagine di output in <b>X</b> e <b>Y</b>, espressa come <i>potenza di due</i>. |
| <b>Posizione fotocamera</b> <i>Float2</i> | La posizione della videocamera attorno alla forma.<br>Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella <b>vista 2D</b> per <i>orbita</i> della fotocamera. |
| <b>Posizione chiara</b> <i>Float2</i> | Posizione della <i>luce direzionale</i> attorno alla forma.<br>Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella <b>vista 2D</b> per <i>orbita</i> della sorgente luminosa. |
| <b>Distanza fotocamera</b> <i>Mobile</i> | La distanza tra la fotocamera e la forma. |
| <b>Camera FOV</b> <i>Mobile</i> | Il campo visivo della fotocamera in <i>gradi</i>. |
| <b>Assorbimento</b> <i>Mobile</i> | Regola la quantità di luce assorbita mentre passa <i>attraverso</i> il volume. |
| <b>Sfumatura</b> <i>Mobile</i> | Moltiplica il valore fornito dall&#39;input <b>Densità</b> con il valore del campo distanza <i>interna</i>.<br>La larghezza della <i>sfumatura di dissolvenza</i> viene regolata in modo efficace dal limite esterno del volume verso l&#39;interno. |
| <b>Metodo colore chiaro</b> <i>Numero intero</i> | Imposta il metodo di acquisizione del colore della luce direzionale:<br>- <i>Temperatura (Kelvin)</i>: il colore deriva dalla temperatura della luce, dove un valore <i>inferiore</i> genera un colore <i>più caldo</i><br>- <i>Colore RGB</i>: definite il colore utilizzando i valori RGB |
| <b>Temperatura leggera (Kelvin)</b> <i>Mobile</i> | Temperatura della luce direzionale che influisce sul <i>colore</i>. Un valore <i>inferiore</i> produce un colore <i>più caldo</i>.<br>Valori utili:<br>1800 K - Luce candela<br>2800 K - Lampada a incandescenza<br>5500 K - Luce diurna<br>6200 K - Bianco naturale<br>7000 K - Cielo coperto<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Metodo colore chiaro</b> è impostato su <i>Temperatura (Kelvin)</i>. |
| <b>Colore chiaro</b> <i>Float3</i> | Colore della luce direzionale.<br><i>Nota</i>: questo parametro è disponibile solo quando <b>Metodo colore chiaro</b> è impostato su <i>Colore RGB</i>. |
| <b>Intensità luce</b> <i>Mobile</i> | Intensità della luce direzionale. |
| <b>Colore ambiente</b> <i>Float3</i> | Il colore del lucernario ambiente. |
| <b>Intensità ambiente</b> <i>Mobile</i> | Intensità del lucernario ambiente. |
| <b>Albedo</b> <i>Float3</i> | Colore di albedo del volume. |
| <b>Modalità sfondo</b> <i>Numero intero</i> | Metodo di ombreggiatura dello sfondo della scena sottoposta a rendering, basato sul <b>colore di sfondo</b>:<br>- <i>ombreggiato</i>: il colore è influenzato dal <i>colore</i> e dalla <i>intensità</i><br> della luce direzionale - <i>colore costante</i>: il colore viene applicato in modo uniforme <i>indipendentemente</i> della luce direzionale |
| <b>Colore di sfondo</b> <i>Float4</i> | Il colore usato per riempire lo sfondo della scena sottoposta a rendering. |
| <b>Dithering</b> <i>Mobile</i> | Regola l’intensità del <i>dithering blu del disturbo</i> utilizzato per attenuare l’ombreggiatura. |
| <b>Abilita piano terreno</b> <i>Booleano</i> | Quando <i>True</i>, esegue il rendering di un piano terreno <i>infinito</i>. Il <i>cubo di unità</i> che racchiude la forma si trova su questo piano. |
| <b>Piano infinito</b> <i>Booleano</i> | Imposta il piano terreno in modo che si estenda <i>all&#39;infinito</i> fino all&#39;orizzonte.<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Abilita piano terreno</b> è impostato su <i>True</i>. |
| <b>Dimensioni piano terreno</b> <i>Float2</i> | Regola la dimensione del piano terreno.<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Abilita piano terreno</b> è impostato su <i>True</i> e il parametro <b>Piano infinito</b> è impostato su <i>False</i>. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3dtexturevolumerender-node.png" />
        </td>
    </tr>
</table>
