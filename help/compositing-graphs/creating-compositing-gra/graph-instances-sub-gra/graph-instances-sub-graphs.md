---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Utilizzate le istanze e i grafici secondari del grafico per creare componenti grafici riutilizzabili e flussi di lavoro di materiale modulare.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Istanze e grafici secondari del grafico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# Istanze e grafici secondari del grafico

![](graph-instances-sub-graphs.resources/sub-graph.png)

Le istanze del grafico sono nodi che <b>fanno riferimento a un altro grafico</b>. Un grafico a cui fa riferimento un nodo di istanza in un grafico host può essere denominato <b>grafico secondario</b> del grafico host.

L’uso delle istanze rende un grafico riutilizzabile più volte in uno o più grafici, anche in pacchetti diversi.

## Perché utilizzare le istanze dei grafici?

<b>Suddividere i grafici in più grafici secondari</b> consente di lavorare *molto* in modo più efficiente<b>.</b>

Ogni volta che si duplica una catena di nodi in Designer, è possibile dividere tale catena in un grafico secondario per semplificarne il riutilizzo e l&#39;aggiornamento.

>[!NOTE]
>
> Nella sezione [Grafici di Substance di esempio](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) di questa documentazione è disponibile un file di progetto che illustra una semplice configurazione di un sottografo per un filtro *personalizzato*.

### Come si crea un’istanza di un grafico?

Trascinare un grafico A da Esplora risorse in un altro grafico B per creare un <b>nodo di istanza</b> che faccia riferimento al grafico A.

I nodi possono essere rapidamente divisi in un nuovo grafico selezionando i nodi e utilizzando &quot;Crea grafico da selezione&quot; nel menu di scelta rapida. Viene quindi richiesto di impostare l&#39;identificatore del nuovo grafico, che deve essere univoco.

Si noti che se i nodi selezionati erano connessi ad altri nodi nel grafico, è necessario creare anche nodi [Input](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) e [Output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) nel nuovo grafico per trasferire queste connessioni al grafico secondario.

Inoltre, la sostituzione dei nodi originali con un nodo di istanza che fa riferimento al nuovo grafico deve essere eseguita manualmente in seguito.

Infine, dovrai decidere se il grafico secondario deve essere esposto agli utenti quando pubblichi il progetto in un file SBSAR condivisibile. Vedere il parametro &#39;Exposed in SBSAR&#39; nelle [proprietà del grafico](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Una parola sull&#39;ereditarietà

Un altro vantaggio o l&#39;utilizzo di grafici secondari è che ogni istanza di un grafico secondario può <b>adattarsi al contesto</b> in cui viene utilizzata. In altre parole, due istanze di uno stesso grafico possono avere risoluzioni di output, profondità di bit e modalità di suddivisione in porzioni diverse.

Si tratta di un <b>concetto essenziale</b> per lavorare sui grafici e ti consigliamo vivamente di ottenere ulteriori informazioni sull&#39;[ereditarietà nei grafici Substance](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) quando sei pronto per utilizzare le istanze in modo più avanzato.

Si noti che, mentre i concetti di istanza e grafico secondario del grafico si applicano anche ai grafici delle funzioni Substance, l&#39;ereditarietà, come discusso in quella pagina, si applica solo ai grafici Substance.

### Posso aggiungere le mie istanze grafiche alla libreria dei nodi?

<b>Sì, è possibile </b>ma richiede una configurazione specifica. Ulteriori informazioni sono disponibili nella pagina [Gestione di contenuti e filtri personalizzati](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) di questa documentazione.

### È possibile esaminare il grafico di origine di un&#39;istanza del grafico?

![(tick)](graph-instances-sub-graphs.resources/check.svg) Sì e *solo* per le istanze di grafici caricati da un **file Substance 3D (SBS)**. Questi nodi di istanza hanno un&#39;etichetta *rosso scuro*.\
Fare clic con il pulsante destro del mouse sul nodo per aprire il relativo menu di scelta rapida e selezionare l&#39;opzione **Apri riferimento**.

>[!NOTE]
>
> Durante il controllo del grafico di origine, puoi utilizzare i dati di input del grafico dell&#39;istanza se l&#39;opzione **Modifica in contesto** è *selezionata* nella sezione **Grafico** delle [Preferenze](../../../interface/preferences-window/preferences-window.md).

![(meno)](graph-instances-sub-graphs.resources/forbidden.svg) È *impossibile* ispezionare i grafici caricati dalle istanze **della risorsa Substance 3D (SBSAR)**, poiché sono già compilati. È possibile caricare la risorsa solo nel pannello **Esplora risorse** per esaminare l&#39;elenco dei grafici esposti e i relativi parametri. Questi nodi di istanza hanno un&#39;etichetta *verde*.\
Fare clic con il pulsante destro del mouse sul nodo per aprire il relativo menu di scelta rapida e selezionare l&#39;opzione **Carica pacchetto**.

>[!NOTE]
>
> **Nodi atomici**
> 
> I nodi *Atomic* sono implementati direttamente tramite codice nel motore di Substance e sono *non* istanze di grafici, da cui il nome atomic: sono i *blocchi predefiniti più piccoli* per *tutti* gli altri nodi in [grafici di Substance](../../../compositing-graphs/substance-compositing-graphs.md).
