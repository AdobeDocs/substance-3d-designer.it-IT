---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: Usa il nodo Multi-angolo a Albedo per estrarre le mappe di albedo da immagini acquisite da più angoli per ottenere colori di materiale puliti.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da multi-angolo a Albedo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# Da multi-angolo a Albedo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-albedo.resources/multi-angle-to-albedo.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo tenta di rimuovere tutte le informazioni di illuminazione da una serie di fotografie/scansioni di input scattate con angoli di illuminazione diversi. Combina tutti i campioni in un’unica immagine in modo da essere il più possibile neutra rispetto all’illuminazione e quindi corretta da PBR.

Tenete presente che più campioni avete e più grande è la differenza nell’angolo di illuminazione, maggiore sarà il successo. A partire da quattro campioni, dovrebbe essere possibile ottenere risultati pressoché perfetti, a seconda delle immagini di input. Le immagini di input devono essere scattate con un treppiede e avere differenze minime o idealmente nulle, a eccezione dell’illuminazione da un’angolazione diversa!

>[!NOTE]
>
> Per la versione Normalmap di questo nodo, vedere [Da multiangolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md). Se desiderate pre-elaborare i vostri input, [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) e [Multi Clona /Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) possono essere utili, in quanto sono destinati a essere combinati con questi nodi.
> 
> [Il post del blog &quot;Il tuo smartphone è uno scanner di materiali&quot; illustra questo processo un po&#39; meglio.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input 1-8</b> <i>Input colore</i> | Il numero di input è determinato dal parametro Quantità campioni. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Quantità di campioni</b> <i>2 - 8</i> | Imposta il numero di campioni (input) da utilizzare nell&#39;elaborazione. |
