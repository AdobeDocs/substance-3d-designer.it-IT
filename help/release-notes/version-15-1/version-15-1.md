---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-15-1.html"
breadcrumb-title: ''
description: Consulta le note sulla versione per Substance 3D Designer versione 15.1 per informazioni sulle nuove funzioni, i miglioramenti e le correzioni di bug.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 15.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 15.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: fde9d7a455c1c7b366323c119f4c1f9a2c114952
workflow-type: tm+mt
source-wordcount: '1719'
ht-degree: 0%

---


# Versione 15.1

Substance Designer 15.1 introduce una finestra di creazione del grafico completamente rinnovata con accesso diretto ai campioni, nodi di disturbo migliorati per maggiori possibilità creative, categorie organizzate nel menu dei nodi e molto altro ancora.

*Data di pubblicazione: 11 dicembre 2025*

![Banner Designer 15.1](version-15-1.resources/bannerweb.png)

## Migliorare la creazione di grafici

In questa versione, la [finestra per la creazione del grafico](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) è stata <b>completamente riprogettata</b> per migliorare l&#39;esperienza iniziale dell&#39;utente in Substance 3D Designer. L’obiettivo principale di questo aggiornamento è quello di semplificare il processo di selezione dei modelli, consentendo agli utenti di identificare in modo efficiente il modello più adatto alle loro esigenze.

Le miniature offrono <b>riferimenti visivi</b> immediati per i tipi di materiale desiderati, mentre le descrizioni comandi dettagliate forniscono tutte le informazioni pertinenti. Per una migliore organizzazione, i modelli sono ora classificati in <b>categorie</b> specifiche, ad esempio materiali, filtri ed elaborazioni di scansione.

Sebbene l’interfaccia principale sia stata aggiornata, gli utenti continuano ad avere accesso alle visualizzazioni precedenti, tra cui le opzioni elenco, pacchetti e directory.

[Ulteriori informazioni](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)

![riprogettare la nuova finestra del grafico](version-15-1.resources/newgraph.png){zoomable="yes"}

## Campioni incorporati

Con il lancio della nuova finestra per la creazione del grafico, abbiamo aggiunto una serie di [<b>materiali di esempio</b>](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) direttamente all&#39;interno del software. Questo miglioramento risponde alla tua richiesta di un migliore accesso alle risorse di apprendimento.

![Nuova finestra di creazione del grafico per gli esempi](version-15-1.resources/GraphSample.png){zoomable="yes"}

Per soddisfare questa esigenza abbiamo incluso campioni di materiale come tessuti (tra cui pelle e raso), legno, metallo, plastica, ceramica e altro ancora. Questi esempi hanno lo scopo di aiutarti a iniziare i tuoi progetti con facilità e a conoscere i principali nodi familiari disponibili in Substance 3D Designer

Ogni grafico è <b>annotato</b>, organizzato con cura e contiene un numero minimo di nodi per facilitarne la comprensione.

Potete accedere ai campioni nella categoria &quot;Campioni di materiale&quot; durante la creazione di un nuovo grafico a Substance o direttamente dalla schermata Home utilizzando il pratico pulsante &quot;Vai a campioni&quot;.

Oltre a questi materiali di base, abbiamo fornito anche <b>esempi avanzati</b> per dimostrare come utilizzare le funzionalità <b>FX-map e del processore Pixel</b> in modo più efficace.

[Ulteriori informazioni](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)

![esempio di legno in substance designer](version-15-1.resources/samplegraph.png){zoomable="yes"}

## Nuovi disturbi

I rumori svolgono un ruolo cruciale nella maggior parte dei grafici ed è per questo che ci siamo concentrati su diversi miglioramenti chiave in questa versione per migliorarne la funzionalità e l’usabilità.

