---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rapida diffusione reazione (Reaction Diffusion Fast) per generare pattern organici utilizzando algoritmi di diffusione rapida di reazione per texture procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diffusione rapida reazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# Diffusione rapida reazione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo diffusione reazione](reaction-diffusion-fast.resources/reaction-diffusion-fast-01.png "Icona nodo diffusione reazione")

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo esegue un effetto di reazione-diffusione su un&#39;immagine in scala di grigio di input.

La reazione-diffusione è un processo in cui la materia si diffonde (diffonde) e interagisce (reagisce) con altre materie. Si tratta di un modello matematico che simula ciò che accade in natura, ad esempio quando si formano determinati modelli sulla pelle animale.

Questo nodo è ottimizzato per le prestazioni e offre alcuni compromessi di precisione per la velocità.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi</i> | Immagine in scala di grigio a cui deve essere applicato l’effetto di diffusione della reazione. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine in scala di grigio che rappresenta l’effetto di diffusione della reazione applicato all’immagine di input. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Raggio</b> *Mobile* | Distanza di diffusione dell’effetto. |
| <b>Contrasto</b> *Mobile* | Regola il contrasto dell&#39;input e funge da soglia. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio 1](reaction-diffusion-fast.resources/reaction-diffusion-fast-02.png "Esempio 1")

</td>
<td style="border: 0;" valign="top">

![Esempio 2](reaction-diffusion-fast.resources/reaction-diffusion-fast-03.png "Esempio 2")

</td>
<td style="border: 0;" valign="top">

![Esempio 3](reaction-diffusion-fast.resources/reaction-diffusion-fast-04.gif "Esempio 3")

</td>
</tr>
</table>
