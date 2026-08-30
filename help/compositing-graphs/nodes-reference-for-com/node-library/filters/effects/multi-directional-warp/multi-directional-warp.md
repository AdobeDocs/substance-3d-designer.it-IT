---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Usate il nodo Alterazione multidirezionale per applicare gli effetti di alterazione in più direzioni per la creazione di serie di distorsioni complesse.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterazione multidirezionale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# Alterazione multidirezionale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-color.png)![](multi-directional-warp.resources/multi-directional-warp-grayscalepng.png)

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Alterazione multidirezionale applica [Alterazione direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) più volte in direzioni opposte, mentre la texture spostata rimane al suo posto. Differisce dall&#39;Alterazione direzionale standard in quanto può spingere in più direzioni, mentre la versione atomica ne consente solo una. In questo modo viene risolto il problema classico per cui Alterazione direzione sembra sempre allontanare troppo l’immagine in un’unica direzione, invece di funzionare lungo più direzioni o assi.

Differisce principalmente da [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) in quanto è leggermente più limitato: la direzione dell&#39;alterazione è controllata solo tramite parametri e non può essere impostata tramite una mappa di input. Il vantaggio è che è leggermente più facile da usare e può essere più preciso a seconda del caso d&#39;uso.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Input colore/scala di grigi</i> | Mappa di base a cui verrà applicata l’alterazione. Può essere a colori o in scala di grigi. |
| <b>Input intensità</b> <i>Input scala di grigi</i> | La mappa maschera obbligatoria che determina l’intensità dell’effetto di alterazione deve essere in scala di grigi. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 20.0</i> | Consente di impostare l’intensità dell’effetto di alterazione e l’ampiezza dell’allontanamento dei pixel. |
| <b>Angolo di alterazione</b> <i>0.0 - 1.0</i> | Consente di impostare l’angolo o la direzione in cui applicare l’effetto Altera. |
| <b>Modalità</b> <i>Media, Max, Min, Catena</i> | Imposta il metodo di fusione per le passate consecutive. Ha effetto solo se Direzioni è 2 o 4! |
| <b>Indicazioni</b> <i>1, 2, 4</i> | Consente di impostare il numero di assi di funzionamento dell’alterazione. 1 significa che si muove nella direzione dell&#39;angolo, e l&#39;opposto di quella direzione, 2 significa l&#39;asse dell&#39;angolo, più l&#39;asse perpendicolare, 4 significa gli assi precedenti, più inclinazioni di 45 gradi. |
