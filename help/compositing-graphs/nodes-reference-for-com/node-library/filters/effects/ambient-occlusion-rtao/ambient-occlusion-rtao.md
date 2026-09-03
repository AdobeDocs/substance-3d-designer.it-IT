---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Utilizza il nodo Occlusione ambiente (RTAO) per generare mappe di occlusione ambientale in tempo reale da mappe di height per un'ombreggiatura realistica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusione ambientale (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Occlusione ambientale (RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo RTAO](ambient-occlusion-rtao.resources/ambient-occlusion-rtao-01.png "Icona nodo RTAO")

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una mappa di Occlusione ambientale in base all&#39;input di una mappa di height.

Questo filtro fornisce risultati più accurati rispetto all&#39;HBAO ma non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo.

Per un&#39;alternativa più semplice e veloce, vedere [Occlusione ambiente (HBAO) (nodo filtro)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Usa Dimensioni fisiche</b> <i>Booleano</i> | Attivate/disattivate per utilizzare le impostazioni della Dimensioni fisiche per determinare la scala del height. |
| <b>Dimensioni fisiche</b> <i>Float3</i> <i>(Disponibile quando <b>Usa Dimensioni fisiche</b> è impostato su <i>Vero</i>)</i> | Regola la scala del height in base alla dimensioni fisiche reale della superficie |
| <b>Esempi</b> <i>Numero intero</i> | Numero di raggi utilizzati per il calcolo dell&#39;occlusione ambientale.<br>Un valore più elevato fornisce un risultato più uniforme e preciso a scapito delle prestazioni. |
| <b>Scala Height</b> <i>Mobile</i> <i>(Disponibile quando <b>Usa Dimensioni fisiche</b> è impostato su <i>False</i>)</i> | Moltiplicatore per l&#39;intensità dell&#39;input della mappa del height. |
| <b>Distribuzione</b> <i>Numero intero</i> | Imposta il metodo di distribuzione. Influisce sul decadimento verso le aree in ombra, |
| <b>Distanza Massima</b> <i>Mobile</i> | Consente di impostare la distanza massima percorribile dai raggi per l’occlusione. |
| <b>Angolo di diffusione</b> <i>Mobile</i> | Consente di impostare l’angolo di diffusione dei raggi da riprendere. Un valore pari a 1 è un emisfero completo. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/ambient-occlusion-rtao-03.png" />
        </td>
    </tr>
</table>
