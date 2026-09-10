---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo di Worley 3D per generare il disturbo di Worley in base alla posizione 3D per la creazione di effetti di texture volumetrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Disturbo di Worley 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 7%

---


# Disturbo di Worley 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-worley-noise.resources/3d-worley.png){width="128px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Uno dei rumori più versatili e avanzati della libreria, genera un disturbo di Worley in uno spazio 3D, basato su una mappa di posizione di input. Offre numerose opzioni che lo rendono molto più potente dei rumori standard basati su [Celle](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)o [Distanza](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>1 - 64</i> | Impostate la scala globale per l’effetto. |
| <b>Dimensioni</b> <i>0.0 - 1.0</i> | Eseguire separatamente il ridimensionamento non uniforme sugli assi X, Y e Z. |
| <b>Modalità</b> <i>Euclideo, Manhattan, Chebyshev, Minkowski</i> | Modificate la metrica della distanza. Consente alcuni tipi di disturbo molto diversi. |
| <b>Numero di Minkowski</b> <i>0.0 - 20.0</i> | Solo con metrica della distanza di Minkowski. Fusioni tra diversi tipi di metriche. |
| <b>Stile</b> <i>F1, F2, F2-F1, Bordo, Colore casuale</i> | Impostare la combinazione di metriche. Consente molte più combinazioni. |
| <b>Larghezza bordo</b> <i>0.0 - 1.0</i> | Quando la combinazione di bordi è attiva, controlla la larghezza del bordo. |
| <b>Arrotondamento</b> <i>0.0 - 1.0</i> | Disponibile solo nelle modalità F1, F2 e F2-F1. Imposta la posizione intermedia del livello. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte il risultato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-worley-noise.resources/3d-worley-ex01.png" />
        </td>
    </tr>
</table>
