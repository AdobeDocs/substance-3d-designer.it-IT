---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rendering superficie Texture 3D per eseguire il rendering delle texture di superficie dai dati 3D per la creazione di effetti di procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering superficie texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Rendering superficie texture 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>Ingresso:</b> Filtro > Effetto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rendering superficie Texture 3D** esegue il rendering della superficie di una forma descritta da una *texture 3D*, utilizzando il corrispondente *campo distanza* dall&#39;input dell&#39;immagine **Campo distanza 3D**.

La superficie è rappresentata entro i limiti di un *cubo di unità*. L&#39;illuminazione viene calcolata utilizzando l&#39;immagine di input **Ambiente** mappata su una sfera infinita.

>[!NOTE]
>
> Il campo distanza dovrebbe essere una texture **4096x4096** che descrive la forma con una griglia **16x16** di 256 sezioni.\
> È possibile utilizzare il nodo [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) della Texture 3D per calcolare il campo distanza per una texture 3D di 256 sezioni.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Campo Distanza 3D</b> <i>Scala di grigi</i> | Immagine 4096x4096 che rappresenta le 256 <i>sezioni</i> del <i>campo distanza</i> di una forma, disposta in una griglia 16x16.<br>È possibile utilizzare il nodo [SDF Texture 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) per calcolare il campo distanza per una texture 3D di 256 sezioni. |
| <b>Ambiente</b> <i>Colore</i> | Immagine che rappresenta l&#39;<i>ambiente</i>, che deve essere mappata a una sfera infinita nel rendering e utilizzata per calcolare l&#39;<i>illuminazione</i>.<br>L&#39;immagine viene utilizzata anche per eseguire il rendering dello sfondo della scena quando il parametro <b>Modalità sfondo</b> è impostato su <i>Ambiente</i> o <i>Ambiente</i>. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Risoluzione output</b> <i>Intero2</i> | La risoluzione dell&#39;immagine di output in <b>X</b> e <b>Y</b>, espressa come <i>potenza di due</i>. |
| <b>Posizione fotocamera</b> <i>Float2</i> | La posizione della videocamera attorno alla forma.<br>Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella <b>vista 2D</b> per <i>orbita</i> della fotocamera. |
| <b>Distanza fotocamera</b> <i>Virgola mobile</i> | La distanza tra la fotocamera e la forma. |
| <b>Camera FOV</b> <i>Virgola mobile</i> | Il campo visivo della fotocamera in <i>gradi</i>. |
| <b>Albedo</b> <i>Virgola mobile 3</i> | Colore di albedo della superficie della forma. |
| <b>Modalità sfondo</b> <i>Numero intero</i> | Metodo di rappresentazione dello sfondo della scena renderizzata:<br>- <i>Irradianza terreno</i>: irradianza calcolata del piano terreno<br>- <i>Ambiente</i>: colore ambientale dell&#39;immagine <b>Ambiente</b> mappato su una sfera infinita, simile a una versione fortemente sfocata dell&#39;immagine<br>- <i>Colore uniforme</i>: riempi in modo uniforme lo sfondo con un colore specificato<br>- <i>Ambiente</i>: l&#39;immagine <b>Ambiente</b> mappata su una sfera infinita di input |
| <b>Colore di sfondo</b> <i>Virgola mobile 4</i> | Colore utilizzato per riempire in modo uniforme lo sfondo della scena sottoposta a rendering.<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Modalità sfondo</b> è impostato su <i>Colore uniforme</i>. |
| <b>Abilita piano terreno</b> <i>Booleano</i> | Se <i>True</i>, esegue il rendering di un piano terreno. Il <i>cubo di unità</i> che racchiude la forma si trova su questo piano. |
| <b>Piano infinito</b> <i>Booleano</i> | Imposta il piano terreno in modo che si estenda <i>all&#39;infinito</i> fino all&#39;orizzonte.<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Abilita piano terreno</b> è impostato su <i>True</i>. |
| <b>Dimensioni piano terreno</b> <i>Virgola mobile 2</i> | Regola la dimensione del piano terreno.<br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Abilita piano terreno</b> è impostato su <i>True</i> e il parametro <b>Piano infinito</b> è impostato su <i>False</i>. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
