---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-2.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo direzionale 2 per generare pattern di disturbo direzionale con due ottave per la creazione di effetti anisotropi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: DISTURBO DIREZIONALE 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 93824555c1b2d3de289eaf470e6f929ebf90dd71
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# DISTURBO DIREZIONALE 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Disturbo direzionale 2 - Icona](directional-noise-2.resources/directional_noise_2.png "Disturbo direzionale 2 - Icona"){width="200px"}

<b>Ingresso:</b> generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei rumori di <b>Disturbo direzionale</b>.

Vedere anche: [Disturbo direzionale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Disturbo direzionale 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md), [Disturbo direzionale 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

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
| <b>Scala</b> <i>Numero intero</i> | Suddivisione della griglia utilizzata per generare le porzioni di disturbo.    Un valore più elevato determina la creazione di più riquadri e un disturbo maggiore. |
| <b>Disturbo</b> <i>Virgola mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Virgola mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> <i>Virgola mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Virgola mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disorder</b> quando il parametro &#39;anisotropia del disturbo&#39; è diverso da zero. |
| <b>Angolo</b> <i>Virgola mobile</i> | Angolo utilizzato per impostare la direzione del disturbo, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> <i>Virgola mobile</i> | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Scostamento porzione</b> <i>Virgola mobile 2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Disturbo direzionale 2 - Esempio 1](directional-noise-2.resources/directional_noise_2_1.png "Disturbo direzionale 2 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Disturbo direzionale 2 - Esempio 2](directional-noise-2.resources/noise_directional_noise_2_v2_speed0.6_aniso0.gif "Disturbo direzionale 2 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Disturbo direzionale 2 - Esempio 3](directional-noise-2.resources/noise_directional_noise_2_v2_speed0.6_aniso1.gif "Disturbo direzionale 2 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Disturbo direzionale 2 - Esempio 4](directional-noise-2.resources/noise_directional_noise_2_v2_speed0.3_aniso0.6.gif "Disturbo direzionale 2 - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
