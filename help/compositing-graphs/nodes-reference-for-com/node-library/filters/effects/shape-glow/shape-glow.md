---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Utilizzate il nodo Bagliore forma per aggiungere effetti di bagliore a forme e texture per creare effetti visivi luminosi e atmosferici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bagliore forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Bagliore forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-01.png){width="128px"}

![](shape-glow.resources/shape-glow-02.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Consente di creare un bagliore morbido attorno a una maschera di input (per la versione in scala di grigio) o a una forma con un canale alfa (per la versione a colori). Rispetto a [Glow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), questa funzione è più simile a quella di altri software di modifica di immagini 2D, in quanto è più completa e offre più controlli.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità</b> <i>Morbido, Preciso</i> | Passa da una modalità di precisione all’altra. |
| <b>Larghezza</b> <i>-1.0 - 1.0</i> | Controlla la distanza del bagliore. |
| <b>Pagine affiancate</b> <i>0.0 - 1.0</i> | Taglia/soglia per l’effetto di sfocatura, fa apparire il bagliore solido vicino alla forma. |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Opacità di fusione per l’effetto bagliore. |
| Colore <b>(Ombra)</b> <i>(valore colore)</i> | Tinta di colore da applicare al bagliore. |
| <b>Colore maschera</b> <i>(Valore colore) (Solo versione in scala di grigio)</i> | Tinta unita da utilizzare per l’output con mappatura della trasparenza. |
| <b>Input Premoltiplicato</b> <i>False/True (Solo Versione A Colori)</i> | Indica se l&#39;input deve essere considerato premoltiplicato. |
| <b>Pre-Moltiplica output</b> <i>Falso/Vero</i> | Indica se l&#39;output deve essere premoltiplicato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shape-glow-03.png" />
        </td>
    </tr>
</table>
