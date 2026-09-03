---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Usate il nodo Traccia forma per aggiungere contorni di traccia alle forme per creare bordi ed effetti per i bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tratto forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Tratto forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke-01.png){width="128px"}

![](shape-stroke.resources/shape-stroke-02.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Aggiunge un tratto o un contorno attorno a una maschera in bianco e nero (per la versione in scala di grigio) o a una forma con un canale alfa (per la versione a colori), come si potrebbe già fare con altre applicazioni di modifica di immagini 2D. Può essere visualizzata come una versione più completa di [Rilevamento bordo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Molto utile per vari effetti di editing delle immagini.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Larghezza</b> <i>-1.0 - 1.0</i> | Larghezza dell’effetto del tratto. |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Opacità globale dell’effetto. |
| Colore <b>(Contorno)</b> <i>(valore colore)</i> | Colore utilizzato per l&#39;effetto contorno. |
| <b>Colore maschera</b> <i>(Valore colore) (Solo versione in scala di grigio)</i> | Tinta unita da utilizzare per l’output con mappatura della trasparenza. |
| <b>Input Premoltiplicato</b> <i>False/True (Solo Versione A Colori)</i> | Indica se l&#39;input deve essere considerato premoltiplicato. |
| <b>Pre-Moltiplica output</b> <i>Falso/Vero</i> | Indica se l&#39;output deve essere premoltiplicato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shape-stroke-03.png" />
        </td>
    </tr>
</table>
