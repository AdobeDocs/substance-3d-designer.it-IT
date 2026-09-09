---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Usate il nodo Switch per passare da una texture di input a un’altra in base a una maschera per la selezione di texture condizionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cambia
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# Cambia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-1.png){width="128px"}

![](switch.resources/switch-grayscale.png){width="128px"}

<b>Ingresso:</b> Filtri > Fusione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Un semplice nodo switch a 2 posizioni. Restituisce Input 1 o Input 2 in base all&#39;impostazione del parametro Switch. Risultato non modificato. Per una versione più avanzata, vedere [Multi Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).

Molto utile per esporre una scelta booleana (Vero/Falso) in un grafico, in cui è necessario solo un singolo pulsante e non un elenco a discesa complesso per un&#39;intera selezione di opzioni.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usare &quot;Switch&quot; per gli ingressi colore, &quot;Switch Greyscale&quot; per gli ingressi scala di grigi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input 1 (True)</b> <i>Input a colori o in scala di grigi</i> |  |
| <b>Input 2 (False)</b> <i>Input a colori o in scala di grigi</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Switch</b> <i>Falso/Vero</i> | Passa dall&#39;input 1 (True) all&#39;input 2 (False). |
