---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: Utilizza il nodo HDRI lineare sfumatura per creare sfumature lineari in ambienti HDRI per impostazioni di illuminazione personalizzate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfumatura lineare (HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Sfumatura lineare (HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-linear-hdri.resources/gradient-linear-hdri-01.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Crea una sfumatura lineare attraverso il centro con un punto posizionato dall’utente. Il risultato finale viene regolato in base alla proiezione sferica, a differenza del normale [gradiente lineare 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Posizione punto</b> | Posizione del punto utilizzato per determinare la direzione del gradiente. |
| <b>Colore principale</b> <i>(valore colore)</i> | Colore della parte superiore della sfumatura (al punto) |
| <b>Colore inferiore</b> <i>(valore colore)</i> | Colore della parte inferiore della sfumatura (lontano dal punto). |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-linear-hdri.resources/gradient-linear-hdri-02.gif" />
        </td>
    </tr>
</table>
