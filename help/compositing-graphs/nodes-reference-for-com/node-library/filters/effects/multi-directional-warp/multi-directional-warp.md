---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# Alterazione multidirezionale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## Alterazione multidirezionale (scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Alterazione multidirezionale applica [Alterazione direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) più volte in direzioni opposte, mentre la texture spostata rimane al suo posto. Differisce dall&#39;Alterazione direzionale standard in quanto può spingere in più direzioni, mentre la versione atomica ne consente solo una. In questo modo viene risolto il problema classico per cui Alterazione direzione sembra sempre allontanare troppo l’immagine in un’unica direzione, invece di funzionare lungo più direzioni o assi.

Differisce principalmente da [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) in quanto è leggermente più limitato: la direzione dell&#39;alterazione è controllata solo tramite parametri e non può essere impostata tramite una mappa di input. Il vantaggio è che è leggermente più facile da usare e può essere più preciso a seconda del caso d&#39;uso.

## Parametri

### Input

* **Input**: *Input colore/scala di grigio*\
  Mappa di base a cui verrà applicata l’alterazione. Può essere a colori o in scala di grigi.
* **Input intensità**: *Input scala di grigi*\
  La mappa maschera obbligatoria che determina l’intensità dell’effetto di alterazione deve essere in scala di grigi.

### Parametri

* **Intensità**: *0,0 - 20,0*\
  Consente di impostare l’intensità dell’effetto di alterazione e l’ampiezza dell’allontanamento dei pixel.
* **Angolo di alterazione**: *0,0 - 1,0*\
  Consente di impostare l’angolo o la direzione in cui applicare l’effetto Altera.
* **Modalità**: *Media, Max, Min, Catena*\
  Imposta il metodo di fusione per le passate consecutive. Ha effetto solo se Direzioni è 2 o 4!
* **Direzioni**: *1, 2, 4* Imposta il numero di assi di funzionamento dell&#39;alterazione. 1 significa che si muove nella direzione dell&#39;angolo, e l&#39;opposto di quella direzione, 2 significa l&#39;asse dell&#39;angolo, più l&#39;asse perpendicolare, 4 significa gli assi precedenti, più inclinazioni di 45 gradi.

## Immagini di esempio

</td>
</tr>
</table>
