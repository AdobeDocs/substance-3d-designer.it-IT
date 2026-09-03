---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rilevamento bordi per rilevare i bordi nelle texture e creare così profili ed effetti maschera basati sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rilevamento bordo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Rilevamento bordo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Rileva il contrasto nelle immagini in bianco e nero, quindi crea una maschera in bianco e nero che evidenzia il contrasto.

Utile in molti casi in cui è necessaria una maschera per i bordi. Tieni presente che funziona meglio con input ad alto contrasto; se necessario, regola il contrasto prima di passare qualcosa in questo nodo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Larghezza bordo</b> <i>1.0 - 16.0</i> | Larghezza delle aree rilevate attorno ai bordi. |
| <b>Rotondità bordo</b> <i>0.0 - 16.0</i> | Arrotonda, sfoca e smussa insieme la maschera generata. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte il risultato. |
| <b>Tolleranza</b> <i>0.0 - 1.0</i> | Fattore soglia tolleranza per la posizione in cui devono apparire i bordi. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-02.png" />
        </td>
    </tr>
</table>
