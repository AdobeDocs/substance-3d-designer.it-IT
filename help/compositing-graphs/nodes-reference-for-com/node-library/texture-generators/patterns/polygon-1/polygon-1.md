---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Usa il nodo Poligono 1 per generare pattern poligonali di base con lati e proprietà personalizzabili per texture geometriche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Poligono 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# Poligono 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-1.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una forma poligonale, con molte opzioni di regolazione. Per una versione più semplice, vedere [Poligono 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Lati</b> <i>3 - 32</i> | Imposta la quantità di lati che deve avere il poligono. |
| <b>Esplodi</b> <i>0.0 - 1.0</i> | Sposta le &quot;sezioni&quot; del poligono. |
| <b>Dimensione triangolo</b> <i>0.0 - 1.0</i> | Regola la dimensione di sezioni/triangoli. Qualsiasi regolazione poteva dividere la forma, solo 1,1. è perfettamente connesso! |
| <b>Scala</b> <i>0.0 - 1.0</i> | Ridimensiona l&#39;intera forma come un&#39;unica forma. |
| <b>Scala automatica</b> <i>Falso/Vero</i> | Regola le proporzioni in modo che l&#39;intero poligono si adatti alla visualizzazione, con i parametri predefiniti. |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota l&#39;intera forma. |
| <b>Sfumatura</b> <i>Falso/Vero</i> | Genera fette/triangoli con gradiente anziché solidi. Nota: diventa simile al Poligono 2 con questa impostazione attivata. |
| <b>Inversione sfumatura</b> <i>Falso/Vero</i> | Capovolge la direzione della sfumatura se &quot;Sfumatura&quot; è abilitato. |
| <b>Affiancatura</b> <i>1 - 16</i> | Imposta il numero di volte in cui il risultato deve essere affiancato. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |
| <b>Affiancamento non quadrato</b> <i>Falso/Vero</i> | Quando è abilitato il Non square expansion, la forma verrà affiancata senza schiacciamenti. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
