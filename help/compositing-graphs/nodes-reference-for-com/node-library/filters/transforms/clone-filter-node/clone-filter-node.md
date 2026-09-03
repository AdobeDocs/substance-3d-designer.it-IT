---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Utilizzate il nodo del filtro Clona per duplicare e scostare le aree della texture e creare pattern ed effetti di affiancamento uniformi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clona (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# Clona (nodo filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-filter-node-01.png)

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Clona l&#39;immagine di input una volta in una posizione specificata. Può funzionare come uno strumento &quot;timbro clone&quot; grezzo.

È necessario prestare particolare attenzione per ottenere i risultati desiderati:

* Idealmente, l’immagine di input avrà un canale alfa (come una decalcomania), poiché la fusione è solo una copia semplice.
* Poiché la maschera è impostata per impostazione predefinita sul nero, per visualizzare i risultati è necessario collegare almeno un valore di scala di grigi bianca uniforme.
* Lo scostamento consente di ritagliare facilmente l’esterno dell’immagine, quindi utilizzate valori piccoli.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Origine</b> <i>Input colore</i> | Immagine da clonare. Importante: l’ideale sarebbe che l’immagine avesse un canale alfa. |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Il valore predefinito è nero. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scostamento</b> <i>-</i> | Sposta o converte il risultato. Positivo è Sinistro e Su, Negativo è Destro e Giù. Usate valori piccoli: 1.0 e superiori lo spostano all’esterno dell’immagine. |
| <b>Maschera sfocatura</b> <i>0.0 - 10.0</i> | Applicate un filtro di sfocatura alla maschera per ammorbidire i bordi. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-filter-node-02.png" />
        </td>
    </tr>
</table>
