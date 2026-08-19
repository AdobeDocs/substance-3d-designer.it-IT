---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-3.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo direzionale 3 per generare pattern di disturbo direzionale con tre ottave per la creazione di texture direzionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: DISTURBO DIREZIONALE 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 2%

---


# DISTURBO DIREZIONALE 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Disturbo direzionale 3 - Icona](../../../../../../assets/directional_noise_3.png "Disturbo direzionale 3 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei rumori di <b>Disturbo direzionale</b>.

Vedere anche: [Disturbo direzionale 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Disturbo direzionale 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Disturbo direzionale 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Output

</td>
<td style="border: 0;" valign="top">

### Parametri

</td>
<td style="border: 0;" valign="top">

### Esempi

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
| <b>Scala</b> Intero | Suddivisione della griglia utilizzata per generare le porzioni di disturbo.    Un valore più elevato determina la creazione di più riquadri e un disturbo maggiore. |
| <b>Disturbo</b> Mobile | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> Mobile | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> Mobile | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>Angolo di anisotropia disturbo</b> Mobile | Controlla la direzione dello spostamento applicato dal parametro <b>Disorder</b> quando il parametro &#39;anisotropia del disturbo&#39; è diverso da zero. |
| <b>Angolo</b> Mobile | Angolo utilizzato per impostare la direzione del disturbo, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> Mobile | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Scostamento porzione</b> Float2 | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Disturbo direzionale 3 - Esempio 1](../../../../../../assets/directional_noise_3_1.png "Disturbo direzionale 3 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Disturbo direzionale 3 - Esempio 2](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso0.gif "Disturbo direzionale 3 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Disturbo direzionale 3 - Esempio 3](../../../../../../assets/noise_directional_noise_3_v2_speed0.6_aniso1.gif "Disturbo direzionale 3 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Disturbo direzionale 3 - Esempio 4](../../../../../../assets/noise_directional_noise_3_v2_speed0.3_aniso0.6.gif "Disturbo direzionale 3 - Esempio 4"){zoomable="yes"}

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
