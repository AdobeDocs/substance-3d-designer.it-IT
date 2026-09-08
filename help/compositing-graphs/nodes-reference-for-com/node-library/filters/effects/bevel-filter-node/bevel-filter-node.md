---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Utilizzare il nodo del filtro Smusso per creare bordi smussati su forme e motivi per aggiungere profondità e dimensione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Smussato (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# Smussato (nodo filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue un effetto di smussatura dei bordi su una mappa di altezza in scala di grigi di input. Restituisce sia Heightmap smussato che Normalmap in base a tale Heightmap.

Questo è un nodo utile per applicare profili di curve esatti su una Heightmap di base idealmente binaria (bianco/nero con elevato contratto).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>input</b> <i>Input scala di grigi</i> | Heightmap da convertire. |
| <b>Curva personalizzata</b> <i>Input scala di grigi</i> | Sfumatura che determina la curva/pendenza esatta. Idealmente è un nodo lineare sfumatura, su cui è possibile eseguire qualsiasi tipo di regolazione, ad esempio [Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) o [Curve](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Attivo solo quando &quot;Usa curva personalizzata&quot; è True. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Distanza</b> <i>-1.0 - 1.0</i> | Indica quanto deve estendersi l’effetto smussato. |
| <b>Tipo angolo</b> <i>Arrotondato, Angular</i> | Indica se il profilo di smussatura deve essere arrotondato o diritto. |
| <b>Arrotondamento</b> <i>0.0 - 5.0</i> | Indica l’effetto di arrotondamento (sfocatura) aggiuntivo da applicare dopo la smussatura. |
| <b>Usa Sfocatura Non Uniforme</b> <i>Falso/Vero</i> | Indica se l&#39;arrotondamento deve essere eseguito in modo non uniforme. |
| <b>Usa curva personalizzata</b> <i>Falso/Vero</i> | Attiva/disattiva l’utilizzo della curva di height personalizzata. Vedi sopra per maggiori informazioni. |
| <b>Intensità normale</b> <i>0.0 - 50.0</i> | Intensità della mappa Normale generata. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Consente di passare da un formato Normalmap a un altro (inverte il canale Verde). |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bevel-example.png" />
        </td>
    </tr>
</table>
