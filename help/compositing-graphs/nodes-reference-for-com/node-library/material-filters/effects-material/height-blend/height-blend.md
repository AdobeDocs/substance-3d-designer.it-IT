---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione di Height per fondere le texture in base alle mappe di altezza per creare transizioni di materiale realistiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Fusione height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend.png){width="128px"}

<b>Tra:</b> Filtri materiali > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Combina due Heightmap in base alle informazioni di height. Genera una mappa di altezza con fusione, ma anche una maschera Bianco e nero che può essere utilizzata altrove.

Questo è utile quando si dispone di due Heightmap di alta qualità da combinare, ma non necessariamente un materiale completo, come è richiesto per [Fusione Height materiale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Primi Height</b> <i>Input scala di grigi</i> |  |
| <b>Height inferiore</b> <i>Input scala di grigi</i> |  |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scostamento Height</b> <i>0.0 - 1.0</i> | Sposta le mappe di altezza in modo che il livello di fusione venga spostato lungo l&#39;asse del height. Questo è il controllo principale per la fusione. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto della fusione, rendendo le transizioni più nitide. |
| <b>Modalità</b> <i>height bilanciato, priorità height inferiore</i> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Opacità di fusione del height in primo piano, determina la dissolvenza in entrata o in uscita. |
