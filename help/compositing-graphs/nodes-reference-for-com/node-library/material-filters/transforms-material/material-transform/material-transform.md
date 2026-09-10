---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasforma materiale per applicare le trasformazioni agli output del materiale, tra cui rotazione, scala e offset.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Trasformazione materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>Tra:</b> Filtri materiali > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

La Trasforma dei materiali è semplicemente la versione &quot;Multi-Channel&quot; dei materiali di [nodo atomico](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Trasforma tutti i canali di un materiale in ingresso contemporaneamente, con la stessa interfaccia di Trasforma 2D.

È sufficiente impostare correttamente i canali. Per impostazione predefinita, sono abilitati sia Metallico/Rugosità sia Specular/Lucentezza, il che potrebbe creare confusione.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Trasformazione</b> <i>(Matrice di trasformazione)</i> | Ruota e ridimensiona il risultato. Lo spostamento e il panning vengono eseguiti tramite il parametro Offset |
| <b>Scostamento</b> <i>-0.5 - 0.5</i> | Sposta o converte il risultato. Quando è presente il controllo Trasformazione, il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Formato Normale</b> | Scegliete tra il formato DirectX e OpenGL (capovolgi verde). |
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
