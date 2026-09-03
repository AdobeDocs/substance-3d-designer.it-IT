---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione normale (Normal Blend) per fondere insieme le mappe normali e creare transizioni omogenee tra i dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Fusione normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Fusione normale consente di fondere due mappe normali con una maschera opzionale, assicurandosi che tutti i valori rimangano normalizzati. Non differisce molto da un [nodo di fusione atomica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), ma ha aggiunto calcoli interni per Normalmaps.

Fusione normale non consente di combinare (sovrapporre) le mappe normali, in cui la mappa superiore aggiunge dettagli alla mappa inferiore. A tale scopo, utilizzare [Combinazione normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>Input colore</i> | Mappa Normale Primo Piano/Superiore. |
| <b>NormalBG</b> <i>Input colore</i> | Normalmap sfondo/inferiore. |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivata/disattivata con il parametro &quot;Usa maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Opacità</b> <i>0.0 - 1.0</i> | Fusione dell’opacità tra primo piano e sfondo |
| <b>Usa maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normal-blend-02.gif" /><br><i> (.gif introduce il dithering, ad esempio, i risultati nell'applicazione sono uniformi)</i>
        </td>
    </tr>
</table>
