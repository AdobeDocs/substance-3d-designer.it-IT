---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/perlin-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo di Perlin per generare pattern di disturbo uniformi e naturali per creare texture e variazioni organiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Perlin noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Perlin noise
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---


# Perlin noise

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rumore di Perlin - Icona](perlin-noise.resources/perlin-noise-01.png "Rumore di Perlin - Icona"){width="200px"}

<b>Ingresso:</b> generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera un disturbo di Perlin, una distribuzione uniforme ampiamente utilizzata dei valori in scala di grigio.

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
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Scostamento porzione</b> <i>Virgola mobile 2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore di Perlin - Esempio 1](perlin-noise.resources/perlin-noise-02.png "Rumore di Perlin - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore di Perlin - Esempio 2](perlin-noise.resources/perlin-noise-03.gif "Rumore di Perlin - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>