Con questo aggiornamento è stato introdotto <b>un migliore supporto per scenari senza suddivisione in porzioni</b>, in modo da garantire che i modelli di disturbo funzionino come previsto senza suddivisione in porzioni obbligatoria. In precedenza, i nodi di disturbo venivano suddivisi in porzioni o producevano risultati errati quando l&#39;Affiancamento veniva disattivato.

La maggior parte dei rumori ora include <b>nuovi parametri</b>, che offrono agli utenti un maggiore controllo creativo. Queste opzioni aggiuntive consentono agli autori dei grafici di regolare l’aspetto e il comportamento del disturbo all’interno dei flussi di lavoro.

Infine, la profondità di bit <b>non è più bloccata a 16 bit</b>. Ora potete ignorare l’impostazione della profondità di bit sulle singole istanze del nodo, per ottenere maggiori dettagli e un intervallo dinamico quando necessario, oppure ottimizzare i grafici per le prestazioni.

Consulta l&#39;elenco completo dei rumori aggiornati nelle [note sulla versione](#release-notes) di seguito.

Esempi: [Cella 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md) [Nuvole 2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/clouds-2/clouds-2.md) [Graffi direzionali](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-scratches/directional-scratches.md) [Rumore di umidità 1](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

![disturbo direzionale](version-15-1.resources/directionaldisorder.gif){zoomable="yes"}

## Gerarchia nel menu dei nodi

Per risolvere il problema di individuare nodi specifici all&#39;interno della libreria estesa, abbiamo introdotto le categorie nel menu Nodo.

Il gran numero di nodi disponibili può rendere difficile trovare rapidamente quello desiderato. Per semplificare questo processo, è stato implementato un nuovo attributo [<b>Gruppo</b>](../../compositing-graphs/graph-parameters/graph-parameters.md) a livello di grafico. Quando questo attributo viene definito, viene utilizzato per organizzare e ordinare i risultati della ricerca.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Ricerca di ![nodi con categoria 1](version-15-1.resources/search1-2.png){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

Ricerca di ![nodi con categoria 2](version-15-1.resources/search2.png){zoomable="yes"}

</td>
</tr>
</table>

## Output predefinito

Quando un nodo ha più [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), non è possibile visualizzarli tutti contemporaneamente nel Vista 2D o come miniatura del nodo. In tali scenari, la linea guida prevalente è quella di utilizzare il primo segnaposto connesso o, se non ne è collegato nessuno, il primo output per impostazione predefinita.

Tuttavia, questo approccio potrebbe non sempre produrre risultati ottimali. Ad esempio, in alcuni nodi della spline il primo segnaposto connesso rappresenta spesso i dati delle coordinate della spline, che non sono adatti per l&#39;anteprima.

Per risolvere questo problema, è stato introdotto un attributo di output predefinito. Questa funzione consente all&#39;autore del grafico di <b>specificare l&#39;output da visualizzare per impostazione predefinita</b>, migliorando in tal modo l&#39;intuitività dell&#39;utilizzo del nodo e facilitando una comprensione più chiara del grafico creato.

Sperimentate con l’immagine seguente per vedere la differenza prima e dopo la definizione di output predefinita.

[Ulteriori informazioni](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

<table>
  <tr>
    <td>
      <img src="version-15-1.resources/defaultouput2.png" alt="defaultouput2">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="version-15-1.resources/defaultouput1.png" alt="Con l’output predefinito, le miniature sono sempre rilevanti.">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

## Nodo &#39;È definito&#39;

Quando lavorate con i grafici delle funzioni, potrebbe essere necessario determinare se una [variabile](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) esiste nel grafico.

Ad esempio, il rilevamento dell’assenza di una variabile consente di fornire un valore di fallback, garantendo che la funzione si comporti come previsto senza richiedere che ogni input venga impostato in modo esplicito. Per questo motivo è stato aggiunto il nodo [&#39;È definito&#39;](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md).

[Ulteriori informazioni](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)

![Nodo definito](version-15-1.resources/isdefined.png){zoomable="yes"}

## Note sulla versione

### 15.1.0

*(Rilasciato l&#39;11 dicembre 2025)*

### Aggiunto

* [NewGraph] Rielaborazione della nuova finestra del grafico
* [NewGraph] Aggiungere campioni di materiali e campioni avanzati
* [NewGraph] Aggiungere un nuovo attributo per il grafico per i dati del modello (categoria e sottotitolo)
* [NewGraph] Rimuovi opzione Formato di output
* [Content] Aggiungi funzioni hash
* [Content] Aggiungi tonemapper alle funzioni.sbs
* [Contenuto] Rumore anisotropo v2: aggiungere il formato di output predefinito, aggiungere il disturbo
* [Content] Applicare le maiuscole/minuscole al nodo e alle etichette dei parametri
* [Content] BnW spot 1 v2: aggiungete il formato di output predefinito, nessun supporto Affiancamento
* [Content] BnW spots 2 v2: aggiungete il formato di output predefinito, nessun supporto Affiancamento
* [Content] BnW spots 3 v2: aggiungete il formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Celle 1,2,3,4 v2: aggiungi formato di output predefinito, nessun supporto Affiancamento, opzioni per i disturbi
* [Content] Cloud 1 v2: aggiungi formato di output predefinito, nessun supporto Affiancamento
* [Content] Cloud 2 v2: aggiungi formato di output predefinito, nessun supporto Affiancamento
* [Content] Cloud 3 v2: aggiungi formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Da colore a maschera v2
* [Content] Disturbo direzionale 1 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Disturbo direzionale 2 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Disturbo direzionale 3 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Disturbo direzionale 4 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Graffi direzionali v2: aggiungi il formato di output predefinito, senza supporto Affiancamento
* [Content] Dirt 1 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Dirt 2 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Dirt 3 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Dirt 4 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Content] Dirt 5 v2: aggiungi il formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Sfumatura Dirt v2: aggiungi formato di output predefinito, nuove opzioni per i disturbi
* [Contenuto] Base Somma frattale v2: aggiungi formato di output predefinito, disturbo, nessun supporto Affiancamento
* [Contenuto] Somma frattale 1,2,3,4 v2: aggiungi formato di output predefinito
* [Content] Gaussian noise v2: aggiungi formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Punte gaussiane 1&amp;2 v2: aggiungete il formato di output predefinito, nessun supporto Affiancamento
* [Contenuto] Fibre disordinate 1,2,3 v2: aggiungi formato di output predefinito, nessun supporto Affiancamento, opzioni di disturbo
* [Content] Uisture noise v2: aggiungete il formato di output predefinito, nessun supporto Affiancamento
* [Content] Nuovo nodo &quot;Disturbo umidità 2&quot;
* [Content] Noises: aggiorna per aggiungere il formato di output predefinito
* [Content] Perlin noise v2: aggiungi formato di output predefinito, nessun supporto Affiancamento
* [Content] Mappatura forme: aggiungi modalità di filtro
* [Content] Mappatura UV: aggiungi modalità di filtro
* [Contenuto] Forma d’onda 1 v2: usa il formato di output predefinito + nuove opzioni
* [Content] Rumore bianco v2: utilizzate il formato di output predefinito e aggiungete le opzioni di distribuzione
* [Baker] Visualizza gli UV solo dalla trama selezionata
* [Baker] Aggiungete un&#39;opzione per selezionare il metodo di corrispondenza della geometria per nome
* [Baker] Seleziona il Baker più vicino quando viene eliminato un baker
* [Baker] UDIM: definizione di un elenco di porzioni UV da eseguire i baking
* [Baker] Aggiorna sdk eseguo i baking alla versione 3.15.4
* [vista 3D/SceneBrowser] Evitate di selezionare un valore UsdPrimitive quando fate clic con il pulsante destro del mouse
* [ColorManagement] Supporto ACE 2.0
* [Grafico di composizione] Consenti di impostare un nodo di output come &quot;Output predefinito&quot;
* [Cooker] Rimuovere l&#39;avviso sugli input non connessi delle istanze di funzione †
* [Functions] Aggiungi operatore isDefined
* [Grafico] Raggruppare gli elementi per l&#39;attributo &#39;group&#39; nel menu del nodo
* [Grafico] Migliorare il rendering delle miniature

### Correzioni

* [vista 3D] La texture in scala di grigi L16 viene visualizzata con una tinta rossa quando collegata all&#39;ambiente o a baseColor
* [vista 3D] La modifica della rilegatura del materiale di una scena senza materiale crea un nuovo materiale &quot;predefinito&quot;
* [vista 3D] Le normali calcolate non sono corrette per maglie OBJ specifiche
* [vista 3D] L&#39;ambiente personalizzato da SBSSCN non è visibile al caricamento in Pathtracer
* [vista 3D] Errori nella console durante la rotazione di un ambiente disabilitato
* [vista 3D] Specular level non applicato correttamente
* [vista 3D] Il Specular edge color non funziona quando si utilizza il rasterizzatore Eclair
* [vista 3D] Il materiale aggiunto dall&#39;utente non viene applicato alle scene predefinite
* [vista 3D][Baker] Il colore del materiale è troppo scuro una volta modificato localmente o quando si utilizza un baker &quot;Colore&quot;
* [vista 3D][Baker] Nessun colore materiale dal file FBX
* [Baker] I colori dei materiali nei file FBX non vengono rilevati correttamente
* [Baker] L’opzione &quot;ricalcola\_tangenti&quot; è sempre &quot;false&quot; nelle esportazioni di predefiniti JSON
* [Baker] CLI: Arresto anomalo quando si esegue lo stesso baker consecutivamente tramite File JSON
* [Baker] L’aggiornamento del parametro &quot;color-generator&quot; non funziona per &quot;Grayscale&quot;
* [Contenuto] Maschera per tracciati: errore nelle proporzioni non quadrate
* [Content] Renderer PBR render/icone: funzione del lobo specular errata
* [Content] Tracciati da spline: impostate la &#39;Dimensione output&#39; su &#39;Relativa alla principale&#39; per impostazione predefinita
* [Contenuto] Elenco punti: i punti non sono nell&#39;ordine corretto quando la texture dati non è quadrata
* [Content] Mappatura spline: errore di riga di 1px in casi casuali
* [Contenuto] Mappatura spline: UV allungamento in alcuni casi quando il thickness è 0
* [Grafico] Arresto anomalo quando si elimina l&#39;output di un grafico secondario di funzioni
* [Grafico] Il tipo di colore del nodo di input può essere modificato in pacchetti di sola lettura
* [Graph] L&#39;input principale può essere modificato in pacchetti di sola lettura
* [Proprietà] Il colore del widget di anteprima colore non corrisponde allo stato del pulsante sRGB
* [Scene] Impossibile caricare un file OBJ di dimensioni superiori a 2 GB
* [UI] Gli stati di ancoraggio di Console e Gestione dipendenze non vengono ripristinati dopo il riavvio

### PROBLEMI NOTI

* [Baker] Arresti anomali durante la esegue i baking con alcuni driver NVIDIA specifici
* [vista 3D] OpenGL: alcune scene importate potrebbero non essere renderizzate
* [vista 3D] Tracciatore: prestazioni lente durante l&#39;aggiornamento della texture con tasselation/spostamento abilitato
* [vista 3D] Alcune proprietà del materiale cromatico non vengono gestite correttamente quando vengono modificate localmente
* [vista 3D] Le scene con forme di base animate non sono supportate correttamente
* [vista 3D] La trama con più UDim non è ancora supportata
* [vista 3D] Le trame con più UV non sono supportate in modo affermativo e potrebbero causare una resa del materiale non valida
* [vista 3D] Tracciatore non supportato sulle schede grafiche AMD
