---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo bianco per generare pattern di disturbo bianco per creare variazioni di texture ed effetti casuali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Disturbo bianco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Disturbo bianco

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rumore bianco - Icona](white-noise.resources/white-noise-01.png "Rumore bianco - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera un disturbo bianco utilizzando uno dei tre metodi disponibili per diverse forme di istogramma: uniforme, gaussiano e triangolo.

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
| <b>Distribuzione del disturbo</b> <i>Numero intero</i> | Metodo di distribuzione degli ingredienti per la forma di un istogramma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Uniforme:</i> istogramma piatto.</li> <li data-preserve-html="true"><i>Gaussiano:</i> istogramma che rappresenta una distribuzione normale, simile a una curva a campana.</li> <li data-preserve-html="true"><i>Triangolo:</i> Un istogramma triangolare.</li> </ul> |
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore bianco - Esempio 1](white-noise.resources/white-noise-02.png "Rumore bianco - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore bianco - Esempio 2](white-noise.resources/white-noise-03.gif "Rumore bianco - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>
