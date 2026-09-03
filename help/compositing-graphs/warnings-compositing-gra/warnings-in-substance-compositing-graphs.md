---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Consulta le avvertenze nella sezione Substance grafici di composizione e scopri come risolvere problemi ed errori comuni.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avvertenze nei grafici Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Avvertenze nei grafici Substance

In questa pagina sono elencati avvisi ed errori che possono essere attivati da [Substance grafici](../../compositing-graphs/substance-compositing-graphs.md) in Substance 3D Designer e sono disponibili passaggi di risoluzione dei problemi comuni per ciascuno di essi.

Gli avvisi vengono visualizzati nella descrizione comandi dell&#39;icona di avviso per la risorsa grafico nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) e nell&#39;angolo inferiore sinistro della [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) se il grafico è caricato.

## ![(errore)](warnings-in-substance-compositing-graphs.resources/error.svg) Nessun nodo di output definito

Il grafico non dispone di un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Soluzione**

Aggiungete uno o più nodi [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) al grafico e collegate l&#39;output dell&#39;ultimo nodo di un flusso.

>[!NOTE]
>
> I modelli di grafico disponibili nella finestra di dialogo [Nuovo grafico](../creating-compositing-gra/creating-a-substance-compositing-graph.md) presentano nodi di output predefiniti pronti per l&#39;uso.

![Correzione dell&#39;avviso &#39;Nessun nodo di output definito&#39;](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-01.gif "Correzione dell&#39;avviso &#39;Nessun nodo di output definito&#39;"){width="512px"}

### ![(errore)](warnings-in-substance-compositing-graphs.resources/error.svg) La funzione del parametro *[x]* contiene alcuni avvisi

Il [grafico della funzione](../../function-graphs/function-graphs.md) applicato al parametro specificato del nodo specificato presenta almeno un avviso.\
Il parametro del nodo viene specificato tra parentesi quadre dopo l&#39;etichetta del nodo, seguendo il modello Node[Parameter].

E.g. Uniform Color[Colore Di Output], Processore Pixel[Funzione Per Pixel]

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Soluzione**

Individuare il nodo che emette l&#39;avviso in base all&#39;etichetta e al badge di avviso nella [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md), quindi selezionarlo per visualizzarne le proprietà nel pannello [Proprietà](../../interface/properties/properties.md). Individuare il parametro che emette l&#39;avviso e aprirne la funzione facendo clic sul pulsante **Modifica funzione**.

Quindi, valuta gli avvisi elencati nell’angolo in basso a sinistra della vista Grafico e risolvi i problemi. È possibile fare riferimento alla pagina [Avvisi nei grafici delle funzioni](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) per la risoluzione dei problemi relativi agli avvisi riportati nei grafici delle funzioni.

![Correggere l&#39;avviso &#39;La funzione del parametro contiene alcuni avvisi&#39;](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-02.gif "Correggere l&#39;avviso &#39;La funzione del parametro contiene alcuni avvisi&#39;")

### ![(errore)](warnings-in-substance-compositing-graphs.resources/error.svg) I dati a cui si fa riferimento contengono alcuni avvisi

La risorsa a cui fa riferimento un nodo presenta uno o più avvisi. Di seguito sono riportati alcuni nodi che fanno riferimento a una risorsa:

* Un nodo [istanza del grafico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) fa riferimento a un grafico
* Un nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) fa riferimento a una [risorsa Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nodo [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) fa riferimento a una risorsa [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) fa riferimento a una [risorsa Font](../../resources/font-resource/font-resource.md)

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Soluzione**

Nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), individuare la risorsa a cui si fa riferimento e risolvere tutti gli avvisi generati dalla risorsa:

* Per i grafici, fai riferimento ad altri elementi in questa pagina
* Per qualsiasi altro tipo di risorsa, consultare la pagina [Avvisi dalle dipendenze](../../resources/warnings-from-dep/warnings-from-dependencies.md)

![Correzione dell&#39;avviso &#39;I dati di riferimento contengono alcuni avvisi&#39;](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-03.gif "Correzione dell&#39;avviso &#39;I dati di riferimento contengono alcuni avvisi&#39;")

### ![(errore)](warnings-in-substance-compositing-graphs.resources/error.svg) Risorsa di riferimento non trovata

Impossibile trovare la risorsa a cui fa riferimento un nodo nel percorso salvato nel file di [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) (SBS). Di seguito sono riportati alcuni nodi che fanno riferimento a una risorsa:

* Un nodo [istanza del grafico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) fa riferimento a un grafico
* Un nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) fa riferimento a una [risorsa Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Un nodo [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) fa riferimento a una risorsa [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) fa riferimento a una [risorsa Font](../../resources/font-resource/font-resource.md)

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Soluzione**

Per i nodi [istanza del grafico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)

Verificare che il grafico di origine esista nel pacchetto che si trova nel percorso salvato nel relativo attributo **Package**.\
In caso contrario, eliminare il nodo dell&#39;istanza e sostituirlo con un nodo dell&#39;istanza che fa riferimento a un pacchetto valido. In alternativa, puoi ricreare il pacchetto e il grafico a cui fa riferimento il nodo dell&#39;istanza, quindi ricaricare il pacchetto host facendo clic su RMB nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) e selezionando l&#39;opzione **Ricarica** nel menu di scelta rapida.

Per i nodi [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) o [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

Trovare le risorse a cui si fa riferimento nel pannello Esplora risorse e verificarne la presenza nel percorso salvato nell&#39;attributo **Percorso file**.\
In caso contrario, fare clic su RMB sull&#39;elemento della risorsa in Esplora risorse e selezionare l&#39;opzione **Riposiziona...** nel menu di scelta rapida per impostare un nuovo file di destinazione valido per la risorsa.

![Correzione dell&#39;avviso &#39;Risorsa di riferimento non trovata&#39;](warnings-in-substance-compositing-graphs.resources/warnings-in-substance-compositing-graphs-04.gif "Correzione dell&#39;avviso &#39;Risorsa di riferimento non trovata&#39;")

### ![(errore)](warnings-in-substance-compositing-graphs.resources/error.svg) Il nodo di testo utilizza un font non valido

Un nodo [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) fa riferimento a un tipo di carattere che non può essere caricato o analizzato correttamente.

<b>![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Soluzione</b>

Selezionare il nodo [Testo](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) e prendere nota del valore della relativa proprietà <b>Font</b>. Trova il file di origine per il font nel sistema e assicurati che sia *integro*, ad esempio utilizzandolo in un&#39;altra applicazione come un editor di testo. Sostituire il font con un file di font integro secondo necessità o cambiare il nodo Testo in un altro font.
