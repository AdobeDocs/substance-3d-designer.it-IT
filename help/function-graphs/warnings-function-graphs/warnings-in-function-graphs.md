---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/warnings-in-function-graphs.html"
breadcrumb-title: ''
description: Consulta le avvertenze nei grafici delle funzioni di Substance 3D Designer e scopri come risolvere i problemi comuni.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Warnings in function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avvertenze nei grafici delle funzioni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---


# Avvertenze nei grafici delle funzioni

In questa pagina sono elencati gli avvisi e i messaggi di errore che possono essere attivati da [grafici di funzione](../../function-graphs/function-graphs.md) in Substance 3D Designer e sono disponibili procedure di risoluzione dei problemi comuni per ciascuno di essi.

Gli avvisi vengono visualizzati nella descrizione comandi dell&#39;icona di avviso per la risorsa grafico nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) e nell&#39;angolo inferiore sinistro della [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) se il grafico è caricato.\
Se la funzione è *applicata a un parametro* in un [grafico di Substance](../../compositing-graphs/substance-compositing-graphs.md), qualsiasi avviso genererà l&#39;avviso &quot;*La funzione del parametro [x] presenta alcuni errori*&quot; generati per tale parametro.

## ![(errore)](warnings-in-function-graphs.resources/error.svg) Nessun nodo di output definito

Per la funzione non è stato definito alcun nodo di output.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg) Soluzione**

Selezionare qualsiasi nodo nel grafico che genera un valore il cui tipo corrisponde al tipo previsto per questa funzione, se presente, quindi fare clic su RMB e selezionare l&#39;opzione **Imposta come nodo di output** nel menu di scelta rapida.\
Il nodo di output di un grafico a funzioni è colorato in *arancione*.

>[!NOTE]
>
> Se una funzione ha un tipo di valore di output previsto, una nota nell&#39;angolo inferiore sinistro della [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) ti consente di conoscere tale tipo.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-output.gif)

</td>
</tr>
</table>

### ![(errore)](warnings-in-function-graphs.resources/error.svg) Il nodo di output corrente restituisce un valore di tipo *x*

Il nodo di output della funzione restituisce un valore il cui tipo non corrisponde al tipo di valore di output previsto per tale funzione.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg) Soluzione**

Selezionare qualsiasi nodo nel grafico che genera un valore il cui tipo corrisponde al tipo previsto per questa funzione, quindi fare clic su RMB e selezionare l&#39;opzione **Imposta come nodo di output** nel menu di scelta rapida.\
Il nodo di output di un grafico a funzioni è colorato in *arancione*.

>[!NOTE]
>
> Se una funzione ha un tipo di valore di output previsto, una nota nell&#39;angolo inferiore sinistro della [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) ti consente di conoscere tale tipo.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-output-type.gif)

</td>
</tr>
</table>

### ![(errore)](warnings-in-function-graphs.resources/error.svg) Alcuni nodi Get non hanno un nome di variabile

Per uno o più nodi [Get](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) è stata lasciata vuota la proprietà <b>Get...</b>, quindi non fare riferimento a nessuna variabile.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg) Soluzione**

Immettere una stringa corrispondente al nome di una variabile *disponibile nell&#39;ambito della funzione* nella proprietà **Get...** dei nodi Get che generano questo avviso.

>[!NOTE]
>
> La stringa di input è *visualizzata nel nodo*, il che semplifica la ricerca di nodi con valori vuoti.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-empty-get.gif)

</td>
</tr>
</table>

### ![(errore)](warnings-in-function-graphs.resources/error.svg) Alcuni nodi Set non hanno un nome di variabile

Per uno o più nodi [Set](../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) è stata lasciata vuota la proprietà **Set**, pertanto non fare riferimento a nessuna variabile.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg) Soluzione**

Immettere una stringa nella proprietà **Set** dei nodi Set che generano questo avviso.

>[!NOTE]
>
> La stringa di input è *visualizzata nel nodo*, il che semplifica la ricerca di nodi con valori vuoti.

>[!NOTE]
>
> Se la stringa *non* corrisponde ad alcuna variabile disponibile nell&#39;ambito della funzione, viene creata una *nuova variabile* all&#39;interno di tale ambito e denominata in base alla stringa.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-func-empty-set.gif)

</td>
</tr>
</table>
