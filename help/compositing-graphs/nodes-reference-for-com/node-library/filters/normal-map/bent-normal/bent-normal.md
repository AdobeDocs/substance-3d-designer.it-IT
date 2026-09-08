---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Utilizzate il nodo Normale piegatura (Bent Normal) per generare mappe normali piegate che tengano conto dell'occlusione ambientale e dell'illuminazione indiretta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura della normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# Curvatura della normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo normale piegato](../../../../../../assets/rt-bent-normal.png "Icona nodo normale piegato")

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una Mappa normale piegata in base all&#39;input di una mappa di altezza. Una Mappa normale piegata è una versione speciale di [Normale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) e [Occlusione ambientale (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), che genera una mappa normale con occlusione ambientale incorporata.\
Questo può essere utilizzato nei motori in tempo reale per eseguire i baking l&#39;Occlusione ambientale nella mappa normale, ad esempio per riflessioni di occlusione più accurate sui metalli.

Questo nodo non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Usa Dimensioni fisiche</b> <i>Booleano</i> | Attivate/disattivate per utilizzare le impostazioni della Dimensioni fisiche per determinare la scala del height. |
| <b>Dimensioni fisiche</b> <i>Virgola mobile 3</i> | (Disponibile quando <b>Usa Dimensioni fisiche</b> è impostato su <i>Vero</i>) Regola la scala del height in base alla dimensioni fisiche reale della superficie. |
| <b>Esempi</b> <i>Numero intero</i> | Numero di raggi utilizzati per calcolare la normale piegata.<br>Un valore più alto fornisce un risultato più uniforme e preciso a scapito delle prestazioni. |
| <b>Scala Height</b> <i>Virgola mobile</i> | (Disponibile quando Usa Dimensioni fisiche è impostato su False) Moltiplicatore per l&#39;intensità dell&#39;input della mappa dell&#39;altezza. |
| <b>Distribuzione</b> <i>Numero intero</i> | Imposta il metodo di distribuzione. Influisce sul decadimento verso le aree in ombra. |
| <b>Distanza Massima</b> <i>Virgola mobile</i> | Consente di impostare la distanza massima percorribile dai raggi per l’occlusione. |
| <b>Angolo di diffusione</b> <i>Mobile</i> | Consente di impostare l’angolo di diffusione dei raggi da riprendere. Un valore pari a 1 è un emisfero completo. |
| <b>Formato Normale</b> <i>Numero intero</i> | Inverte il canale verde dell’output. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bent-normal-ex-1.jpg" />
        </td>
    </tr>
</table>
