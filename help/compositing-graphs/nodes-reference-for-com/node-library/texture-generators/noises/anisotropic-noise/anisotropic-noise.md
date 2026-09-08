---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo anisotropo per generare pattern di disturbo direzionale per la creazione di effetti di texture anisotrope.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rumore anisotropo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Rumore anisotropo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rumore anisotropo - Icona](../../../../../../assets/anisotropic_noise_v2.png "Rumore anisotropo - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una pila orizzontale o verticale di strisce colorate casualmente si dissolve l&#39;una nell&#39;altra.

La quantità di strisce è regolabile, così come lo smoothness delle loro transizioni.

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
| <b>X importo</b> <i>Numero intero</i> | Quantità di strisce sull&#39;asse X. |
| <b>Importo Y</b> <i>Numero intero</i> | Quantità di strisce sull&#39;asse Y. |
| <b>Importo Y per risoluzione</b> <i>Booleano</i> | Se è True, il numero di strisce sull&#39;asse Y sarà uguale alle dimensioni dell&#39;immagine su tale asse. |
| <b>Ruota</b> <i>Booleano</i> | Ruota il disturbo di 90 gradi. |
| <b>Smoothness</b> <i>Mobile</i> | Quantità di dissolvenza tra le strisce, dove 0 non è una dissolvenza e 1 è una dissolvenza per l&#39;intera lunghezza. |
| <b>Interpolazione Smoothness</b> <i>Mobile</i> | Ponderazione dei due metodi di interpolazione applicati per sfumare le strisce, dove 0 è lineare e 1 è gaussiano. |
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.   Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.   Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore anisotropo - Esempio 1](../../../../../../assets/anisotropic_noise_v2_1.png "Rumore anisotropo - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore anisotropo - Esempio 2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "Rumore anisotropo - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>
