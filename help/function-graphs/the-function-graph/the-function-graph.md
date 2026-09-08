---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: Informazioni sui grafici delle funzioni Substance in Designer per la creazione di funzioni personalizzate e reti di nodi riutilizzabili.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Grafico della funzione Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Somiglianze con un grafico a Substance

A prima vista, il grafico della funzione Substance è molto simile a quello della Substance e il flusso di lavoro è quasi lo stesso.

![Substance grafico funzioni](../../assets/image2015-12-18-11-29-28.png "Substance grafico funzioni")

## La navigazione è simile

Nel grafico della funzione Substance, è possibile creare e organizzare i nodi nello stesso modo in cui si creano in un grafico a Substance.

è possibile accedere ai nodi nello stesso modo:

* Dalla libreria
* premendo barra spaziatrice o tasto Tab
* facendo clic con il pulsante destro del mouse e utilizzando il menu Aggiungi nodo

### Flusso di lavoro simile

Come nel grafico delle Substance, costruirete la vostra funzione concatenando serie di nodi, ciascuno dei quali usando il risultato generato da quello(i) precedente(i).

L&#39;output definirà il valore di un parametro o l&#39;output del nodo di elaboratore pixel.

## Differenze con un grafico a Substance

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### I nodi

I nodi disponibili nel grafico della funzione Substance sono completamente diversi da quelli che si incontrerebbero in un grafico della Substance.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Elenco dei nodi del grafico della funzione Substance](../../assets/image2015-12-18-13-46-55.png "Elenco dei nodi del grafico della funzione Substance")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### L&#39;output

Contrariamente ai grafici a Substance, una funzione può avere un solo output.

Un altro punto da notare è che non esiste un nodo di output specifico in cui collegare il risultato finale. È invece possibile contrassegnare direttamente come output il nodo che genera il risultato previsto:

</td>
<td style="border: 0;" valign="top">

![Nodo di output del grafico a funzioni Substance](../../assets/image2015-12-18-13-49-43.png "Nodo di output del grafico a funzioni Substance")

</td>
</tr>
</table>

#### Come definire il nodo di output?

Per definire l&#39;output, fare clic con il pulsante destro del mouse sul nodo che genera l&#39;output previsto e scegliere *Imposta come nodo di output:*

![Definizione del nodo di output](../../assets/setoutputnode.gif "Definizione del nodo di output")

>[!WARNING]
>
> <b>Verificare il tipo di risultato generato</b>
> 
> Se si nota che *Imposta come nodo di output* è disattivato, il valore generato dal nodo è diverso dal valore previsto dal parametro o dall&#39;elaboratore pixel.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Per quanto riguarda i grafici a Substance, potete importare funzioni create in un altro grafico. Per aprire il grafico di riferimento, fare clic con il pulsante destro del mouse su di esso e scegliere &quot;Apri riferimento&quot;:

</td>
<td style="border: 0;" valign="top">

![Apri grafico della funzione Substance con riferimento](../../assets/image2017-6-27-10-44-55.png "Apri grafico della funzione Substance con riferimento")

</td>
</tr>
</table>

Se disponi di un file sbs contenente più funzioni, puoi trascinarlo direttamente in un grafico a funzioni Substance e scegliere la funzione che desideri importare nell’elenco visualizzato:

![Rilasciare il grafico della funzione Substance dal pacchetto](../../assets/sbsdrag.gif "Rilasciare il grafico della funzione Substance dal pacchetto")
