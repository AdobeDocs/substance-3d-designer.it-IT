---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/the-graph-view/node-finder.html"
breadcrumb-title: ''
description: Utilizzare Ricerca nodi per individuare e cercare rapidamente i nodi nei grafici Substance per una navigazione efficiente.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node finder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ricerca nodi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 0%

---


# Ricerca nodi

![Barra degli strumenti Ricerca nodi](../../../assets/node-finder-toolbar.png "Barra degli strumenti Ricerca nodi"){zoomable="yes"}

Lo strumento Ricerca nodi consente di eseguire una <b>ricerca di nodi e variabili</b> mediante una query di testo. Tutti i nodi che non corrispondono alla query vengono disattivati per rendere visibili i risultati.

La query può soddisfare uno qualsiasi dei seguenti criteri:

* Identificatore <b>di un grafico</b> a cui fa riferimento un nodo di istanza
* Identificatore <b>di un parametro o di una variabile esposta</b> utilizzato in una funzione dei parametri del nodo
* <b>UID</b> di un nodo (identificatore univoco)
* <b>etichetta</b> di un nodo

La ricerca può attraversare [istanze del grafico](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) in modo ricorsivo, in modo da poter trovare nodi e variabili in [grafici secondari](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md). Se non si è certi del termine esatto da cercare, è disponibile un&#39;opzione di ricerca non definita per applicare una tolleranza alla query.

## Interfaccia

È possibile accedere a Node Finder in due modi:

Nella visualizzazione Grafico, premere <b>Ctrl+F</b> (Windows) / <b>Cmd+F</b> (macOS) per visualizzare la barra degli strumenti Ricerca nodi e impostare automaticamente lo stato attivo sul campo della query. In questo modo è possibile eseguire una ricerca rapidamente.

Nella barra degli strumenti Visualizzazione grafico fare clic sul pulsante <b>Ricerca nodi ![](../../../assets/graph-node-finder.png)</b> per visualizzare la barra degli strumenti Ricerca nodi. Una volta visualizzata, la barra degli strumenti viene chiusa solo facendo clic su questo pulsante.

<b>Esegue la ricerca nei grafici incrociati</b>. In altre parole, una ricerca rimane attiva quando si aprono grafici tramite queste azioni:

* Nodo istanza: apri riferimento nel contesto (Ctrl+E/Cmd+E) (*Nota:* la modifica del grafico nel contesto deve essere abilitata in Modifica > Preferenze > Grafico)
* Processore pixel: funzione Edit (Ctrl+E/Cmd+E)
* Funzione Value Processor: Modifica (CTRL+E/Cmd+E)
* FX-Map: Modifica grafico FX-Map (Ctrl+E/Cmd+E)
* Parametri nodo: funzione Modifica

![Ricerca nodi: analisi dei grafici durante la ricerca](../../../assets/node-finder-traversal.gif "Ricerca nodi: analisi dei grafici durante la ricerca"){zoomable="yes"}

### Query di ricerca

![Campo query di ricerca nodi](../../../assets/node-finder-query-field.png "Campo query di ricerca nodi"){zoomable="yes"}

I termini di ricerca possono essere digitati in questo campo e il pulsante freccia apre un elenco di suggerimenti di query che includono alcune delle variabili disponibili nel contesto corrente.

