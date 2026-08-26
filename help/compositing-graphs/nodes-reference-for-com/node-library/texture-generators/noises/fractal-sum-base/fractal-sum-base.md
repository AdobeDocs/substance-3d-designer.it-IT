---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Utilizzate il nodo Somma frattale base per generare pattern di disturbo frattale di base per la creazione di texture organiche complesse.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Somma frattale base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Somma frattale base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Base Somma frattale - Icona](../../../../../../assets/fractal_sum_base.png "Base Somma frattale - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Un disturbo frattale personalizzabile con un intervallo e un bilanciamento regolabili di ottave.

I rumori della Somma frattale <b></b> sono tutti basati su questo nodo.

Vedere anche: [Somma frattale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Somma frattale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Somma frattale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Somma frattale 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

</td>
</tr>
</table>

## Output

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | Il disturbo generato come bitmap in scala di grigio. |

## Parametri

|  |  |
| --- | --- |
| <b>Rugosità</b> Mobile | Bilanciamento delle ottave di disturbo.    Un valore più elevato renderà più visibili le ottave con frequenza più elevata. |
| <b>Min. level</b> Integer | L&#39;ottava minima utilizzata nel rumore.    Un valore più elevato determina una frequenza di disturbo più elevata. |
| <b>Max. level</b> Integer | Ottava massima utilizzata nel rumore.    Un valore più elevato determina una frequenza di disturbo più elevata. |
| <b>Disturbo</b> Mobile | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> Mobile | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Contrasto</b> Mobile | Contrasto del risultato finale. |
| <b>Opacità globale</b> float | Opacità delle ottave di disturbo sommate nel risultato finale.    Un valore elevato può causare la bruciatura di aree bianche. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Base Somma frattale - Esempio 1](../../../../../../assets/fractal_sum_base_1.png "Base Somma frattale - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Base Somma frattale - Esempio 2](../../../../../../assets/noise_fractal_sum_base_v2_speed0.6_aniso0.gif "Base Somma frattale - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
