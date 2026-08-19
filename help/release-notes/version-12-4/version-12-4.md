---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-12-4.html"
breadcrumb-title: ''
description: Consulta le note sulla versione per Substance 3D Designer versione 12.4 per informazioni sulle nuove funzioni, i miglioramenti e le correzioni di bug.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 12.4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 1%

---


# Versione 12.4

**Substance 3D Designer 12.4** offre diversi miglioramenti a livello di qualità di vita (uno strumento per ripulire un grafico, utilizzando formule di base per impostare i parametri, un pulsante per generare un valore di inizializzazione casuale, un blocco per le dimensioni, ecc.) e il supporto di Substance grafiche di modelli nell’API Python. Vedere di seguito per ulteriori dettagli su tutte queste modifiche.

Data di pubblicazione: *31 gennaio 2023*

## Miglioramenti alla qualità della vita

### Pulizia dello strumento grafico

Quando modificate il grafico, a volte dovete sperimentare diverse possibilità e collegare/scollegare vari nodi fino al momento in cui ottenete il risultato desiderato. Quindi, alla fine, nel grafico ci sono alcuni nodi che non sono collegati a un output, quindi non hanno alcun impatto sul risultato finale. Questo nuovo strumento consentirà di rilevare ed eliminare automaticamente questi nodi per pulire i grafici prima di finalizzarli. Lo strumento di pulizia è anche disponibile come opzione nelle funzioni dei parametri e può essere avviato sul grafico corrente tramite il pulsante dedicato nella barra degli strumenti Visualizzazione grafico oppure su una selezione di grafici dalla visualizzazione Esplora.

![](../../assets/final-clean.gif){width="640px"}

### Digitare le formule nei campi dei parametri

Non è più necessario utilizzare una calcolatrice o calcolare nella testa quando si desidera immettere valori di parametri specifici. È ora possibile immettere direttamente formule di base come aggiunte, divisioni, moltiplicazioni o sottrazioni quando si imposta un valore numerico per un parametro in [Proprietà](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html) e in altre posizioni dell&#39;applicazione.

![](../../assets/final-formula.gif){width="640px"}

### Pulsanti di accesso rapido nella vista 3D

Nella [vista 3D](../../interface/3d-view/3d-view.md) è stata aggiunta una barra degli strumenti aggiuntiva che corrisponde a tutte le opzioni disponibili nel menu [Visualizza](../../interface/3d-view/3d-view.md), per un rapido accesso a tutte queste opzioni (ad esempio, Wireframe, Griglia, Rettangolo di selezione e così via) come pulsante. È stato inoltre aggiunto un interruttore per mostrare/nascondere la mappa dell&#39;ambiente.

![](../../assets/final-3dview.gif){width="640px"}

### Pulsante per generare un valore di Numero casuale

Ora puoi creare rapidamente diverse variazioni utilizzando un nuovo pulsante per generare il valore di inizializzazione casuale per il grafico, anziché spostare un cursore.

![](../../assets/final-seed.gif){width="640px"}

### Blocca per il widget Dimensione output

Ora puoi bloccare la larghezza e il height delle dimensioni di output per assicurarti di mantenere una dimensione quadrata ed evitare di manipolare i due valori ogni volta che desideri aggiornarli.

![](../../assets/final-lock.gif){width="640px"}

### Trasforma l&#39;input dell&#39;immagine in scala di colori/grigi

Passate rapidamente da un [colore di input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) a un [scala di grigi di input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) tramite il menu di scelta rapida del nodo.

![](../../assets/final-switch.gif){width="640px"}

### Seleziona la puntina su cui si fa clic durante la visualizzazione dell’Editore sfumatura

Nel pannello delle proprietà, se fai clic su una puntina per modificare una sfumatura, ora selezionerai automaticamente la puntina corrispondente nell&#39;[Editore sfumatura](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) visualizzato.

![](../../assets/final-gradient.gif){width="640px"}

### Seleziona nodi a valle

Nuova voce nel menu contestuale [nodo](../../interface/the-graph-view/the-graph-view.md) per selezionare direttamente o indirettamente tutti i nodi connessi all&#39;output dei nodi selezionati. In questo modo si selezionano tutti i nodi interessati dal nodo. Utile per eliminare parte del grafico o rielaborare il layout del grafico.

![](../../assets/final-downstream.gif){width="640px"}

## Aggiornamenti dell’API Python

Questa versione 12.4 offre anche il supporto completo dei grafici dei modelli di Substance tramite l’API Python. Ciò significa che ora disponi di tutti gli strumenti necessari per creare, modificare o valutare i grafici dei modelli di Substance. Per informazioni dettagliate, vedere la documentazione disponibile nel menu Guida del software.

## Note sulla versione

### 12.4.0

*(Rilasciato il 24 gennaio 2023)*

<b>Aggiunto:</b>

* [Vista 3D] Aggiungi pulsanti di accesso rapido per impostare le opzioni di visualizzazione (Wireframe, mappa dell&#39;ambiente, statistiche delle scene, ecc.)
* [Gestione colore] Migliorare la qualità delle LUT 3D al forno in modalità ACE
* [Documentazione] Progetti di esempio per grafici Substance
* [Documentazione] Progetto di esempio per i grafici delle funzioni
* [Explorer] Consente di spostare il grafico e le risorse da un elemento padre a un altro senza chiudere o invalidare i widget
* [Editore sfumatura] Seleziona la puntina su cui hai fatto clic quando visualizzi l’editor della sfumatura
* [Grafico] Aggiungere l&#39;opzione nel menu di scelta rapida di un nodo per selezionare tutti i relativi figli
* [Grafico] Pulisci lo strumento grafico per rilevare e rimuovere i nodi inutilizzati in tutti i tipi di grafico e i grafici delle proprietà
* [Grafico] Trasforma l&#39;input dell&#39;immagine in scala di colori/grigi
* [Parametri] Aggiungere un blocco ai widget integer2
* [Parametri] Consente di digitare formule di base come parametro
* [Substance modello] Attiva/disattiva per passare da valori a icone per i nodi di valori e viceversa
* [UI] Pulsante per generare un valore casuale quando è richiesto un valore di inizializzazione casuale
* [UI] Evidenzia nella vista 3D l’elemento attualmente selezionato nell’Elenco scene
* [UX] Reimposta gli intervalli del cursore quando il loro valore viene reimpostato
* [API] Consenti l’aggiunta di azioni alle barre degli strumenti della visualizzazione grafico
* [API] Consenti di creare, modificare o valutare un grafico del modello di Substance dall’API

<b>Corretto:</b>

* [Vista 3D] Il valore della proprietà &quot;DirectX normale&quot; non è condiviso tra i moduli di rendering
* [Vista 3D] La visualizzazione delle statistiche della scena viene estesa quando la finestra della vista è piccola
* [Vista 3D] La proprietà di visualizzazione Wireframi non viene salvata
* [Contenuto] I parametri del colore Sfocatura radiale non hanno effetto sul canale alfa
* [Localizzazione] Ulteriori cursori e pulsanti vengono visualizzati in Proprietà OpenGL dell&#39;ambiente.
* [MDL]&#x200B;[Substance modello] Arresto anomalo durante l&#39;eliminazione di nodi esposti
* [Preferenze] Il file predefinito\_config non viene mai ricreato se viene eliminato
* [Modello Substance] Parametro di riordinamento in caso di arresto anomalo che non viene visualizzato a livello di istanza
* [API] SDProperty.getDefaultValue() restituisce quasi sempre Nessuno
