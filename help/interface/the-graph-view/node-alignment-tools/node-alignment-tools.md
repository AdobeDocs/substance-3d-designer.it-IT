---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: Utilizza gli strumenti di allineamento dei nodi per organizzare e allineare i nodi nella vista del grafico per grafici più nitidi e leggibili.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Strumenti di allineamento dei nodi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# Strumenti di allineamento dei nodi

![Barra degli strumenti di allineamento dei nodi](node-alignment-tools.resources/node-alignment-toolbar.png "Barra degli strumenti di allineamento dei nodi"){zoomable="yes"}

Gli strumenti di allineamento dei nodi consentono di disporre i nodi nei grafici per migliorarne la leggibilità e l’esperienza di creazione. Offrono azioni per allineare i nodi, distribuirli uniformemente e agganciarli alla griglia.

Agiscono solo sui <b>nodi attualmente selezionati</b>.

>[!NOTE]
>
> Scelte rapide da tastiera
> 
> Alcune azioni dispongono di scelte rapide da tastiera per un accesso rapido: H, V e S. Vengono visualizzate tra parentesi nell&#39;elenco di azioni seguente.
> 
> Si noti che queste scelte rapide da tastiera sostituiranno qualsiasi [scelta rapida da tastiera assegnata ai nodi](../../../interface/preferences-window/preferences-window.md).

## Allineamenti

I nodi possono essere allineati orizzontalmente e verticalmente, con tre modalità per ogni asse:

### Allineamenti orizzontali

<b>![](node-alignment-tools.resources/node-alignment-h-left.png) a sinistra:</b> Allineare il lato sinistro dei nodi selezionati al lato sinistro del nodo più a sinistra.

<b>![](node-alignment-tools.resources/node-alignment-h-center.png) Centro (H):</b> Allineare il centro orizzontale dei nodi selezionati al centro orizzontale del rettangolo di selezione che li racchiude.

<b>![](node-alignment-tools.resources/node-alignment-h-right.png) Destra:</b> Allineare il lato destro dei nodi selezionati al lato destro del nodo più a destra.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: a sinistra](node-alignment-tools.resources/node-alignment-left.gif "Strumenti di allineamento dei nodi: a sinistra"){zoomable="yes"}

*Sinistra*

</td>
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: center](node-alignment-tools.resources/node-alignment-center.gif "Strumenti di allineamento dei nodi: center"){zoomable="yes"}

*Centro*

</td>
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: a destra](node-alignment-tools.resources/node-alignment-right.gif "Strumenti di allineamento dei nodi: a destra"){zoomable="yes"}

*Destra*

</td>
</tr>
</table>

### Allineamenti verticali

<b>![](node-alignment-tools.resources/node-alignment-v-top.png) In alto:</b> Allineare il lato superiore dei nodi selezionati al lato superiore del nodo superiore.

<b>![](node-alignment-tools.resources/node-alignment-v-middle.png) Centro (V):</b> Allineare il centro verticale dei nodi selezionati al centro verticale del rettangolo di selezione che li racchiude.

<b>![](node-alignment-tools.resources/node-alignment-v-bottom.png) In basso:</b> Allineare il lato inferiore dei nodi selezionati al lato inferiore del nodo inferiore.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: top](node-alignment-tools.resources/node-alignment-top.gif "Strumenti di allineamento dei nodi: top"){zoomable="yes"}

*Primi*

</td>
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: mezzo](node-alignment-tools.resources/node-alignment-middle.gif "Strumenti di allineamento dei nodi: mezzo"){zoomable="yes"}

*Centro*

</td>
<td style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: in basso](node-alignment-tools.resources/node-alignment-bottom.gif "Strumenti di allineamento dei nodi: in basso"){zoomable="yes"}

*Inferiore*

</td>
</tr>
</table>

### Impilamento

L&#39;<b>opzione ![](node-alignment-tools.resources/node-alignment-stack.png) dello stack </b> consente di <b>evitare sovrapposizioni</b> durante l&#39;utilizzo degli allineamenti. È attivata per impostazione predefinita.

Quando questa opzione è attivata, i nodi verranno spostati il più possibile nella posizione di riferimento fino a quando non entreranno in conflitto con un altro nodo nella selezione. In questo modo, vengono impilati nell&#39;asse selezionato con un margine di una cella della griglia media tra ogni nodo.

![Strumenti di allineamento dei nodi: stacking](node-alignment-tools.resources/node-alignment-stacking.gif "Strumenti di allineamento dei nodi: stacking"){zoomable="yes"}

## Distribuzioni

I nodi possono essere distribuiti uniformemente tra i nodi a ogni estremità della selezione corrente sull&#39;asse desiderato.

<b>![](node-alignment-tools.resources/node-alignment-distribute-h.png) orizzontalmente:</b> nodi sono distribuiti uniformemente tra i nodi più a sinistra e più a destra della selezione.

<b>![](node-alignment-tools.resources/node-alignment-distribute-v.png) in verticale:</b> nodi vengono distribuiti uniformemente tra i nodi più in alto e quelli più in basso nella selezione.

Le distribuzioni mirano a <b>spaziatura uniforme</b> tra i nodi, indipendentemente dalle loro dimensioni.

Quando più nodi hanno i loro centri perfettamente allineati sull&#39;asse selezionato, restano e vengono <b>trattati come uno</b> nella distribuzione. Il *più grande* dei nodi allineati viene utilizzato per calcolare la spaziatura uniforme.

Quando la dimensione totale dei nodi selezionati è maggiore dello spazio disponibile sull&#39;asse selezionato, è possibile che si verifichi una sovrapposizione.

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: distribuzione orizzontale](node-alignment-tools.resources/node-alignment-distribute-h.gif "Strumenti di allineamento dei nodi: distribuzione orizzontale"){zoomable="yes"}

*Orizzontalmente*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: distribuzione verticale](node-alignment-tools.resources/node-alignment-distribute-v.gif "Strumenti di allineamento dei nodi: distribuzione verticale"){zoomable="yes"}

*Verticalmente*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## Aggancio alla griglia

L&#39;azione <b>Aggancia (S) ![](node-alignment-tools.resources/node-alignment-snap.png)</b> sposta ciascun nodo selezionato in modo che il relativo angolo superiore sinistro si trovi sul punto più vicino sulla griglia media.

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Strumenti di allineamento dei nodi: aggancio alla griglia](node-alignment-tools.resources/node-alignment-snapping.gif "Strumenti di allineamento dei nodi: aggancio alla griglia"){zoomable="yes"}

</td>
</tr>
</table>
