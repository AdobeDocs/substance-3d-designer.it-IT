---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exposing-parameters-in-mdl-graphs.html"
breadcrumb-title: ''
description: Scopri come esporre i parametri nei grafici MDL per rendere i materiali personalizzabili e riutilizzabili in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exposing parameters in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Esposizione dei parametri nei grafici MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Esposizione dei parametri nei grafici MDL

Questa pagina spiega il processo di esposizione dei parametri nei grafici MDL in modo che possano essere collegati ai valori e alle texture forniti da *altri nodi* nel grafico o da *origini esterne*.

![Stato esposto degli input del nodo](../../assets/mdl-node-inputs-hl.png "Stato esposto degli input del nodo")

*Stato esposto degli input del nodo*

## Esposizione degli input del nodo

Nella maggior parte dei casi, i *connettori di input* delle proprietà di un nodo possono essere esposti in modo che il relativo *valore sia impostato da altri nodi* nel grafico. Questa è una parte *critica* di qualsiasi flusso di lavoro nei grafici MDL e deve essere ben compresa.

Quando si seleziona un nodo nella <b>visualizzazione Grafico</b>, le relative proprietà vengono visualizzate nel pannello <b>Proprietà</b>. La maggior parte delle proprietà è elencata con un set di pulsanti a destra della relativa etichetta:

* **![](../../assets/mdl-expose-new-node.png)Copia il valore in un nuovo nodo e collegalo a questo parametro**: crea un *connettore di input* per questa proprietà e lo connette a un *nuovo nodo* che genera il valore corrente di questa proprietà
* **![](../../assets/mdl-expose-new-input.png)Crea un pin di input per questo parametro**: crea un *connettore di input* per questa proprietà
* **![](../../assets/mdl-expose-reset.png)Reimposta il parametro sul valore predefinito**: quando nessun valore è connesso al connettore di input della proprietà, reimposta il valore predefinito

![](../../assets/mdl-expose-input.gif)

*Manipolazione degli input del nodo*

Se si fa clic su uno dei primi due pulsanti, al nodo verrà aggiunto un *connettore di input digitato*. Le proprietà del nodo reagiscono allo *stato connessione* del connettore:

* **Non connesso**: il parametro è ancora modificabile nel pannello **Proprietà** e il valore immesso in questo pannello è *applicato*
* **Connesso**: il parametro non è più modificabile nel pannello **Proprietà**, il valore immesso in questo pannello è *sostituito* dal valore ricevuto dal *connettore di input* e non è possibile ripristinare il valore predefinito della proprietà

È possibile *rimuovere* il connettore di input facendo nuovamente clic sul pulsante **Crea un pin di input per questo parametro**. A questo punto, il valore della proprietà torna al valore impostato nel pannello **Proprietà**.

![Parametri del nodo esposti](../../assets/mdl-exposed-float-hl.png "Parametri del nodo esposti")

*Parametri del nodo esposti*

## Esposizione degli input del grafico

Nel grafico MDL, l&#39;esposizione di un parametro al livello del grafico, ovvero, in modo che appaia come un parametro di input del materiale MDL, viene eseguita esponendo il nodo che produce il valore.

I nodi che possono essere esposti dispongono di un&#39;opzione <b>Esposizione</b> nel menu di scelta rapida. Nella maggior parte dei casi, si tratta di nodi che generano un valore o dati quali coordinate di virgola mobile, colore o texture.

Opzione ![&quot;Esposizione&quot; nel menu contestuale di un nodo](../../assets/mdl-expose-float-menu-hl.png "&quot;Esposizione&quot; nel menu contestuale di un nodo")

Opzione *&quot;Esposizione&quot; nel menu contestuale di un nodo*

Il parametro esposto è configurato direttamente nel *nodo esposto*, non nelle proprietà del grafico. Le proprietà dei parametri esposti sono le seguenti:

* <b>Identificatore</b>: nome univoco del parametro di input nel grafico corrente
* <b>Valore predefinito</b>: valore predefinito per questo parametro. Può anche essere utilizzato come *anteprima* dell&#39;aspetto che avrà il parametro di input in Designer. Le proprietà <b>Nome visualizzato</b>, <b>Nel gruppo</b> e <b>Intervalli</b> vengono utilizzate per ottenere un&#39;anteprima il più possibile accurata
* <b>Intervalli</b>:
  * *Intervallo sfumato*: imposta l’intervallo predefinito del widget utilizzato per visualizzare questo parametro, ad esempio un cursore. Questa proprietà esiste solo a scopo di interfaccia e i valori che si trovano oltre l’intervallo soft possono essere immessi manualmente
  * *Intervallo rigido*: imposta l&#39;intervallo di valori accettati per questo parametro. I valori al di sotto dell’intervallo vengono bloccati al valore minimo, mentre i valori al di sopra dell’intervallo vengono bloccati al valore massimo. I valori predefiniti e soft dell&#39;intervallo del parametro sono *regolati automaticamente* per adattarsi a questo intervallo.
* <b>Descrizione</b>: descrizione del parametro
* <b>Nel gruppo</b>: il gruppo di parametri a cui appartiene questo parametro di input. Se non è vuoto, il parametro verrà visualizzato in Designer come parte di una sezione comprimibile dal nome del gruppo
* <b>Nome visualizzato</b>: il nome del parametro visualizzato nell&#39;interfaccia
* <b>Nascosto</b>: se impostato su True, il parametro non è visibile negli input del grafico e nelle proprietà del materiale MDL
* <b>Tipo gamma</b>: gamma da utilizzare per il campionamento dei valori da una texture collegata a questo parametro
* <b>Visibile per impostazione predefinita</b>: imposta la visibilità di questo parametro nelle integrazioni MDL nei casi in cui alcuni parametri potrebbero essere nascosti
* <b>Modificatore di tipo</b>: imposta se il valore è uniforme o variabile. Quando è impostato su auto, il parametro eredita questa proprietà dall’input (ad esempio, per un valore Float: uniforme se connesso a un valore Float, variabile se connesso a una texture)
* <b>Utilizzo di Sampler</b>: identificatore dell&#39;utilizzo del parametro, utilizzato per *connettere la texture appropriata* s quando più output sono connessi contemporaneamente a un materiale MDL. Ad esempio, quando si connette un [grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md) a un materiale MDL nella vista 3D, le texture vengono collegate agli input corretti in base agli identificatori di utilizzo corrispondenti.

>[!WARNING]
>
> Mentre gli input del grafico sono configurati come configurati a livello *nodo*, il loro ordine è gestito a livello *grafico* nella sezione **Input grafico** delle [proprietà del grafico](../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md).

![Esposizione di nodi negli input del grafico](../../assets/mdl-expose-parameter.gif "Esposizione di nodi negli input del grafico")

*Esposizione di nodi negli input del grafico*
