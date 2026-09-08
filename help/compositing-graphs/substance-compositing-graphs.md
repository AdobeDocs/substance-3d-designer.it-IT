---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: Scoprite come creare Substance di grafici di composizione in Substance 3D Designer per texture procedurali e flussi di lavoro dei materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grafici Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Grafici Substance

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../assets/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[I grafici Substance](https://substance3d.adobe.com/) sono il tipo principale di grafico creato in Substance 3D Designer. Il loro scopo è <b>generare ed elaborare dati di immagini 2D</b> che non siano vincolati a una risoluzione, un colore o una forma impostata. Sono intesi come strumenti di elaborazione e generazione delle immagini estremamente versatili, non solo come risultati statici preimpostati.

I risultati possono presentarsi sotto forma di semplici pattern in bianco e nero, di filtri che vengono eseguiti solo su altre immagini e non generano contenuti di per sé, o anche di materiale procedurale completo con più canali.

I grafici a Substance sono[il tipo di grafico più supportato](../getting-started/overview/overview.md) e possono essere esportati e utilizzati in numerosi flussi di lavoro diversi.

</td>
</tr>
</table>

## Esempi

Di seguito sono riportati alcuni esempi tipici di casi di utilizzo comuni.

+++Forma semplice
![Forma semplice nel grafico della Substance](../assets/simpleshape.png "Forma semplice nel grafico della Substance"){width="512px"}



Una semplice forma maschera per una decalcomania viene creata generando[un testo](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) e una [forma disco](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md), [estraendo il bordo](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md) dal disco e infine [unendoli](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) prima di impostarli come [output](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

Il testo con il numero o il thickness del bordo può essere esposto esternamente per rendere questo grafico più dinamico.

+++

+++Filtro di regolazione
![Filtro di regolazione nel grafico della Substance](../assets/simplefilter.png "Filtro di regolazione nel grafico della Substance"){width="512px"}



Un grafico di filtro prende una mappa normale come [input](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)(con un&#39;anteprima personalizzata), [la converte in curvatura](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) e quindi [regola il contrasto](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) per creare una maschera di bordi convessi come [output](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

I valori di contrasto impostati nell’istogramma possono essere esposti, rendendo questo un filtro semplice ma utile in combinazione con lo slot di input dinamico.

+++

+++Materiale completo
![Materiale completo nel grafico della Substance](../assets/simplematerial.png "Materiale completo nel grafico della Substance"){width="512px"}



Un grafico più complicato[fonde due Materiali di base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md). Un [Materiale di base](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) è semplice, l&#39;altro utilizza alcuni input personalizzati per aggiungere interesse. Viene utilizzata una maschera per determinare quale dei due materiali viene visualizzato in una posizione prima di essere impostato come [output](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) finale.

In questo esempio vengono utilizzate [modalità di creazione del collegamento](../interface/the-graph-view/link-creation-modes/link-creation-modes.md) per semplificare l&#39;utilizzo di più collegamenti.

+++
