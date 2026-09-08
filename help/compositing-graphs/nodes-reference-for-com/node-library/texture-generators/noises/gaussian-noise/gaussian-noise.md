---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo gaussiano per generare pattern di disturbo distribuiti gaussiani per la creazione di texture e variazioni organiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rumore gaussiano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78ee271bee643682c3815dd1657d66accb2f31c4
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 1%

---


# Rumore gaussiano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rumore gaussiano - Icona](../../../../../../assets/gaussian_noise-1.png "Rumore gaussiano - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Un disturbo uniforme generato dalla combinazione di sfumature in cui i valori passano dal nero al bianco seguendo una distribuzione normale, simile a una curva a campana.

Consultate anche: [Macchie gaussiane 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md), [Macchie gaussiane 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> <i>Mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disturbo</b> quando il parametro <b>anisotropia disturbo</b> è diverso da zero. |
| <b>Scostamento porzione</b> <i>Float2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore gaussiano - Esempio 1](../../../../../../assets/gaussian_noise-1_1.png "Rumore gaussiano - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore gaussiano - Esempio 2](../../../../../../assets/noise_gaussian_noise_v2_speed0.6_aniso0.gif "Rumore gaussiano - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore gaussiano - Esempio 3](../../../../../../assets/noise_gaussian_noise_v2_speed0.6_aniso1.gif "Rumore gaussiano - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore gaussiano - Esempio 4](../../../../../../assets/noise_gaussian_noise_v2_speed0.3_aniso0.6.gif "Rumore gaussiano - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
