---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-2.html"
breadcrumb-title: ''
description: Utilizzate il nodo Somma frattale 2 per generare un disturbo frattale con due ottave per creare variazioni di texture organiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SOMMA FRATTALE 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# SOMMA FRATTALE 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Somma frattale 2 - Icona](fractal-sum-2.resources/fractal_sum_2.png "Somma frattale 2 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei rumori di <b>Somma frattale</b>.

Vedere anche: [Somma frattale base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Somma frattale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Somma frattale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Somma frattale 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

</td>
</tr>
</table>

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Il disturbo generato come bitmap in scala di grigio. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Somma frattale 2 - Esempio 1](fractal-sum-2.resources/fractal_sum_2_1.png "Somma frattale 2 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Somma frattale 2 - Esempio 2](fractal-sum-2.resources/noise_fractal_sum_2_v2_speed0.6_aniso0.gif "Somma frattale 2 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>