Ulteriori informazioni sulle query che è possibile eseguire nella sezione [Query di ricerca](#search-query) seguente.

### Tipo di nodo

![Tipo di nodo](../../../assets/node-finder-node-types.png "Tipo di nodo"){zoomable="yes"}

Questa casella combinata consente di filtrare i risultati della ricerca in modo da mantenere solo un tipo specifico di nodi.

Si noti che tutti i nodi di istanza sono dello *stesso tipo* di nodo, ovvero del tipo &#39;instance&#39;, mentre i nodi atomici sono del proprio tipo.

+++Elenchi dei tipi di nodo
L’elenco è contestuale al tipo di grafico corrente.

![Tipi di nodo (composizione)](../../../assets/node-finder-types-compositing.png "Tipi di nodo (composizione)"){zoomable="yes"}



*Tipi di nodo per la composizione dei grafici*

![Tipi di nodo (funzione)](../../../assets/node-finder-types-function.png "Tipi di nodo (funzione)"){zoomable="yes"}



*Tipi di nodo per i grafici delle funzioni*

+++

+++Ricerca di nodi atomici
![Ricerca nodi: ricerca per tipo &#39;Livelli&#39; (composizione)](../../../assets/node-finder-compositing-levels.png "Ricerca nodi: ricerca per tipo &#39;Livelli&#39; (composizione)"){zoomable="yes"}



*Ricerca del tipo di nodo &#39;Livelli&#39; in un grafico a Substance*

+++

+++Ricerca di nodi di istanza
![Ricerca nodi: ricerca per tipo &#39;Instance&#39; (composizione)](../../../assets/node-finder-compositing-instances.png "Ricerca nodi: ricerca per tipo &#39;Instance&#39; (composizione)"){zoomable="yes"}



*Ricerca del tipo di nodo &#39;Instance&#39; in un grafico a Substance*

![Ricerca nodi: ricerca per tipo &#39;Instance&#39; (funzione)](../../../assets/node-finder-functions-instances.png "Ricerca nodi: ricerca per tipo &#39;Instance&#39; (funzione)"){zoomable="yes"}



*Ricerca del tipo di nodo &#39;Instance&#39; in un grafico della funzione Substance*

+++

### Opzioni di ricerca

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Il pulsante <b>Opzioni di ricerca ![](../../../assets/node-finder-search-options.png)</b> consente di aprire un elenco delle impostazioni utilizzate per la ricerca che è possibile attivare e disattivare.

Ulteriori informazioni su queste opzioni sono disponibili nella sezione Opzioni di ricerca riportata di seguito.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Opzioni di ricerca Node Finder](../../../assets/node-finder-search-options-open.png "Opzioni di ricerca Node Finder"){zoomable="yes"}

</td>
</tr>
</table>

## Query di ricerca

Per trovare i nodi, una query di testo viene confrontata con le proprietà dei nodi elencate di seguito.

>[!NOTE]
>
> La query deve essere digitata tenendo presente le seguenti avvertenze:
> 
> * La ricerca non fa distinzione tra maiuscole e minuscole. Ad esempio, &#39;etichetta nodo personale&#39; e &#39;etichetta nodo personale&#39; restituiscono gli stessi risultati.
> * Gli spazi prima e dopo la query vengono ignorati.
> * Non è possibile eseguire più query contemporaneamente nello stesso grafico. Ad esempio, &quot;sfocatura livelli&quot; non corrisponderà a entrambi i nodi &quot;Livelli&quot; e &quot;Sfocatura&quot;. Analogamente, gli operatori logici non sono supportati.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Identificatori del grafico dell’istanza

È possibile trovare [nodi di istanza](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) utilizzando l&#39;<b>identificatore</b> dei grafici a cui fanno riferimento.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Ricerca nodi: ricerca per identificatore grafico](../../../assets/node-finder-functions-identifier.png "Ricerca nodi: ricerca per identificatore grafico"){zoomable="yes"}

*Fare clic sull&#39;immagine per ingrandirla*

</td>
</tr>
</table>

+++Identificatore in Esplora risorse
I grafici sono elencati in base ai relativi identificatori in Esplora risorse.

![Esplora risorse: contenuto pacchetto](../../../assets/explorer-package-simple.png "Esplora risorse: contenuto pacchetto"){zoomable="yes"}



+++

+++Identificatore nella descrizione comando del nodo dell&#39;istanza
La descrizione dei nodi di istanza include l&#39;identificatore del relativo grafico di riferimento.

![Identificatore grafico nella descrizione comandi del nodo dell&#39;istanza](../../../assets/node-finder-compositing-identifier.png "Identificatore grafico nella descrizione comandi del nodo dell&#39;istanza"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Parametri e variabili esposti

È possibile eseguire la ricerca direttamente nell&#39;identificatore di [parametri esposti](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) o in qualsiasi altra variabile.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Ricerca nodi: variabili nodo](../../../assets/node-finder-compositing-variable.png "Ricerca nodi: variabili nodo"){zoomable="yes"}

*Fare clic sull&#39;immagine per ingrandirla*

</td>
</tr>
</table>

+++Suggerimenti per query
Il campo di query può essere espanso per visualizzare un elenco di suggerimenti.

Queste includono [variabili incorporate](../../../function-graphs/variables/system-variables/system-variables.md) disponibili per il tipo di grafico corrente, nonché gli identificatori dei parametri esposti del grafico.

![Suggerimenti per le query di ricerca nodi](../../../assets/node-finder-available-query-suggestions.png "Suggerimenti per le query di ricerca nodi"){zoomable="yes"}



L&#39;identificatore dei parametri esposti può anche essere copiato o modificato direttamente nelle [proprietà del grafico Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md).

![Ricerca nodi: parametri esposti](../../../assets/node-finder-compositing-exposed-parameter.png "Ricerca nodi: parametri esposti"){zoomable="yes"}



*Fare clic sull&#39;immagine per ingrandirla*

+++

+++Ricerca di una variabile da un avviso/errore della console
Quando un grafico presenta errori o avvisi generati da una <b>variabile</b> utilizzata da un nodo, passare a <b>Windows > Console</b> per visualizzare il messaggio di errore/avviso completo che includerà la variabile. È quindi possibile copiare e incollare questa variabile nel campo di query Node Finder per individuare rapidamente il nodo che causa il problema.

Le variabili possono anche essere copiate direttamente dai dati XML nel file SBS utilizzando qualsiasi editor di testo.

![Ricerca nodi: ricerca variabile da avviso/errore console](../../../assets/node-finder-console-identifier.png "Ricerca nodi: ricerca variabile da avviso/errore console"){zoomable="yes"}



+++

+++Ottieni/Imposta nodi
Quando si cerca una variabile in un grafico, inclusi i parametri esposti, la ricerca evidenzierà tutti i nodi in cui un nodo [Get](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) o [Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) utilizza tale variabile in una qualsiasi delle funzioni dei parametri del nodo.

![Ricerca nodi: ricerca di una variabile corrisponde a Recupero nodi che la utilizzano](../../../assets/node-finder-exposed-parameter-01.gif "Ricerca nodi: ricerca di una variabile corrisponde Recupero nodi che la utilizzano"){zoomable="yes"}



+++

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### UID nodo

Ogni nodo di un grafico ha un numero identificativo univoco (UID) che può essere utilizzato per cercare quel nodo.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Ricerca nodi: ricerca per UID](../../../assets/node-finder-compositing-uid-search.png "Ricerca nodi: ricerca per UID"){zoomable="yes"}

*Fare clic sull&#39;immagine per ingrandirla*

</td>
</tr>
</table>

+++Copia dell&#39;UID di un nodo
L&#39;UID di un nodo può essere copiato negli Appunti dal relativo menu di scelta rapida.

L&#39;azione copia l&#39;UID in questo formato:

uid=1234567890

![Ricerca nodi: azione UID del nodo di copia](../../../assets/node-finder-compositing-uid-copy.png "Ricerca nodi: azione UID del nodo di copia"){zoomable="yes"}



+++

+++Ricerca di un UID nodo da un avviso/errore della console
Quando un grafico presenta errori o avvisi generati da un nodo, accedete a Windows > Console per visualizzare il messaggio di errore/avviso completo che includerà l&#39;<b>UID</b> del nodo. Puoi quindi copiare e incollare questo UID nel campo di query Trova nodi per individuare rapidamente il nodo che causa il problema.

Gli UID dei nodi possono anche essere copiati direttamente dai dati XML nel file SBS utilizzando qualsiasi editor di testo.

![Ricerca nodi: ricerca dell&#39;UID del nodo dalla console](../../../assets/node-finder-console-uid.png "Ricerca nodi: ricerca dell&#39;UID del nodo dalla console"){zoomable="yes"}



+++

### Etichetta nodo

I nodi possono essere trovati anche utilizzando le relative etichette.

La ricerca di nodi specifici è particolarmente efficace quando si utilizza l&#39;etichetta esatta con la ricerca fuzzy disattivata.

## Opzioni di ricerca

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Il pulsante <b>Opzioni di ricerca ![](../../../assets/node-finder-search-options.png)</b> consente di attivare/disattivare le modalità <b>ricorsiva</b> e <b>sfocata</b> per la ricerca dei nodi.

Entrambe le opzioni possono essere attivate contemporaneamente.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Opzioni di ricerca Node Finder](../../../assets/node-finder-search-options-open.png "Opzioni di ricerca Node Finder"){zoomable="yes"}

</td>
</tr>
</table>

### Modalità ricorsiva

Abilita questa opzione affinché le ricerche attraversino [istanze del grafico](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) per includere i risultati da [grafici secondari](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

Questa opzione può essere essenziale quando si eseguono operazioni di risoluzione dei problemi grafici, se è necessario trovare un nodo in base all&#39;UID acquisito da un messaggio di avviso o di errore nella Console.

![Ricerca nodi: ricerca ricorsiva](../../../assets/node-finder-recursion-01.png "Ricerca nodi: ricerca ricorsiva"){zoomable="yes"}

*La query a destra evidenzia il nodo di istanza sottostante perché il grafico a cui fa riferimento a sinistra contiene corrispondenze per la query*

+++Esempio 1
![Ricerca nodi: esempio di ricerca ricorsiva 1](../../../assets/node-finder-recursion-01.gif "Ricerca nodi: esempio di ricerca ricorsiva 1"){zoomable="yes"}



Un nodo di istanza fa riferimento a un grafico in cui più nodi corrispondono alla query.

+++

+++Esempio 2
![Ricerca nodi: esempio di ricerca ricorsiva 2](../../../assets/node-finder-recursion-02.gif "Ricerca nodi: esempio di ricerca ricorsiva 2"){zoomable="yes"}



L’attivazione dell’opzione &quot;Ricerca ricorsiva&quot; evidenzia il nodo di istanza che fa riferimento a un grafico in cui un nodo Processore pixel utilizza una variabile che corrisponde alla query.

+++

### Modalità fuzzy

In caso di dubbi sull&#39;ortografia esatta di una query, questa opzione consente di attivare una <b>tolleranza</b> nei risultati.

Si noti che l&#39;utilizzo di questa opzione può causare corrispondenze indesiderate.

![Ricerca nodi: modalità fuzzy](../../../assets/node-finder-functions-fuzzy.png "Ricerca nodi: modalità fuzzy"){zoomable="yes"}
