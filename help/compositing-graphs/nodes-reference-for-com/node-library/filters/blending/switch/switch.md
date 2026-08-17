---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Usate il nodo Switch per passare da una texture di input a un’altra in base a una maschera per la selezione di texture condizionale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cambia
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# Cambia

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/switch-1.png){width="128px"}

![](../../../../../../assets/switch-grayscale.png){width="128px"}

## Switch (scala di grigi)

**Ingresso:** *Filtri/Fusione*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Un semplice nodo switch a 2 posizioni. Restituisce Input 1 o Input 2 in base all&#39;impostazione del parametro Switch. Risultato non modificato. Per una versione più avanzata, vedere [Multi Switch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).

Molto utile per esporre una scelta booleana (Vero/Falso) in un grafico, in cui è necessario solo un singolo pulsante e non un elenco a discesa complesso per un&#39;intera selezione di opzioni.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usare &quot;Switch&quot; per gli ingressi colore, &quot;Switch Greyscale&quot; per gli ingressi scala di grigi.

## Parametri

### Input

* **Input 1 (True)**: *Input a colori o in scala di grigi*
* **Input 2 (False)**: *Input a colori o in scala di grigi*

### Parametri

* **Switch**: *False/True* Consente di passare dall&#39;input 1 (True) all&#39;input 2 (False).

## Immagini di esempio

</td>
</tr>
</table>
