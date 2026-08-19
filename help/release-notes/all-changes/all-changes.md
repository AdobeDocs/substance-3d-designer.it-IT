---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/all-changes.html"
breadcrumb-title: ''
description: Esamina tutte le modifiche e gli aggiornamenti nelle versioni di Substance 3D Designer per tenere traccia dell’evoluzione e dei miglioramenti delle funzionalità.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > All changes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tutte le modifiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: e71846d2834d9c1979fe840f1cf9e321f2d4d93f
workflow-type: tm+mt
source-wordcount: '31805'
ht-degree: 0%

---


# Tutte le modifiche

## Versione 16

### 16.0.4

*(Rilasciato il 2 luglio 2026)*

**Aggiunto:**

* [Vista 3D] Blocca la risoluzione di rendering a 4096 in X e Y
* [Bakers] Aggiornare bake-sdk alla versione 3.22.3
* [Engine] Aggiorna il motore di Substance alla versione 9.4.4
* [OpenGL]&#x200B;[OpenPBR] Riduci il disturbo nel lobo specular per elevata rugosità + anisotropia
* [Scene] Mantenere la modalità di interpolazione UV-primaverile

**Corretto:**

* [Vista 3D] Esportazione USD: il percorso delle risorse viene memorizzato con un percorso assoluto
* [Pannelli] Il forno non riesce quando il caricamento di una trama poly elevata viene annullato (Windows)
* [Panettieri] L&#39;elenco delle scene 3D con poly alto non include risorse con lo stesso identificatore di poly basso
* [Bakers] Spazio normale: una normale WS viene sempre restituita quando è presente una normale di input
* [Contenuto] Normale non corretto durante il ridimensionamento non uniforme del pattern nello splatter forma V2
* [Content] Splatter forma V2: normali neri per le forme &#39;Piano&#39; e &#39;Disco&#39;
* [Content] Splatter forma v2: la prima forma non viene fusa correttamente con lo sfondo
* [Arresto anomalo] Arresto anomalo casuale possibilmente collegato a un video (descrizioni comandi avanzate)
* [Grafico] Arresto anomalo quando si incolla un nodo copiato da un nuovo grafico con identificatore vuoto
* [PSD] I file PSD vengono caricati troppe volte

### 16.0.3

*(Rilasciato Il 29 Maggio 2026)*

**Corretto:**

* [Arresto anomalo] Correggere una regressione introdotta nella versione 16.0.2 che causa un arresto anomalo all’avvio per alcuni utenti

### 16.0.2

*(Rilasciato Il 28 Maggio 2026)*

**Aggiunto:**

* [OpenPBR] Aggiungere il supporto per le costanti Colore di base/AO

**Corretto:**

* [Vista 3D] Perdita di VRAM nel tracciatore del percorso GPU quando lo spostamento è attivato
* [Vista 3D] Il thread principale rimane occupato quando la vista 3D esiste
* [Vista 3D]&#x200B;[OpenPBR] OpenGL: i widget &quot;Spessore&quot; sembrano bloccati ma accettano valori non compresi nell’intervallo consentito
* [Arresto anomalo] Arresto anomalo quando si sposta l&#39;input a cui si fa riferimento più di una posizione alla volta
* [Arresto anomalo] Arresto anomalo quando si annulla l’ingrandimento di una finestra
* [Arresto anomalo] Arresto anomalo durante la scrittura di TARGA o BMP dal fornaio
* [Arresto anomalo] Arresto anomalo casuale durante la visualizzazione della vista 3D
* [Grafico] Ordine errato dei pin di I/O durante lo spostamento di I/O dopo la modifica degli identificatori
* [Linux]&#x200B;[Export] Le finestre di dialogo &quot;Publish sbsar&quot; e &quot;Invia a&quot; non aggiungono l&#39;estensione del file

### 16.0.1

*(Rilasciato Il 5 Maggio 2026)*

**Aggiunto:**

* [Samples] Aggiungi un campione di materiale dedicato a SDF/Shape Splatter
* [Content] Visualizzatore 3D: Modificare lo stato predefinito
* [Content] Visualizzatore 3D: aggiungi ambiente predefinito
* [Content] Mappatura splatter forma v2: Aggiungi parametro centro proiezione per asse per mappatura triplanare
* [Content] Mappatura splatter forma v2: Aggiungi parametro di suddivisione
* [Content] Splatter forma v2: abilita estrusione forma per impostazione predefinita
* [3DView] Supporto delle GPU Intel Panther Lake in Pathtracer
* [Vista 3D] Migliorare la formattazione delle descrizioni a comparsa per lo Spostamento
* [Engine] Aggiornamento a Substance Engine v9.4.3
* [OpenPBR] geometry_tangent: aggiunta del supporto per le costanti
* [Preferenze] Aggiungete un’opzione affinché TGA/BMP scriva il canale alfa se è completamente opaco
* [ThirdParty] Aggiornamento a &quot;Adobe Color Engine&quot; (ACE) 7.0
* [UI] Rendi sempre visibile la finestra Gestione plug-in (modale)

**Corretto:**

* [Vista 3D] Il ridimensionamento del riquadro di visualizzazione viene applicato quando si utilizza la risoluzione fissa
* [Vista 3D]&#x200B;[OpenPBR] Si verifica un blocco quando si carica una scena GLTF esportata da Designer e si utilizza un materiale OpenPBR
* [Vista 3D]&#x200B;[OpenPBR] I materiali esportati da Painter non possono essere sostituiti in Designer
* [Content] Visualizzatore 3D: shape.id non è inizializzato e genera messaggi nella console
* [Contenuto] Schizzo forma v2 mappatura scala di grigi: l&#39;input motivo 4 non viene utilizzato nella proiezione triplanare
* [Content] Mappatura splatter forma v2: l&#39;ID SDF è scostato di -1 quando si utilizza la modalità &quot;1 immagine per ID materiale&quot;
* [Eclair]&#x200B;[USD] risultato errato quando si applica un materiale su un USD generato da Designer
* [Engine] Calcolo di un nuovo nodo Livelli splatter forma V2 grafico principale codificato seguendo calcoli
* [Engine] In alcuni casi il modulo di una variabile a fronte del suo valore uguale non restituisce 0 con il motore GPU
* [Engine]&#x200B;[Content] La tangente ad arco 2 restituisce 0 o Pi per i vettori X-right in un caso specifico
* [Engine]&#x200B;[Ubuntu]&#x200B;[SSE2] Arresto anomalo durante il caricamento di SBSAR specifici nel grafico
* [Grafico] Arresto anomalo durante la connessione dell&#39;output del processore valori in input bitmap
* [Grafico] Arresto anomalo quando si collega un valore all’input dell’immagine in alcuni casi
* [Grafico] Il grafico viene calcolato automaticamente su ogni salvataggio automatico quando si utilizza la mappa con baking
* [GraphRender] Arresto anomalo durante la connessione del valore di output dell&#39;Atlas scatter nell&#39;input dell&#39;immagine dell&#39;Atlas splitter
* [Linux]&#x200B;[Esporta] Il formato di file modificato viene ignorato nelle finestre di dialogo per il salvataggio dei file
* [Mac]&#x200B;[Steam] All’avvio di Designer viene visualizzata una finestra a comparsa con la protezione
* [Trama] I materiali OBJ non vengono importati correttamente
* [PSD] L’importazione di PSD richiede di estrarre i livelli dal file PSD a ogni salvataggio automatico

### 16.0.0

*(Rilasciato il 14 aprile 2026)*

**Aggiunto:**

* [Contenuto] Nodo splatter forma v2
* [Contenuto] Nodi colore/scala di grigi dello splatter di forme v2
* [Contenuto] Schizzo forma v2 nel nodo maschera
* [Content] Atlante griglia di nodi
* [Content] Nodo visualizzatore 3D
* [Content] Nodi operatore SDF 3D
* [Content] Nodi di base SDF 3D
* [Content] Nodi di trasformazione SDF 3D
* [Content] Nodi di materiale SDF 3D
* [Content] Angolo a nodo vettoriale
* [Content] Nodi a valore costante
* [Vista 3D] OpenPBR per il modulo di rendering OpenGL
* [Vista 3D] OpenPBR shader per i moduli di rendering Rasterizzatore e Pathtracer GPU
* [Vista 3D] Finestra di Spostamento per impostare la scala del height, il livello del height e la tassellatura
* [Vista 3D] Riorganizzare gli elementi della barra degli strumenti
* [Vista 3D] Imposta OpenPBR come modello di materiale predefinito nella vista 3D
* [Vista 3D] La vista 3D deve tenere conto dell’attributo grafico &quot;Modello di materiale&quot;
* [Vista 3D] Sincronizzazione dei modelli di materiale quando si passa dal modulo di rendering Rasterizzatore/Pathtracer GPU al modulo di rendering OpenGL
* [Vista 3D] Assicurati che il modello di materiale sia persistente quando si cambia modulo di rendering 3D e vengono sincronizzate le modifiche alla definizione del materiale
* [Vista 3D] Pathtracer GPU: attiva il ciclo dei pixel blu con disturbo
* [Vista 3D] Esposizione del controllo dell&#39;opacità dell&#39;occlusione ambiente
* [Vista 3D] Imposta l&#39;intervallo del parametro &#39;Tiling&#39; su [0, 10] per tutti gli shader
* [Vista 3D] Rinomina l’azione &quot;Focus&quot; in &quot;Frame&quot;
* [Vista 3D] Gestisce il nuovo parametro refineLevel che sostituisce tassellationFactor
* [Vista 3D] Aggiungere un contatore FPS
* [Vista 3D] Sposta la barra di avanzamento nella stessa barra degli strumenti orizzontale dello spazio colore in basso
* [Panettieri] Visualizza l’UV del panettiere selezionato nell’anteprima
* [Grafico] Aggiungere un nuovo attributo &quot;Modello di materiale&quot; ai grafici Substance
* [NewGraph] Aggiungere separatori nella visualizzazione miniature
* [Parameters] Definire il valore costante predefinito per i parametri di input con l&#39;editor &#39;Function&#39;
* [Parametri] Popolare la casella combinata dei parametri di nodo `Set` e `Is defined` con le variabili disponibili
* [Preferenze] Rimuovere l&#39;opzione obsoleta &quot;Decadimento fattore&quot; nella scheda &quot;Vista 3D&quot;
* [Publish] Finestra di dialogo Publish: Includi modello di materiale nelle informazioni del grafico
* [Python] Aggiungere una nuova classe SDMaterialModelDescription per ottenere le informazioni di un modello di materiale
* [Python] Consenti di ottenere/impostare la proprietà modello di materiale degli oggetti SDSBSCompGraph
* [Python Editor] Aumenta la dimensione del font a 12
* [Modelli] Aggiungi modelli di OpenPBR
* [Modelli] Convertire i campioni di materiale in OpenPBR
* [ThirdParty] Aggiornamento alla versione 1.88
* [ThirdParty] Aggiornamento dell’API C++ in C++20
* [ThirdParty] Aggiornamento NGL alla 1.42
* [ThirdParty] Aggiornamento di oneTBB alla versione 2022.x
* [ThirdParty] Aggiornamento di OpenColorIO alla versione 2.5.x
* [ThirdParty] Aggiornamento OpenEXR alla versione 3.4.x
* [ThirdParty] Aggiorna Qt &amp; QtForPython a 6.8.x e Python a 3.13.x
* [ThirdParty] Aggiorna TBB a oneTBB 2021.x
* [Deprecato] Rimuovi Iray ed editor MDL

**Corretto:**

* [Vista 2D] L&#39;intervallo di selezione dell&#39;istogramma non viene mantenuto quando la larghezza del widget diventa piccola
* [Esportazione 3D] Le trame esportate da Designer non vengono riprodotte nello stesso modo in usdview
* [Vista 3D] L’assegnazione di elementi non udim alla vista 3D lascia la modalità di rendering a porzione singola
* [Vista 3D] Risultato bloccato quando si utilizza OCIO
* [Vista 3D] Arresto anomalo quando si applica una texture del grafico a un materiale non sottoposto a override per una scena specifica
* [Vista 3D] Arresto anomalo durante la creazione di frame buffer
* [Vista 3D] Pathtracer GPU Eclair: geometria danneggiata e prestazioni ridotte durante il rendering di un modello specifico
* [Vista 3D] Trasformazione della texture errata per scene specifiche
* [Vista 3D] Inquadratura incoerente della scena/selezione quando si utilizza la risoluzione di rendering fissa
* [Vista 3D] Colore di diffusione errato durante il rendering di alcuni file GLTF
* [Vista 3D] Ambiente invisibile quando si cambia modulo di rendering in un caso specifico
* [Vista 3D] I materiali non vengono rilevati correttamente quando si importano alcuni file .fbx
* [Vista 3D] Se si escludono più di una volta i materiali, la suddivisione in porzioni viene ripristinata su 1
* [Vista 3D] Le proprietà della categoria &quot;UV&quot; non vengono salvate nei file SBSSCN
* [Vista 3D] &quot;Reimposta e visualizza gli output nella vista 3D&quot; dai grafici a output singolo non reimposta i materiali
* [Vista 3D] &quot;Salva rendering&quot;: il formato immagine modificato non viene mantenuto
* [Vista 3D] La selezione non funziona su GPU AMD
* [Vista 3D] La scena 3D indipendente non viene aggiornata quando viene modificata sul disco
* [Vista 3D] Alcune proprietà del materiale cromatico non sono gestite correttamente dal colore quando vengono modificate localmente
* [Vista 3D] Le texture UDIM non vengono applicate correttamente a una trama specifica
* [Vista 3D] La scena USD con materiale MaterialX non viene più riprodotta correttamente
* [Pannelli] Si arresta in modo anomalo con alcune trame
* [Baker] Trasferimento texture: arresto anomalo in bkBufferViewCopy
* [Cooker] Ciclo infinito nel nodo While Loop in un caso che potrebbe essere impedito
* [Engine] Arresta il motore di Substance alla chiusura dell&#39;applicazione
* [Generale] Evitare arresti anomali casuali quando si esce dall’applicazione (solo Windows)
* [Grafico] Grafico a funzioni: la propagazione del tipo non funziona correttamente in alcune situazioni
* [Grafico] I collegamenti del grafico vengono eliminati quando un nodo di input dell&#39;immagine viene rinominato
* [Grafico] A volte i collegamenti e i perni visualizzano artefatti
* [Preferenze] Il ridimensionamento del riquadro di visualizzazione è invertito
* [Properties] Arresto anomalo durante la modifica della regolazione dell&#39;input grafico durante la visualizzazione dei parametri dell&#39;istanza
* [Python] Impossibile importare moduli PySide6 (possibile conflitto con l&#39;installazione PySide6 esistente)
* [Python] I moduli PySide e Shiboken esistenti sono in conflitto con i moduli Designer
* [UI] Lo stile del passaggio del mouse scompare sui pulsanti in casi specifici (solo Windows)
* [UI] Lo stile del passaggio del mouse non è visibile sui pulsanti a discesa quando si fa clic (solo macOS)
* [UI] Il pulsante &quot;Ulteriori informazioni&quot; nella descrizione comandi &#39;?&#39; non funziona quando la descrizione comandi non rientra nei limiti della finestra di dialogo (solo Windows)

**Problemi noti:**

* [Grafico] Le icone generate per gli OpenPBR non sono accurate
* [Vista 3D] Le scene con forme di base animate non sono supportate correttamente
* [Vista 3D] Il tracciatore non è supportato su tutte le schede grafiche AMD

## Versione 15

### 15.1.3

*(Rilasciato Il 10 Marzo 2026)*

**Aggiunto:**

* [Bakers] Aggiungere una macro di dimensioni output per il nome file
* [Panettieri] Evitate di caricare la trama di alta qualità prima della cottura
* [Bakers] CLI: aggiornare la descrizione dell&#39;opzione &#39;output-size&#39; con le macro di dimensione
* [Bakers] Convertire il formato della texture di input nel formato richiesto
* [Pannelli] Disattiva l’opzione &quot;Offset map&quot; quando è selezionata l’opzione &quot;Usa gabbia&quot;
* [Panettieri] Lo schermo mappa con baking già quando si riapre la finestra di cottura
* [Panettieri] Tenere la finestra di cottura aperta fino a quando tutti i processi di cottura sono effettivamente annullati
* [Bakers] Migrazione della funzione BindTexture
* [Bakers] [Impostazioni] Imposta il valore predefinito &#39;Modalità filtro nome&#39; su &#39;Nome padre (legacy)&#39;
* [Bakers] [Tooltip] Aggiungi il valore &#39;Modalità filtro nome&#39; alla descrizione del parametro &#39;Corrispondenza&#39;
* [Engine] Aggiorna motore di Substance alla versione 9.3.4

**Corretto:**

* [Vista 3D] &quot;Visualizza output in vista 3D&quot; non sostituisce l&#39;assegnazione esistente sui grafici con output singolo
* [Vista 3D] In alcuni casi non è possibile visualizzare gli UV
* [Vista 3D] Le tangenti calcolate appaiono spezzate per USD
* [Vista 3D] Arresto anomalo all’apertura del menu Modulo di rendering
* [Bakers] Impossibile impostare una distanza maggiore di 1 quando l&#39;opzione &quot;Rispetto a Bbox&quot; è deselezionata
* [Panettieri] Il panettiere a colori impiega troppo tempo per finire in casi specifici
* [Panettieri] Colore: arresto anomalo durante le Isole UV di cottura al forno
* [Bakers] Gli intervalli dei parametri di distanza e raggio sono troppo stretti quando il valore è assoluto
* [Panettieri] Errore durante la cottura da tangenti e bitangenti mancanti di poli alti che non sono necessari
* [Panettieri] I colori dei materiali non sono corretti nella riga di comando del panettiere
* [Panettieri] In alcune situazioni vengono ignorate più trame poly alte
* [Pannelli] Normale: output nero quando si utilizza l&#39;antialiasing e la diffusione (solo macOS)
* [Bakers] Il controllo del percorso della mappa di offset segnala errori imprevisti durante l&#39;utilizzo delle risorse del pacchetto bitmap
* [Bakers] Descrizione comando Offset map non corretta
* [Pannelli] L’inserimento della risorsa in una cartella specifica della trama non funziona
* [Panettieri] Trasferimento texture: il valore &#39;UV set&#39; non viene ripristinato come quando si riapre la finestra di cottura
* [Bakers] Trasferimento texture: un input in scala di grigio non genera un output in scala di grigio
* [Baker] Avvertenza per il fornaio ereditato disattivato non viene cancellato quando si cambia l’origine della texture nel fornaio di destinazione
* [Bakers] [UDIM] La mappa di offset viene applicata solo a UDIM 1001
* [Grafico] UDIM 1001 viene sempre calcolato indipendentemente dal file UVT utilizzato

### 15.1.2

*(Rilasciato Il 3 Febbraio 2026)*

**Corretto:**

* Livelli [Engine]: i valori in virgola mobile vengono sempre bloccati su [0, 1]
* [Baker] La corrispondenza della geometria per nome principale (Legacy) non funziona per le sottomissioni
* [Pannelli] Colore: le modifiche ai colori dei materiali nell&#39;interfaccia utente vengono ignorate
* [3D View]&#x200B;[Bakers] Il caricamento del file OBJ richiede molto tempo

### 15.1.1

*(Rilasciato il 20 gennaio 2026)*

**Aggiunto:**

* [Esempi] Aggiungete due campioni per creare sezioni da alimentare con lo strumento barra multifunzione di Painter
* [Engine] Aggiornamento a Substance Engine v9.3.2
* [Engine]&#x200B;[Metal] Migliora le prestazioni
* [Engine] L&#39;interpolazione bilineare delle texture intere viene ora eseguita con maggiore precisione (backend CPU)
* [Baker] Registra un avviso se il colore Vertice non è presente nella trama poli alta
* [Branding] Aggiornamento delle icone dei tipi di file
* [NewGraph] Applicare stili al passaggio del mouse sull&#39;icona (i) nelle modalità di visualizzazione &quot;Elenco&quot;, &quot;Pacchetti&quot; e &quot;Directory&quot;

**Corretto:**

* [3DView] Le trame UDIM non eseguono più il rendering di una singola porzione
* [3DView] Arresto anomalo quando non viene rilevato renderDevice
* [Branding] Correggere le icone per i file .SBS su Linux
* [Content] Funzione da RGB a HSL: risultato errato per quasi 0 ingressi
* [Grafico] Il generatore di icone/miniature del grafico non funziona
* [Grafico] Menu Nodo: gli elementi raggruppati senza miniatura non hanno alcun rientro
* [Engine]&#x200B;[Contenuto] Colore da mascherare v2: artefatti sul motore SSE2 quando si utilizza lo spazio colore della distanza Lab
* [Engine]&#x200B;[Content] Colore da maschera v2: artefatti sui motori GPU arm64 quando si utilizza lo spazio colore della distanza Lab
* [Engine]&#x200B;[Metal] Output di irradianza nero per PBR render Node
* [Engine]&#x200B;[Mac] Risultato errato in una funzione di processore pixel su Metal
* [Engine]&#x200B;[Mac] Migliora la precisione per alcune istruzioni utilizzate nei processori Pixel sulle GPU Apple Silicon M1/M2
* [Engine] Il ridimensionamento delle immagini di input (o delle risorse incorporate) non introdurrà più artefatti dei bordi (backend CPU)
* [Engine] Il filtro Livelli non bloccherà più i valori di input a virgola mobile quando si eseguono output di texture 8I/16I (backend CPU)
* [Engine] È stato corretto un bug di FxMaps a causa del quale le immagini di input in scala di grigio utilizzate dai nodi FxMaps potevano essere campionate in modo errato (backend CPU).
* [Engine] Sono stati corretti alcuni artefatti nella versione 1-seed del filtro Distanza (backend GPU).

### 15.1.0

*(Rilasciato l&#39;11 dicembre 2025)*

**Aggiunto:**

* [NewGraph] Rielaborazione della nuova finestra del grafico
* [NewGraph] Aggiungere campioni di materiali e campioni avanzati
* [NewGraph] Aggiungere un nuovo attributo per il grafico per i dati del modello (categoria e sottotitolo)
* [NewGraph] Rimuovi opzione Formato di output
* [Content] Aggiungi funzioni hash
* [Content] Aggiungi tonemapper alle funzioni.sbs
* [Contenuto] Rumore anisotropo v2: aggiungere il formato di output predefinito, aggiungere il disturbo
* [Content] Applicare le maiuscole/minuscole al nodo e alle etichette dei parametri
* [Content] BnW spot 1 v2: aggiungete il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] BnW spots 2 v2: aggiungete il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] BnW spot 3 v2: aggiungete il formato di output predefinito, senza supporto di suddivisione in porzioni
* [Contenuto] Celle 1,2,3,4 v2: aggiungi formato di output predefinito, nessun supporto per la suddivisione in porzioni, opzioni per i disturbi
* [Content] Cloud 1 v2: aggiungete il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Cloud 2 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Cloud 3 v2: aggiungete il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Contenuto] Da colore a maschera v2
* [Content] Disturbo direzionale 1 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Disturbo direzionale 2 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Disturbo direzionale 3 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Disturbo direzionale 4 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Contenuto] Graffi direzionali v2: aggiungi il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Dirt 1 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Dirt 2 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Dirt 3 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Dirt 4 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Dirt 5 v2: aggiungi formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Contenuto] Sfumatura Dirt v2: aggiungi formato di output predefinito, nuove opzioni per i disturbi
* [Contenuto] Base Somma frattale v2: aggiungi formato di output predefinito, disturbo, nessun supporto di suddivisione
* [Contenuto] Somma frattale 1,2,3,4 v2: aggiungi formato di output predefinito
* [Content] Gaussian noise v2: aggiungi formato di output predefinito, nessun supporto di suddivisione in porzioni
* [Contenuto] Punte gaussiane 1&amp;2 v2: aggiungete il formato di output predefinito, senza supporto di porzioni
* [Contenuto] Fibre disordinate 1,2,3 v2: aggiungi formato di output predefinito, nessun supporto di affiancamento, opzioni di disturbo
* [Contenuto] Disturbo da umidità v2: aggiungi il formato di output predefinito, senza supporto per la suddivisione in porzioni
* [Content] Nuovo nodo &quot;Disturbo umidità 2&quot;
* [Content] Noises: aggiorna per aggiungere il formato di output predefinito
* [Content] Perlin noise v2: aggiungi formato di output predefinito, nessun supporto di suddivisione in porzioni
* [Content] Mappatura forme: aggiungi modalità filtro
* [Content] Mappatura UV: aggiungi modalità filtro
* [Contenuto] Forma d’onda 1 v2: usa il formato di output predefinito + nuove opzioni
* [Content] Rumore bianco v2: utilizzate il formato di output predefinito e aggiungete le opzioni di distribuzione
* [Bakers] Visualizza gli UV solo dalla trama selezionata
* [Bakers] Aggiungere un&#39;opzione per selezionare il metodo di corrispondenza della geometria in base al nome
* [Panettieri] Seleziona il panettiere più vicino quando viene eliminato un panettiere
* [Panettieri] UDIM: definire un elenco di porzioni UV da cuocere
* [Bakers] Aggiornare bake sdk alla versione 3.15.4
* [3D View/SceneBrowser] Evitare di selezionare un oggetto UsdPrimitive quando si fa clic con il pulsante destro del mouse
* [ColorManagement] Supporto di ACES 2.0
* [Grafico di composizione] Consenti di impostare un nodo di output come &quot;Output predefinito&quot;
* [Cooker] Rimuovere l&#39;avviso sugli input non connessi delle istanze di funzione †
* [Functions] Aggiungi operatore isDefined
* [Grafico] Raggruppare gli elementi per l&#39;attributo &#39;group&#39; nel menu del nodo
* [Grafico] Migliorare il rendering delle miniature

**Corretto:**

* [Vista 3D] La texture in scala di grigi L16 viene visualizzata con una tinta rossa quando collegata all&#39;ambiente o a baseColor
* [Vista 3D] La modifica del binding del materiale di una scena senza materiale crea un nuovo materiale &quot;predefinito&quot;
* [Vista 3D] Le normali calcolate non sono corrette per mesh OBJ specifiche
* [Vista 3D] L&#39;ambiente personalizzato da SBSSCN non è visibile al caricamento in Pathtracer
* [Vista 3D] Errori nella console durante la rotazione di un ambiente disabilitato
* [Vista 3D] Lo Specular level non viene applicato correttamente
* [Vista 3D] Il Specular edge color non funziona quando si utilizza il rasterizzatore Eclair
* [Vista 3D] Il materiale aggiunto dall&#39;utente non viene applicato alle scene predefinite
* [Vista 3D]&#x200B;[Pannelli] Il colore del materiale è troppo scuro una volta sovrascritto o quando si utilizza un panettiere a &quot;colori&quot;
* [Vista 3D]&#x200B;[Pannelli] Nessun colore materiale dal file FBX
* [Pannelli] I colori dei materiali nei file FBX non vengono rilevati correttamente
* [Bakers] L’opzione &quot;recompute\_tangents&quot; è sempre &quot;false&quot; nelle esportazioni di predefiniti JSON
* [Bakers] CLI: arresto anomalo durante l&#39;esecuzione consecutiva dello stesso baker tramite file JSON
* [Bakers] L&#39;aggiornamento del parametro &#39;color-generator&#39; non funziona per &#39;Grayscale&#39;
* [Contenuto] Maschera per tracciati: errore nelle proporzioni non quadrate
* [Content] Renderer PBR render/icone: funzione del lobo specular errata
* [Content] Tracciati da spline: impostare &#39;Dimensioni output&#39; su &#39;Relative a padre&#39; per impostazione predefinita
* [Contenuto] Elenco punti: i punti non sono nell&#39;ordine corretto quando la texture dei dati è non quadrata
* [Content] Mappatura spline: errore di riga di 1px in casi casuali
* [Contenuto] Mappatura spline: UV estesi in alcuni casi quando il thickness è 0
* [Grafico] Arresto anomalo quando si elimina l’output di un grafico secondario di funzioni
* [Grafico] Il tipo di colore del nodo di input può essere modificato in pacchetti di sola lettura
* [Graph] L&#39;input principale può essere modificato in pacchetti di sola lettura
* [Proprietà] Il colore del widget di anteprima colore non corrisponde allo stato del pulsante sRGB
* [Scene] Impossibile caricare un file OBJ di dimensioni superiori a 2 GB
* [UI] Gli stati di ancoraggio di Console e Gestione dipendenze non vengono ripristinati dopo il riavvio

### 15.0.3

*(Rilasciato Il 23 Ottobre 2025)*

**Corretto:**

* [Content] L&#39;anteprima dell&#39;output dei nodi di Strumento spline non viene visualizzata per impostazione predefinita
* [Grafico] Arresto anomalo quando si elimina l’output di un grafico secondario di funzioni

### 15.0.2

*(Rilasciato Il 18 Settembre 2025)*

**Aggiunto:**

* [3D View/OpenGL] Rimuovi l&#39;effetto wireframe applicato alla trama selezionata
* [Vista 3D] Consente di usare il tasto &quot;F&quot; per mettere a fuoco una trama selezionata quando l&#39;Elenco scene è attivo
* [Vista 3D] Il rendering non viene aggiornato quando si modifica il formato mappa normale
* [BakersCLI] Aggiungi opzione per controllare la dimensione della cache di superficie
* [BakersCLI] Rinomina l&#39;opzione &quot;use\_cache&quot; in &quot;keep\_meshes\_in\_cache&quot;
* [UI] Icona di aggiornamento per le scene 3D nella libreria

**Corretto:**

* [Vista 3D] Arresto anomalo durante l’assegnazione di un nodo di materiale a una scena con più materiali
* [Vista 3D] Il grafico creato dagli input della texture viene sempre visualizzato nella vista 3D indipendentemente dalle preferenze
* [Vista 3D] Utilizzo errato in una descrizione del badge &quot;Visualizzato in vista 3D&quot; in un caso specifico
* [Vista 3D] Molti errori USD durante l&#39;override di scene specifiche
* [Vista 3D] Artefatti dell&#39;ombra quando si utilizza lo spostamento su una scena piatta nella rasterizzazione
* [Vista 3D] Alcune scene specifiche non sono visibili quando si utilizza il modulo di rendering OpenGL
* [Vista 3D] La finestra di dialogo utilizzata per &quot;Selezionare il Grafico Substance di destinazione&quot; presenta sempre l&#39;icona del grafico &quot;In sospeso&quot;.
* [Vista 3D] Il menu di scelta rapida della finestra della vista non viene visualizzato per scene specifiche
* [Vista 3D] I badge &quot;Visualizzato in vista 3D&quot; non vengono cancellati quando si cambia scena in un caso specifico
* [Vista 3D] Colore sbiadito nella vista 3D quando si utilizza la gestione colore di Adobe
* [Vista 3D]&#x200B;[Linux] Diverse scene vengono renderizzate in nero nel modulo di rendering OpenGL
* [Vista 3D]&#x200B;[Visualizzatore scene] I tasti freccia spostano la selezione alla radice
* [BakerCLI] Impossibile eseguire l&#39;override di alcuni parametri
* [Panettieri] Artefatti nella dilatazione quando si utilizzano panettieri normali con antialiasing
* [Bakers] Il processo di cottura si è interrotto bruscamente in CLI durante la cottura di un&#39;elevata quantità di UDIM in 4K
* [Panettieri] Arresto anomalo quando si spinge il panettiere verso il basso nell&#39;elenco dei panettieri in casi specifici
* [Bakers] La selezione del formato passa da .surface a .dds
* [Panettieri] Si blocca durante la cottura di grandi quantità di UDIM a 4K
* [Bakers]&#x200B;[macOS] Arresto anomalo durante il trasferimento di texture con antialising
* [Contenuto] Elenco punti: i punti non sono nell&#39;ordine corretto quando la texture dei dati è non quadrata
* [Content] Visualizza tavolozza colori: i nodi interni vengono calcolati con risoluzioni troppo alte
* [Data] Arresto anomalo durante la ridenominazione dell’output per correggere l’output fantasma nell’istanza
* [Engine] Distanza: la luminanza della maschera di input viene modificata
* [FxMap] $tiling non ha alcun effetto se FX-Map si trova all’interno di un grafico secondario
* [Grafico] La ricerca fuzzy restituisce risultati irrilevanti
* [Python Editor] Gli script caricati non vengono riaperti tra le sessioni

### 15.0.1

*(Rilasciato il 22 luglio 2025)*

**Aggiunto:**

* [Vista 3D] Consente di creare texture di trame USD con associazioni displayColor e nessuna associazione Material
* [Vista 3D] Non creare automaticamente un solo materiale per trama che non ha un legame con il materiale
* [Vista 3D] Rinomina &quot;Campioni di pixel convergenti&quot; in &quot;Campioni&quot;
* [Vista 3D] Rinomina il parametro &quot;Scala UV abilitata&quot; in &quot;Attiva Dimensioni fisiche da grafico&quot;.
* [Vista 3D] Riduce l&#39;intensità dello spostamento in base al parametro &#39;Tiling&#39;
* [3D View/OpenGL/Iray] Aggiunge un messaggio nella finestra della vista quando l&#39;ambiente predefinito è disattivato
* [Panettieri] Usare le icone dei pulsanti per riordinare le linee nell&#39;elenco di rendering Panettieri
* [Preferenze] Aggiungete un’opzione per definire il modulo di rendering per la vista 3D predefinito
* [Properties] Fai in modo che &quot;Ripristina predefiniti&quot; utilizzi gli eventuali valori predefiniti creati

**Corretto:**

* [Vista 3D] Artefatti su scene specifiche quando renderizzati con OpenGL
* [Vista 3D] L’ambiente predefinito non è disattivato quando si carica una risorsa scena 3D USD che ne contiene una
* [Vista 3D] La visualizzazione del menu contestuale del riquadro di visualizzazione richiede diversi secondi in scene di grandi dimensioni
* [Vista 3D] L’intensità di emissione è 0 quando si sostituiscono materiali non USD utilizzando solo il colore di emissione
* [Vista 3D] I canali Rosso e Blu vengono scambiati in una texture a 8 bit utilizzata come ambiente
* [Vista 3D] Il trascinamento RMB non funziona in modo uniforme a causa del clic con il pulsante destro del mouse sul registro
* [Vista 3D] L’opzione &quot;Mostra solo&quot; del sottoinsieme nasconde la trama principale
* [Vista 3D] Le scene predefinite caricate da un file vengono visualizzate con un colore di base errato
* [Vista 3D] La proprietà &quot;Scala UV&quot; viene reimpostata quando si passa da OpenGL a un altro modulo di rendering e viceversa
* [3D View]&#x200B;[Iray] I rendering sono spesso sfocati e pixelati
* [Baker] Artefatti quando si utilizza la diffusione su una GPU AMD
* [Panettieri] La cottura non riesce con alcune scene per i set UV diversi da 0
* [Panettieri] &quot;Texture trasferita&quot;: l&#39;elenco &quot;UV Set&quot; non tiene conto dell&#39;opzione &quot;Usa come poly alto&quot;
* [Panettieri] La selezione dei riquadri UV è sempre impostata su &quot;Tutto&quot;
* [Grafico] Arresto anomalo durante l&#39;eliminazione di un nodo nel contesto
* [Mac OS]&#x200B;[Vista 3D] Risoluzione di rendering errata sui display mac
* [Parametri] I parametri modificati non vengono formattati sul primo display
* [UX] Le voci disabilitate nel menu a discesa sono invisibili

### 15.0.0

*(Rilasciato il 15 luglio 2025)*

**Aggiunto:**

* [Vista 3D] Nuovo modulo di rendering, con modalità rasterizzatore e tracciatore tracciatore
* [Vista 3D] Aggiungi uno strumento di selezione per selezionare un oggetto nella scena 3D
* [Vista 3D] Aggiungi nuova &quot;Esporta scena con livelli...&quot; azione nel menu &quot;Scena&quot;
* [Vista 3D] Aggiungere nuovi pulsanti della barra degli strumenti
* [Vista 3D] Aggiungi la possibilità di passare da una videocamera all’altra contenuta in una scena USD
* [Vista 3D] Consente di attivare l&#39;oggetto selezionato quando si preme &#39;F&#39; nella finestra della vista
* [Vista 3D] Consente di generare un grafico di composizione Substance da un materiale esistente
* [Vista 3D] Consenti l’invio di un grafico composizione SBS nella vista 3D e assegna il suo output univoco all’utilizzo Ambiente/Panorama
* [Vista 3D] Cancella la selezione corrente premendo il tasto Esc
* [Vista 3D] Visualizza una scena 3D importata con texture
* [Vista 3D] Distinguere i controlli di ripetizione delle texture X e Y
* [Vista 3D] Attivare/Disattivare le ombre
* [Vista 3D] Attivare/Disattivare il piano terreno
* [Vista 3D] Nel menu &quot;Materiali&quot;, aggiungi &quot;Rimuovi&quot; solo per il Materiale che è stato aggiunto manualmente e che non è utilizzato
* [Vista 3D] Nel menu &quot;Materiali&quot;, rimuovi l&#39;azione &quot;Rimuovi tutto&quot;
* [Vista 3D] Rendere i file USDZ esportati autonomi
* [Vista 3D] Rendi persistenti le proprietà del modulo di rendering quando si cambia modalità
* [Vista 3D] Mantiene gli input di materiale esistenti quando si sostituisce un materiale
* [Vista 3D] Ridisporre le proprietà della videocamera
* [Vista 3D] Rimuovi azioni &quot;Videocamera/Salva schermata...&quot; e &quot;Videocamera/Copia schermata negli Appunti&quot;
* [Vista 3D] Rimuovi l&#39;azione del menu &quot;Materiale/Ricostruisci tutto&quot;
* [Vista 3D] Rimuovi il prefisso &quot;Default&quot; dell&#39;etichetta della fotocamera predefinita
* [Vista 3D] Imposta l&#39;azione di menu &quot;Ripristina valore predefinito&quot; come ultima nel menu hamburger delle proprietà di input del materiale
* [Vista 3D] Regolazioni scelte rapide
* [Vista 3D] Supporto di ombre e trasparenza in modalità tempo reale
* [Vista 3D] Supporto degli shader MaterialX da una scena USD importata
* [Vista 3D/OpenGL] Rinomina il parametro &quot;Scala UV abilitata&quot; in &quot;Abilita Dimensioni fisiche da grafico&quot;.
* [Vista 3D / Effetti Post] Bloom
* profondità del campo [Vista 3D/Effetti Post]
* [Vista 3D / Effetti Post] Mappatura toni
* [Vista 3D / Browser scena] Consente di visualizzare le proprietà del materiale quando lo si seleziona in SceneBrowser
* [Vista 3D/Visualizzatore scene] Nascondi la colonna &quot;Materiale&quot;
* [Vista 3D/Visualizzatore scene] Inserisci in grassetto gli elementi di base USD controllati da un&#39;entità predefinita
* [Panettieri] Aggiungi un menu di scelta rapida nella vista albero con le azioni &quot;Seleziona tutto&quot;/&quot;Deseleziona tutto&quot;
* [Baker] Aggiungete un&#39;opzione per controllare l&#39;interpolazione bitangent
* [Bakers] Aggiungi splitter orizzontale nella GUI
* [Bakers] Aggiungi macro UDIM per impostazione predefinita nel nome di output quando la scena è udim
* [Pannelli] Consente di ricalcolare la tangente
* [Panettieri] Consenti di rinominare un panettiere senza interrompere i collegamenti
* [Panettieri] Modificare le dimensioni predefinite del pannello centrale
* [Bakers] Texture di input per flusso di lavoro UDIM
* [Bakers] Imposta l&#39;ordine dell&#39;elenco di mappe 2D View come ordine dell&#39;elenco di rendering Bakers
* [Panettieri] Rendete modale la finestra di cottura
* [Panettieri] Gestire i parametri di mappatura tonale
* [Bakers] Rimuovi selezione plug-in spazio tangente
* [Panettieri] Salva stato &quot;abilitato&quot; o &quot;disabilitato&quot; per i panettieri durante il salvataggio di un predefinito
* [Panettieri] Selezionare il materiale per impostazione predefinita nel widget di selezione
* [Bakers] Impostare l&#39;orientamento predefinito della texture di output Normale rispetto alla preferenza
* [Panettieri] Per impostazione predefinita, imposta le porzioni UV su Tutto
* [Bakers] Opzione di aggiunta WordSpaceDirection FromTexture/FromValue
* [Pannelli] Da universale a tangente: imposta l’input predefinito su &quot;Da texture&quot;
* [SBSBaker] Create un&#39;opzione per controllare l&#39;ordine backend
* [SBSBaker] Migliore utilizzo dell&#39;argomento StringList
* [SBSBaker] Rinominare &quot;match\_source\_instance&quot; in &quot;match\_mesh\_name&quot;
* [SBSBaker] Rinominare &quot;Submesh&quot; in &quot;GeomSubset&quot;
* [SBSBaker] Rinomina in substance3d\_baker
* [Content] Aggiungi la forma &#39;Hemisphere&#39; ai nodi del generatore che espongono le forme Quadrant
* [Interop] Supporto del formato di file GLTF
* [Interop] Supporto del formato file PLY
* [Interop] Supporto del formato di file STL
* [Library] Uniformizzare le descrizioni comandi per i nodi atomici
* [Mac] Interrompi il supporto della piattaforma MacIntel
* [Nodes] Aggiungere descrizioni comandi avanzate per i nodi atomici
* [Parameters] Chiude la sezione &#39;Attributes&#39; per impostazione predefinita
* [Parametri] Consente all&#39;utente di specificare i valori di default dei parametri di base per le nuove istanze
* [Preferenze] Pannelli: aggiungi un&#39;opzione booleana per calcolare lo spazio tangente per frammento
* [Preferenze] Rimuovi i plug-in dello spazio tangente
* [Preferenze] Memorizzare le preferenze per le versioni secondarie di SD (XX.X)
* [VFX] Aggiornamento incrementale alla versione 1.85.0
* [VFX] Aggiornate MacOS versione minima alla versione 12.0
* [VFX] Aggiornare OpenColorIO alla versione 2.4.2
* [VFX] Aggiornamento di OpenColorIO alla versione 2.4.x
* [VFX] Aggiornamento di OpenExr alla versione 3.3.x
* [VFX] Aggiornare Qt alla versione 6.5.8

**Corretto:**

* [Vista 3D] Le texture nella scena USD esportata non vengono applicate correttamente
* [Vista 3D] [UDIM] Impossibile visualizzare gli output del grafico UDIM in Vista 3D quando la visualizzazione automatica all&#39;apertura del grafico è disattivata nelle preferenze del grafico
* [Panettieri] &#39;Antialiasing.&#39; e &#39;Media. le celle normali per i forni non applicabili sono vuote e modificabili
* [Bakers] L’azione &quot;Aggiorna&quot; utilizza il backend ray tracing quando è disattivato nelle preferenze
* [Panettieri] Panettieri bloccati come occupati dopo un errore durante il processo &quot;Aggiorna tutte le mappe con baking&quot;
* [Bakers] Arresto anomalo a oltre 180 UDIM durante la cottura della mappa di posizione OpenGL su una trama specifica
* [Bakers] Arresto anomalo quando si apre la finestra di dialogo &quot;Informazioni modello di forno&quot; più volte di seguito (solo macOS)
* [Bakers] Nell’esportazione dei predefiniti JSON, il valore &quot;udim&quot; è sostituito da &quot;1001&quot; quando era impostato su &quot;All&quot;
* [Baker] Memoria non rilevata correttamente su Linux
* [Bakers] La dipendenza di input mappa mancante non attiva il rendering di avvisi e/o blocchi
* [Bakers] Nessuna etichetta di errore quando il nome dell&#39;output è vuoto
* [Pannelli] Il passaggio della trama ad alto poli dal file non ha alcun effetto
* [Bakers] Il baker di destinazione non è selezionato per impostazione predefinita quando si utilizza l&#39;azione &quot;Rebake&quot;
* [Engine] Distanza: visibile &quot;taglio&quot; in alcune situazioni
* [Engine] Mappa Fx: i colori negativi non sono supportati quando la profondità di bit è 8 bit (solo motori GPU)
* [Localizzazione] L’input di caratteri torna dal giapponese al latino nel menu dei nodi
* [Sicurezza] Analisi dei file USDC senza vulnerabilità di scrittura associata
* [Security] Vulnerabilità di scrittura II non associata, durante l&#39;analisi del file NEF
* [Sicurezza] Vulnerabilità di lettura non associata III, durante l&#39;analisi del file DNG
* [Preferenze] Problemi UX nelle impostazioni del progetto per progetti di sola lettura
* [Risorse] Più set UV non vengono visualizzati quando si aprono file FBX
* [UI] Etichette sovrapposte nella barra di stato
* [UI] Le descrizioni del menu a discesa &quot;Modalità creazione collegamento&quot; non vengono visualizzate

## Versione 14

### 14.1.2

*(Rilasciato il 15 aprile 2025)*

**Aggiunto:**

* [Grafico] Utilizza il motore GPU predefinito per generare miniature per il grafico corrente
* [Libreria] Utilizzate il motore GPU predefinito per generare le miniature della libreria

**Corretto:**

* [Grafico] In alcuni casi non è possibile spostare le connessioni in modalità di creazione di collegamenti standard
* [Content] Artefatti nell&#39;output del filtro MLV in un caso specifico
* [Contenuto] Atlas splitter/dispersione: viene disegnata correttamente solo la prima cella (solo macOS + motore GPU)
* [Contenuto] Smusso uniforme: il formato è assoluto 32f
* [Content] Fibre 1: artefatti visivi durante la conversione in mappa normale
* [Content] RT AO, Ombre, Rendering normale piegato in alcuni casi in modo errato
* [Panettieri] Le voci di menu con sottomenu perdono un margine a destra del testo
* [MacArm]&#x200B;[sbsrender] Motore CPU errato quando il motore GPU non viene trovato
* [Mac/Linux]&#x200B;[sbsrender] Motore GPU predefinito errato

### 14.1.1

*(Rilasciato il 20 febbraio 2025)*

**Aggiunto:**

* [Grafico] Strumenti di allineamento dei nodi: ripristina le scelte rapide da tastiera e abilita lo stacking per impostazione predefinita
* [MDL] Avvisa gli utenti che i &quot;grafici MDL&quot; diventeranno obsoleti in una versione futura
* [Preferenze] Avvisa gli utenti che i &quot;Plug-in personalizzati per spazi tangenti&quot; diventeranno obsoleti in una versione futura

**Corretto:**

* [Vista 2D] Visualizza le coordinate del pixel centrale anziché l&#39;angolo superiore sinistro
* [Contenuto] Anisotropo Kuwahara Grayscale: avvertenza dei cuochi per la mancanza della variabile &quot;ignore\_alpha&quot;
* [Contenuto] Avvisi relativi ai fornelli in alcuni nodi di Grunge
* [Contenuto] Errori di cottura per parametro mancante nel nodo &#39;Livelli automatici&#39;
* [Contenuto] Errori di cottura in Console durante il rendering delle miniature di alcuni pacchetti
* [Content] Edge Notch: Avviso di cottura nella console
* [Contenuto] Colore MLV: pagina al vivo a colori nonostante l’utilizzo di Nessuna porzione in un caso specifico
* [Contenuto] Maschera su tracciati: in casi specifici, i tracciati possono essere troppi, troppo pochi o di lunghezza zero
* [Content] PBR render v1: alcuni grafici di utilità sono esposti nella libreria
* [Contenuto] Dispersione sulla spline: viene disegnato un pattern anche se non è presente alcun input della spline
* [Parametri] Etichetta &#39;Valore fantasma&#39; quando si incolla un parametro elenco con indice non corrispondente
* [UI] Arresto anomalo alla chiusura di Designer tramite l’azione &quot;Esci&quot; nel dock di macOS (solo macOS)
* [UI] I tracciati delle texture nelle proprietà dello shader non vengono ritagliati in base alla larghezza dell’ancoraggio

### 14.1.0

*(Rilasciato il 14 gennaio 2025)*

**Aggiunto:**

* [Vista 2D] Aggiungere la visualizzazione dei pixel bloccati nel pannello Informazioni
* [API] Esposizione dei nodi Dimensione riquadro nella scena di visualizzazione grafico
* [Content] &quot;Material Height Blend&quot;: output &quot;Height Mask&quot;
* [Content] &#39;Path Vertex Processor&#39;: usa il pulsante &#39;Edit function&#39; per il parametro &#39;Per vertex function&#39;
* [Contenuto] Livelli automatici: pulisci il parametro non utilizzato, regola le etichette e la descrizione comandi
* [Contenuto] Maschera per tracciati v2
* [Contenuto] Nuova media del nodo della minima varianza (MLV)
* [Contenuto] Nuovo nodo Filtro mediano
* [Content] Quantizza colore: aggiungi l’opzione di filtro &quot;Più vicino&quot;
* [Content] Elenco Spline Bridge: aggiungete parametri di scostamento spline casuali
* [Content] Strumenti spline: nuovo nodo della spline (quadratico)
* [Content] Triangle Grid: modifica il metodo di triangolazione e utilizza i loop
* [Contenuto] Nuove spline Dispersione nel nodo Spline
* [Cooker] Esporre il parametro di base &#39;Pixel ratio&#39; come variabile statica &#39;$pixelratio&#39;
* [CrashReport] Integrazione della nuova finestra di CrashReport
* [Engine] Aggiungi la versione Vulkan/Metal del motore di fusione
* [Grafico] Modalità materiale: consente la connessione all&#39;input senza utilizzo quando è selezionato un singolo collegamento
* [Grafico] Collegamento materiale: consenti connessioni standard quando la connessione non è ambigua
* [Grafico] Strumenti di allineamento dei nodi: aggiunta di distribuzioni orizzontali/verticali, allineamenti sinistro/destro/superiore/inferiore e supporto di nodi sovrapposti
* [Libreria] Correggere il colore del testo nei menu contestuali
* [Parametri] Copiare i parametri da un nodo a un altro
* [Proprietà] &quot;Ripristina tutto&quot;: rimuovi la finestra a comparsa di conferma
* [Resources] Impostare il formato su &quot;All format&quot; nella finestra di dialogo &quot;Link Bitmap&quot;
* [Cerca] Aggiungi un modo per abilitare/disabilitare una modalità ricorsiva
* [Cerca] Aggiungi un modo per abilitare/disabilitare la ricerca fuzzy
* [Cerca] Mostra sempre e attiva il campo dei termini di ricerca quando si abilita Ricerca nodi utilizzando la relativa scelta rapida da tastiera
* [Search] Rielaborare l&#39;opzione di filtro
* [Scelte rapide] Consenti assegnazione tasti &#39;V&#39;, &#39;H&#39; e &#39;S&#39;
* [ThirdParty] Upgrade to Qt 6.5.7
* [UX] Le finestre di dialogo modali non devono essere minimizzabili
* [UX] Rimuovi scorrimento orizzontale nella finestra di dialogo di avviso

**Corretto:**

* [Content] Smussato: il formato normale non è interessato dalla preferenza globale
* [Contenuto] Il nodo Colore da maschera non ignora il canale alfa
* [Content] Distanza direzionale: risultato errato quando l&#39;input ha un rapporto di immagine verticale
* [Content] Mappatura Flood Fill: avviso generato per la variabile assente
* [Contenuto] Calcolo istogramma: il risultato è 16 volte quello che dovrebbe essere
* [Contenuto] Le caustiche RT non funzionano con risoluzione non quadrata
* [Contenuto] Elenco Spline Bridge: risultato errato quando si utilizzano gli offset di inizio/fine
* [Contenuto] Selezione spline: la quantità di spline di output può essere maggiore della quantità di spline di input
* [Content] Spline Warp genera un risultato nero con il motore SSE
* Triangle Grid [Content]: il pattern non viene affiancato correttamente
* [Content] Triangle Grid: la suddivisione in porzioni è interrotta in un caso specifico
* [Data] Arresto anomalo quando si modifica l’identificatore di input del grafico in un caso specifico
* [Grafico a funzioni] I valori lunghi appaiono sovrapposti sui nodi &quot;mobili&quot;
* [Fx-Map] Arresto anomalo durante la visualizzazione delle proprietà del nodo quadrante
* [Grafico] [UDIM] Una barra di scorrimento nell&#39;elenco UDIM genera 1.1 1.2 voci
* [Grafico]&#x200B;[Scelte rapide] Il nodo creato utilizzando una scelta rapida non viene posizionato sul collegamento esistente dopo la duplicazione del nodo
* [Properties] Visualizzazione del parametro non corretta quando il valore non è valido
* [Publish] Le dipendenze reciproche generano un ciclo infinito durante la pubblicazione di un pacchetto
* [Publish] Errore invisibile quando si utilizza l&#39;azione &#39;Publish&#39; su un pacchetto con dipendenza scaricata
* [UI] Il widget &quot;Dimensione principale&quot; non viene visualizzato correttamente quando viene espanso e potrebbe bloccare l’interfaccia (solo macOS)
* [UI] In alcuni casi, la finestra principale si trova dietro ad altre applicazioni (solo Windows)

### 14.0.2

*(Rilasciato Il 10 Ottobre 2024)*

<b>Aggiunto:</b>

* [Grafico a funzioni] Miglioramento dell&#39;allineamento del testo all&#39;interno dei nodi
* [MacOS] Consenti nuovamente l&#39;installazione sulla versione BigSur (11.0)
* [Windows] Consenti nuovamente l’installazione su Windows 10 19H2

<b>Corretto:</b>

* [Bitmap] I tratti di disegno sulla risorsa bitmap non contrassegnano il pacchetto host come modificato
* [Grafico a funzioni] Arresto anomalo quando si chiude un pacchetto con grafico a funzioni che ospita un nodo di istanza
* [Grafico a funzioni] Arresto anomalo quando si annullano due modifiche del nodo Colore di esempio in una riga

### 14.0.1

*(Rilasciato Il 24 Settembre 2024)*

<b>Aggiunto:</b>

* [Motore] Aggiornamento alla Substance Engine 9.1.4
* [Content] Triangle Grid: modifica il metodo di triangolazione e utilizza i loop

<b>Corretto:</b>

* [API] Impossibile caricare di nuovo i plug-in scaricati
* [Contenuto] Calcolo istogramma: il risultato è 16 volte quello che dovrebbe essere
* Triangle Grid [Content]: il pattern non viene affiancato correttamente
* [Data] Arresto anomalo quando si modifica l’identificatore di input del grafico in un caso specifico
* [Engine] Il nodo Distanza produce artefatti quando si utilizzano dimensioni dei pixel molto basse
* [Engine] Risultato nodo Distanza errato con risoluzione 8K sul motore SSE2
* [Grafico a funzioni] I valori lunghi appaiono sovrapposti sui nodi &quot;mobili&quot;
* [Grafico]&#x200B;[Scelte rapide] Il nodo creato utilizzando una scelta rapida non viene posizionato sul collegamento esistente dopo la duplicazione del nodo
* [Properties] Visualizzazione del parametro non corretta quando il valore non è valido

### 14.0.0

*(Rilasciato il 30 luglio 2024)*

<b>Aggiunto:</b>

* [Contenuto] Nuovo filtro Kuwahara anisotropo
* [Content] Nuovo nodo Smusso uniforme
* [Contenuto] Nuovo nodo v2 arrotondato curvatura
* [Content] Nuovo nodo Distanze direzionali
* [Content] Nuovi strumenti istogramma: Calcola, Equalizza, Rendering
* [Contenuto] Nuovo ID per il nodo Maschera
* [Contenuto] Nuovo nodo Normale per la rimozione della combinazione
* [Content] Nuovi nodi della tavolozza: Crea, Applica, Modifica, Visualizza
* [Content] Nuovo nodo Quantize Color
* [Contenuto] Alterazione direzionale non uniforme: imposta il valore predefinito della mappa dell’intensità su 1
* [Content] Aggiungere il suffisso &quot;Color&quot; o &quot;Grayscale&quot; a tutte le etichette dei nodi che dispongono di queste versioni
* [Contenuto] L’opzione &quot;Disturbo bianco&quot; obsoleta mantiene solo &quot;Disturbo bianco veloce&quot;
* [Content] Nodo &#39;Negate Float1&#39; deprecato nel grafico della funzione Substance
* [Content] Rinomina &quot;Quantizza colore&quot; in &quot;Quantizza colore (semplice)&quot;
* [Vista 2D] Visualizza i valori nel pannello Informazioni per i pixel esterni all’intervallo 0-1
* [Engine]&#x200B;[Testo] Nuova crenatura per alcuni font
* [Grafico] Miglioramento del tempo di invalidamento durante la modifica di grafici secondari profondi durante l&#39;utilizzo di un&#39;edizione contestuale
* [Linker] Non duplicare bitmap in SBSASM
* [Parameters] Aggiungere un nuovo widget &quot;function&quot; per tutti i tipi di parametri di input
* [Proprietà] Miglioramento della visualizzazione dei parametri ereditati
* [UX] Miglioramento del supporto del trackpad (solo Mac)
* [UX] Modernizza il panning quando si raggiunge il bordo del grafico durante la selezione
* [UX] Rimozione della funzionalità &quot;Disattiva High DPI&quot;
* [Branding] Nuovo branding per la schermata iniziale e la finestra Informazioni su
* [Gradient Map] Aggiungi un modo per spostare tutti i tasti e il ciclo
* [Library] Imposta tutti i filtri predefiniti su maiuscole/minuscole
* [API] Metodo Add per inserire un frame in un nodo specifico nella finestra della vista Grafico
* [API] Metodo Add per aprire una risorsa pacchetto nel relativo editor (ad esempio, un grafico a Substance nella vista Grafico)
* [API] Aggiungi metodo per selezionare una risorsa pacchetto in Esplora risorse (ad esempio, un grafico a Substance)
* [API] Aggiungi metodi per ottenere e impostare il tipo di grafico di un grafico di composizione Substance
* [ThirdParty] Segui le raccomandazioni sulle piattaforme VFX del 2023
* [ThirdParty] Segui le raccomandazioni sulle piattaforme VFX del 2024
* [ThirdParty] Aggiorna Boost a 1.82.0 + USD a 23.08
* [ThirdParty] Aggiornamento NGL alla 1.38
* [ThirdParty] Aggiorna OpenColorIO alla versione 2.3.x
* [ThirdParty] Aggiornamento di OpenExr alla versione 3.2.x
* [ThirdParty] Aggiornamento di OpenSubdiv alla versione 3.6.x
* [ThirdParty] Aggiorna Python alla versione 3.11.x
* [ThirdParty] Aggiornamento di Qt alla versione 6.5.x
* [ThirdParty] Aggiornamento di gcc alla versione 11.2.1
* [ThirdParty] Aggiorna glibc a 2.28
* [ThirdParty] Aggiorna libstdc++ ABI a C++11 one
* [Documentazione] Nuova pagina &quot;Glossario&quot;

<b>Corretto:</b>

* [Bakers] Arresto anomalo quando si ripristina una scena il cui nome file è stato modificato
* [Bakers] Arresto anomalo durante il salvataggio del predefinito bakers in un file JSON
* [Content] &#39;Dispersione su spline&#39;: Esposizione parametro alfa immagine di input
* [Content] &#39;Tile Sampler Color&#39;: espressione visibleif mancante
* [Contenuto] Disturbo anisotropo: un valore negativo per la quantità X/Y produce un risultato errato
* [Content] Disturbo anisotropo: problema di suddivisione quando si utilizza un valore dispari come quantità X e nessun smoothness
* [Content] Funzione Distrib normale: max() posizionato in modo errato può portare a NaN
* [Contenuto] Le ombre RTAO, Normale piegato e RT non funzionano correttamente su alcune piattaforme
* [Content] Colore fusione splatter forma: le mappe normali OpenGL non vengono fuse correttamente
* [Content] Spazio non garantito dopo il prefisso &quot;Multi&quot; nelle etichette dei nodi
* [Dipendenze] Arresto anomalo quando si sposta il grafico all’interno o tra i pacchetti
* [Engine] Errore di precisione nei nodi di alterazione che influisce sui nodi di sfocatura Pendenza
* [Engine] Il livello SBSAR in SD non è in grado di leggere SBSAR con contenuto SBSASM > 2 GB
* [Grafico a funzioni] Risultato errato per 0^n
* [Grafico] L&#39;opzione &quot;Dimensione del nodo di visualizzazione&quot; è etichettata in modo errato
* [Grafico] Arresto anomalo quando si copia un commento principale in un altro grafico
* [Grafico] Si verifica un blocco quando Alt trascina un nodo Punto
* [Grafico] In alcuni casi, la ricerca nei nodi può non rilevare le corrispondenze evidenti
* [Grafico] Problema di prestazioni durante la modifica di un grafico a funzioni istanziato più volte con il supergrafico aperto
* [Grafico] Troppe invalidazioni durante la creazione di un output
* [Sicurezza] Vulnerabilità scrittura analisi fuori limite ICO
* [Protezione] Elimina alcuni formati immagine inutilizzati
* [Parametri] Il percorso di risorsa PKG bitmap non deve essere modificabile
* [Parametri] Risolvi i problemi relativi all&#39;esposizione/batch che espone il parametro di un processore di valori
* [Parametri] I parametri stringa vengono ignorati quando si espone un batch
* [Proprietà] Problema di prestazioni durante la modifica di un grafico a funzioni istanziato più volte con proprietà aperte
* [SVG] Le modifiche alle forme non vengono applicate nell’immagine rasterizzata
* [UI] Correggere alcuni bug/incoerenze con i widget scorrevoli (solo Windows)
* [UI] Ordine incoerente dei formati di file di scena 3D negli elenchi di importazione/esportazione
* [UI] Le azioni della finestra sono duplicate nell&#39;interfaccia utente
* [Controllo versione] Lo script &#39;perforce.py&#39; non funziona su Python 3

## Versione 13

### 13.1.2

*(Rilasciato il 16 aprile 2024)*

<b>Aggiunto:</b>

* [Grafico] Non posizionare nodi duplicati sopra il nodo originale
* [Grafico] Migliorare l&#39;allineamento dei commenti collegati ai nodi
* [Grafico] Migliorare lo spostamento dei commenti
* [Grafico] Agganciare alla griglia i fotogrammi incollati/duplicati e i commenti
* [Fotogrammi] Aggancia nuovi fotogrammi e commenti alla griglia
* [Content] &quot;Curvatura uniforme&quot;: aggiungete una nota sul supporto della suddivisione in porzioni nella descrizione
* [3DView]&#x200B;[IRay] Consente l&#39;assegnazione dell&#39;output int al parametro enum
* [AxF] Aggiungi proprietà sul modello di camice trasparente
* [AxF] Miglioramento della gestione degli errori durante l’esportazione
* [AxF] Miglioramento dei materiali GLSLFX e MDL per la rappresentazione &quot;SVBRDF&quot; come memorizzati in un file AXF
* [AxF] Rimuovere la proprietà &#39;CC No Refraction&#39; dal modello &#39;AxF to AxF&#39;
* [AxF] Rinomina le proprietà &quot;properties.has\_xxx&quot; in &quot;features.has\_xxx&quot;
* [AxF] Aggiorna il modello per includere tutte le proprietà utilizzate dai nostri shader SVBRDF

<b>Corretto:</b>

* [Vista 3D] Arresto anomalo durante la reimpostazione di un parametro Int MDL mappato a un enumeratore MDL
* [Vista 3D] Widget errati per le proprietà dello shader SVBRDF quando il materiale viene reimpostato dopo la modifica della scena 3D
* [Vista 3D] Widget non corretti per le proprietà dello shader SVBRDF quando non viene applicato alcun grafico
* [Vista 3D] Il pulsante &quot;Mostra ambiente&quot; è disabilitato per le nuove viste senza file SBSSCN predefinito
* [Vista 3D] Il passaggio dal modulo di rendering Iray a OpenGL disconnette l’output di un grafico
* [AxF] La variante Fresnel non viene aggiornata dall&#39;output del grafico
* [AxF] Le etichette delle proprietà dello shader AxF sono formattate in modo incoerente
* [AxF] L&#39;avviso relativo alle risorse non modificate viene visualizzato solo in Console
* [Content] &quot;Non uniforme&quot; non viene scritto in modo uniforme in tutti i nodi
* [Content] Dispersione sulla spline: pattern mancanti sulle spline del ponte
* [Content] Mappatura spline: si verifica un blocco quando si imposta un valore &#39;Quantità segmento&#39; negativo
* [Content] &#39;Symmetry&#39;: etichette mancanti e incoerenti
* [Grafico] I commenti esistenti sono leggermente sfalsati
* [Sicurezza] Vulnerabilità di lettura dei file RAS che analizzano elementi fuori limite

### 13.1.1

*(Rilasciato L&#39;8 Febbraio 2024)*

<b>Aggiunto:</b>

* [AxF] Aggiungere proprietà booleane hasClearCoat, hasSheen e così via.
* [AxF] Aggiungi alcune proprietà mancanti
* [AxF] Consenti importazione EP-SVBRDF
* [AxF] Rinomina proprietà &quot;anisotropiche&quot;, &quot;fresnel&quot; e &quot;fresnel variant&quot;
* [AxF] Aggiornamento ad AxF-Editing 1.0.0
* [Grafico] Incolla sulla posizione del mouse se la posizione all&#39;interno della vista Grafico
* [UX] Aumenta il height del campo di testo &quot;Descrizione&quot; di Frame e Comment
* [UX] Attivare i campi dell&#39;edizione di testo durante la creazione di cornici, commenti o perni

<b>Corretto:</b>

* [AxF] I valori della mappa &quot;Colore Specular&quot; non sono corretti durante l&#39;esportazione
* [AxF] L’anteprima e le texture non vengono visualizzate correttamente nella finestra di dialogo &quot;Importa AxF&quot;
* [AxF] La proprietà &#39;CC No Refraction&#39; non viene inserita correttamente nel modello &#39;AxF to AxF&#39;
* [Content] &quot;Flood Fill alla posizione&quot; è assente dalla libreria
* [Content] &#39;Splatter Circular&#39;: i valori negativi &#39;Pattern Amount&#39; generano calcoli molto lunghi e intensi
* [Content] &#39;Elenco unione spline&#39;: ordine di input errato
* [Dipendenze] La dipendenza viene rimappata alla relativa copia dopo essere stata salvata come copia
* [Frame] Il pulsante &quot;Attiva marcatura HTML&quot; non viene attivato quando si annulla l’utilizzo
* [Fotogrammi] La selezione di un fotogramma e il suo contenuto provoca lo spostamento dell’intero contenuto del fotogramma durante l’espansione automatica
* [Grafico] I commenti duplicati dai commenti associati vengono sempre inseriti all’origine del grafico
* [Grafico] L’interruzione di riga nel commento è più severa durante la creazione
* [Publish] Imposta il percorso predefinito per la pubblicazione SBSAR sulla cartella &quot;Documenti&quot;
* [SBSAR] La ripetizione del caricamento SBSAR lo rende modificabile e i suoi dati possono andare persi

### 13.1.0

*(Rilasciato il 12 dicembre 2023)*

<b>Aggiunto:</b>

* [Fotogrammi] Espansione automatica
* [Cornici] Modifica le regole per definire quando un oggetto appartiene a una cornice
* [Cornici] Disattiva il ridimensionamento del testo per la descrizione delle cornici
* [Cornici] Adatta dimensioni a contenuto
* [Fotogrammi] Nuovo stato predefinito, passaggio del mouse e stati selezionati
* [Cornici] Aggancia a griglia grande
* [Frames] Codice HTML di supporto per la descrizione dei fotogrammi
* [Frame] Aggiorna le zone di interazione
* [Frame] Aggiorna aspetto visivo
* [Grafico] Crea il nodo al centro del collegamento visibile anziché al centro del collegamento
* [Grafico] Visualizza le proprietà di un elemento se è l&#39;unico elemento con proprietà disponibili in una selezione
* [Grafico] Rimuovi l&#39;opzione &quot;Ridimensionamento&quot; per i commenti nel grafico
* [Grafico] Agganciare i nodi sulla griglia principale durante l&#39;operazione di copia/incolla
* [UX] Consenti ricerca fuzzy nel menu Nodo e Ricerca libreria
* [UX] Eseguire il ciclo continuo dell&#39;elenco dei menu Nodo
* [AxF] Supporto dell&#39;esportazione AxF
* [AxF] Disattiva AxF su Linux
* [API] Imposta la proprietà &quot;Visible if&quot; dei parametri del grafico, degli input e degli output utilizzando l’API Python
* [API] Imposta l’ordine di I/O del grafico utilizzando l’API Python
* [Dipendenze] Aggiorna Incremento a 1.80.0
* [Dipendenze] Aggiornare OpenSubdiv alla versione 3.5.x
* [Dipendenze] Aggiornamento di gcc alla versione 11.2.1 - Problema con Iray/MDL C++20
* [Dipendenze] Aggiornate FBX SDK al 2020.3
* [Dipendenze] Aggiorna NGL in 1.35.0.20
* [Gestione colore] Aggiungi il supporto per i display ICC OCIO
* [Livelli] Aggiungi un modo per ripristinare l’istogramma
* [Python] Avvisa gli utenti se non è possibile importare QtForPython
* [Vista 2D] Salva lo stato delle opzioni di visualizzazione
* [Vista 3D] Tecnica Aggiungi posizione allo shader delle informazioni sulla trama
* [Esporta] Aggiungi un pulsante &quot;Salva impostazioni&quot; per salvare le modifiche alle opzioni di esportazione

<b>Corretto:</b>

* [Vista 3D] Impossibile assegnare una texture a un input di tipo texture\_2d di un materiale MDL
* [AxF] Gli identificatori grafici nell&#39;elenco dei modelli possono essere vuoti
* [AxF] Il campo modello grafico Substance è vuoto per impostazione predefinita
* [Content] Atlas scatter: comportamento errato in casi specifici
* [Content] Mappatura Flood Fill: output vuoto quando tutte le forme hanno la stessa dimensione Bbox
* [Content] Riempimento a posizione: artefatti di imprecisione in alcune situazioni
* [Content] Output &#39;Specular&#39; errato nel nodo &#39;BaseColor/Metallic/Roughness converter&#39;
* [Contenuto] Maschera su tracciato non funziona in verticale non quadrato
* [Content] Descrizione mancante per i nodi Valore di input, Scala di grigi di input, Colore di input e Output
* [Content] Descrizione mancante per i nodi Set e Sequence
* [Content] Splatter forma: artefatti di imprecisione nell&#39;output &#39;Splatter data 2&#39;
* [Engine] I booleani nei processori di valore restituiscono sempre &#39;False&#39; (solo Apple Silicon)
* [Esplora risorse] L&#39;ordine dei pulsanti della barra degli strumenti non è coerente tra i sistemi operativi
* [Fotogrammi] Non acquisire i nodi quando si sposta un fotogramma con il modificatore CTRL
* [Gradient Map] reimposta tutte le opzioni dovrebbe ripristinare anche il widget della sfumatura
* [GraphRender] Alcuni nodi vengono renderizzati in nero quando si modifica in modalità di anteprima
* [Grafico] L’anteprima &quot;Valore di input&quot; è bloccata su &quot;False&quot; quando si modifica il valore booleano predefinito (solo Apple Silicon)
* [Grafico] I nodi punto vicini al bordo del fotogramma non vengono spostati dal fotogramma
* [Interoperabilità] L&#39;icona di reinvio non viene aggiornata dopo l&#39;invio a Substance 3D Stager
* [MDL] Impossibile modificare la rugosità nei nodi in cui è disponibile questo parametro
* [MDL] Connessioni non valide nel modello &#39;AxF to Metallic Roughness&#39;
* [UI] La finestra &quot;Esporta output&quot; può essere ridotta a icona (solo Windows)
* [UI] Le immagini appaiono pixelate nella schermata Info su quando si utilizza il ridimensionamento della visualizzazione
* [UI] Strumenti di allineamento dei nodi nella barra degli strumenti del grafico creazione di più passaggi di annullamento

### 13.0.2

*(Rilasciato il 27 luglio 2023)*

<b>Aggiunto:</b>

* [Grafico a funzioni] Aggiungi variabile di sistema $getPhysicalSize
* [Schermata Home] Supporto per l’apertura di file SBS mediante trascinamento
* [Content] Mappatura spline/Mappatura flusso spline : Aggiungi parametro &#39;Correzione non quadrata&#39;

<b>Corretto:</b>

* [Schermata Home] Non visualizzare la schermata Home quando un file viene inviato da un altro software
* [Schermata Home] Stato errato dell’icona di Designer nella barra degli strumenti di Windows
* [Content] Atlas splitter: descrizione non corretta
* [Content] Valore di riferimento errato nella funzione &#39;Linear to sRGB (luminanza)&#39;
* [Content] Lo strumento di visualizzazione dei numeri non supporta risoluzioni non quadrate
* [Content] Elenco punti: il valore minimo del parametro &#39;Point number&#39; non è corretto
* [Content] Ombra esterna forma: l&#39;ombra può scomparire quando la suddivisione in porzioni è disattivata
* [Contenuto] Spline (Poly Quadratic): anteprima non corretta delle tangenti e del thickness con risoluzioni non quadrate
* [Content] Spline (Poly Quadratic): le etichette dei punti non vengono nascoste quando si utilizzano le opzioni di connessione di inizio/fine
* [Content] Bridge spline (elenco): il parametro &#39;Correzione non quadrata&#39; non ha effetto
* [Contenuto] Spline Cubic: il parametro di correzione non quadrato non ha effetto sull’output di anteprima
* [Contenuto] Mappatura spline: rendering errato quando la spline ha un thickness molto piccolo
* [Content] Nodi spline: descrizione del segno alfa invertito nella descrizione del comando Spine Coords
* [Content] Nodi spline: il parametro &quot;Correzione non quadrata&quot; non ha effetto sull&#39;output di anteprima
* [Content] Rendering spline: il formato di output è assoluto 32F
* [Content] Rendering spline: l&#39;output è bloccato nell&#39;intervallo [0, 1]
* [Contenuto] Thickness di campionamento spline: la spline può essere sottratta in valori negativi
* [Contenuto] Selezione spline: per impostazione predefinita, le spline vengono chiuse con un singolo segmento
* [Arresto anomalo]&#x200B;[Cooker] Arresto anomalo durante il caricamento di grafici specifici
* [Arresto anomalo]&#x200B;[UI] Arresto anomalo durante l’attivazione dei menu dopo il caricamento del pacchetto dalla schermata Home
* [API] Il collegamento &quot;Documentazione utente&quot; nel riferimento agli script è obsoleto
* [Properties] Impossibile aprire la funzione Value Processor in un grafico bloccato
* [Publish] Impossibile pubblicare pacchetti contenenti grafici MDL
* [UI] L’opzione &quot;Gestisci account...&quot; è disattivata nel menu Aiuto
* [UI] Voci mancanti nel menu Aiuto quando si apre Designer tramite un file

### 13.0.1

*(Rilasciato Il 27 Giugno 2023)*

<b>Aggiunto:</b>

* [Content] Spline (Poly Quadratic), Elenco punti: aggiungete il nome dei punti nell&#39;output di anteprima
* [Content] Mappatura spline: aggiungete un parametro per spostare il centro del profilo del cilindro
* [DotNode] Ordina l&#39;elenco dei portali di input in ordine alfabetico

<b>Corretto:</b>

* [Contenuto] Risultato errato in diversi nodi della spline quando si utilizza la distribuzione uniforme
* [Content] Errori minori nelle descrizioni comandi dei nodi Spline &amp; Path
* [Content] Quad Transform on Path: i valori predefiniti p01 e p10 sono modificati
* [Content] Quad Transform: il risultato non è corretto in una situazione specifica
* [Contenuto] Cerchio spline: il risultato &quot;Capovolgi direzione&quot; non è corretto quando non si utilizza la distribuzione uniforme
* [Contenuto] Cerchio spline: le tangenti non sono corrette durante la regolazione dei parametri di spirale e dimensione
* [Content] Mappatura flusso spline: striature nere nel risultato quando si utilizza la potenza a spirale elevata in Spline Circle
* [Content] Mappatura spline / Mappatura UV: il colore di sfondo non funziona
* [Content] Mappatura spline: il height di base è 0, con conseguente ritaglio
* [Content] Mappatura spline: il height spline viene modificato dal moltiplicatore di input anche quando l&#39;input non è collegato
* [Content] Mappatura spline: le estremità spline che soddisfano un bordo immagine non vengono mappate
* [Content] Mappatura spline: la Scala UV Y non ha effetto quando si utilizza una forma non piana
* [Content] Mappatura spline: combattimento a Z durante il rendering di spline sovrapposte dello stesso height
* [Content] Spline Poly Quadratic: il risultato &#39;Capovolgi direzione&#39; non è corretto quando non si utilizza la distribuzione uniforme
* [Content] Rendering spline: i giunti non vengono gestiti in modo uniforme tra le opzioni Stile spline
* [Content] Rendering spline: l&#39;ultimo segmento non viene disegnato
* [Contenuto] Rendering spline: la correzione non quadrata non viene applicata correttamente
* [Contenuto] Il colore della mappatura UV viene visualizzato due volte nella libreria
* [DotNode] L&#39;area di aggancio della connessione non viene aggiornata dopo la disattivazione del limite di ridimensionamento del testo
* [DotNode] La creazione tramite menu di scelta rapida è interrotta
* [DotNode] La posizione del nome del portale di input non viene modificata dopo l&#39;annullamento o la ripetizione di una modifica del nome
* [GraphRender] Troppi errori durante la modifica di un grafico a funzioni
* [Grafico] La posizione del widget di trasformazione non viene aggiornata correttamente
* [Localizzazione] I parametri &#39;Soft range&#39; e &#39;Hard range&#39; non sono localizzati nei grafici MDL
* [Parametri] Le modifiche consecutive al testo non vengono registrate nello stack di cronologia
* [Parametri] Hitbox per spostare i parametri di input del grafico nell&#39;elenco non è affidabile
* [Proprietà] Un clic semplice è considerato come un doppio clic sul widget della casella di selezione nei progetti pesanti
* [Publish] L’ordine delle risorse nel pacchetto non viene mantenuto nella risorsa pubblicata

### 13.0.0

*(Rilasciato Il 6 Giugno 2023)*

<b>Aggiunto:</b>

* [Grafico] Nodo portale
* [Onboarding] Nuova schermata iniziale
* Nodo [Content] Spline (Cubic)
* Nodo spline (poli quadratico) di [Content]
* [Content] Spline Circle, nodo
* [Content] - Nodo elenco punti
* Nodo [Content] Spline Bridge (2 spline)
* Nodo [Content] Spline Bridge (List)
* [Content] Spline - Aggiungi nodo
* [Content] Spline Seleziona nodo
* [Contenuto] Nodo Elenco unione spline
* [Content] Spline 2D Transform, nodo
* [Contenuto] Nodo Alterazione spline
* [Content] Spline Nodo Height di esempio
* [Content] Spline Nodo Thickness di esempio
* [Content] Nodo Rendering spline
* [Content] Dispersione sul nodo Colore spline
* [Contenuto] Dispersione sul nodo Scala di grigi spline
* [Content] Nodo colore di Spline Mapper
* [Content] Spline Mapper Nodo in scala di grigi
* [Content] Spline Bridge Mapper Nodo colore
* [Content] Spline Bridge Mapper Nodo in scala di grigi
* [Content] Nodo Mappatore flusso spline
* [Content] Nodo colore mappatore UV
* [Contenuto] Nodo in scala di grigi con mappatura UV
* [Content] Percorsi al nodo Spline
* Nodo [Contenuto] Maschere su tracciati
* [Content] Nodenode trasformazione tracciati 2D
* Nodo poligono [Content] Paths
* [Contenuto] Nodo Anteprima tracciati
* [Contenuto] Nodo Alterazione tracciati
* [Content] Seleziona tracciati, nodo
* [Content] Nodo processore vertici tracciati
* [Content] Elaboratore vertici tracciati Nodo semplice
* [Content] Quad Transform sul nodo Path
* [Content] Occlusione ambientale con ray tracing v2
* [Contenuto] Normale curvato con ray tracing v2
* [Content] Ombre con ray tracing v2
* [Engine] Aggiornamento alla versione 9
* [Engine] Nodo loop nei grafici di funzione
* [Motore] Aggiungi modalità solida a Sfumatura
* [Engine] Nodo atomic pow() nel grafico delle funzioni
* [Engine] Aggiungi opzioni di disposizione dei bordi (blocco a spigolo / ripetizione) nel nodo Sampler
* [Engine] Campionamento più vicino nei nodi Altera e Alterazione direzionale
* [Motore] Aggiungete una modalità &quot;punchthrough alfa&quot; al filtro Nitidezza per gli input di colore
* [Engine] FxMap: morphlet Emisfero
* [Engine] Operazioni Atomic Get/Set nei grafici delle funzioni
* [Motore] Funzioni: utilizzare la funzione precisa di log/log2/exp, 2pow - Unificare le funzioni tra la cucina e il motore
* [Engine] Aggiungete un parametro di &quot;offset intensità&quot; al filtro Alterazione direzione
* [API] Supporto della gestione dei predefiniti per la composizione di grafici
* [Funzioni] Modificare il nome di input per le funzioni nodi atomici
* [Localizzazione] Aggiungere le lingue portoghese (Brasile), italiano (Italia) e spagnolo (Spagna)
* [Localizzazione] Rispetta la regola &quot;Lingua (Paese)&quot; nell’elenco delle lingue
* [Predefiniti] Disattiva i pannelli &quot;Anteprima&quot; e &quot;Predefiniti&quot; nelle proprietà del grafico quando si utilizza la modifica in contesto
* [Grafico modelli Substance] Fine del supporto dei grafici modelli Substance

<b>Corretto:</b>

* [Vista 3D] La visualizzazione di stringhe lunghe nelle statistiche delle scene è tagliata (solo macOS)
* [API] Il modulo &#39;structure::Structure&#39; è ancora incluso nel riferimento API
* [API] I nodi dei punti nei grafici MDL non hanno definizioni né proprietà
* [API] Comportamento errato durante l&#39;impostazione del parametro dei nodi di funzione
* [Content] Voronoi 3D e i nodi 3D voronoi fractal generano un avviso di cottura
* [Engine] Il parametro &#39;Intensity Map Offset&#39; non ha alcun effetto sui dati in scala di grigi nel motore SSE2
* [Explorer] È possibile eliminare l&#39;i/o del grafico
* [Graph] La bitmap viene ignorata quando viene utilizzata nelle istanze
* [Grafico] Posizione del nodo punto errata durante la creazione del nodo da un nodo
* [Grafico] Attivazione errata nella finestra di dialogo &#39;Esporta parametro&#39; quando si utilizza il tasto &#39;Invio&#39;
* [Grafico] Risultato errato nella scansione dell&#39;istogramma con bitmap nella modifica del contesto
* [Localizzazione] Risolvere vari problemi di ritaglio
* [Parametri] Arresto anomalo quando si elimina un parametro di input
* [Publish] I grafici nelle cartelle vengono spostati nella cartella principale nel pacchetto pubblicato
* [Resources] Arresto anomalo durante l&#39;aggiornamento di una risorsa caricata sul disco
* [VisibleIf] Correggere la regressione nella valutazione della visibilità condizionale

## Versione 12

### 12.4.1

*(Rilasciato: 30 marzo 2023)*

**Aggiunto:**

* [Cooker]&#x200B;[Grafico] Tenere in considerazione i tag di trasformazione EXIF nel file JPEG
* [Sicurezza] Aggiorna a USD 23.02
* [Sicurezza] Rimuovi il supporto per l&#39;importazione di formati di file Collada (.dae)
* [Modelli di Substance] Avvertenza sulla fine del ciclo di Substance dei grafici dei modelli nella prossima versione principale

**Corretto:**

* [3D View]&#x200B;[ASM] Rivestimento dell&#39;artefatto di rugosità quando si utilizza CoatNormal
* [Content] Il parametro &#39;Gradient Filled Cella&#39; del nodo Alveolus è invertito
* [Content] Il numero di input dei nodi Multi-Switch non è bloccato
* [Contenuto] Avviso di cottura nel nodo Normale di Generator Scratches
* [Data] Arresto anomalo durante il caricamento manuale del pacchetto dopo aver annullato il caricamento precedente
* [Data] Arresto anomalo quando si annullano rapidamente più operazioni grafiche fino al caricamento del pacchetto

### 12.4.0

*(Rilasciato il 31 gennaio 2023)*

**Aggiunto:**

* [Vista 3D] Aggiungi tutte le opzioni del menu Visualizza come pulsanti della barra degli strumenti
* [API] Consenti l’aggiunta di azioni alle barre degli strumenti della visualizzazione grafico
* [API] Consenti di creare, modificare o valutare un grafico del modello di Substance dall’API
* [Gestione colore] Migliorare la qualità delle LUT 3D al forno in modalità ACE
* [Documentazione] Progetti di esempio per Substance grafici di composizione
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
* [UI] L’elemento attivo non è evidenziato nel browser Scena
* [UX] Reimposta gli intervalli del cursore quando il loro valore viene reimpostato

**Corretto:**

* [API] SDProperty.getDefaultValue() restituisce quasi sempre Nessuno
* [Vista 3D] Il valore della proprietà &quot;DirectX normale&quot; non è condiviso tra i moduli di rendering
* [Vista 3D] La visualizzazione delle statistiche della scena viene estesa quando la finestra della vista è piccola
* [Vista 3D] La proprietà di visualizzazione Wireframi non viene salvata
* [Contenuto] I parametri del colore Sfocatura radiale non hanno effetto sul canale alfa
* [Localizzazione] Ulteriori cursori e pulsanti vengono visualizzati in Proprietà OpenGL dell&#39;ambiente.
* [MDL]&#x200B;[Substance modello] Arresto anomalo durante l&#39;eliminazione di nodi esposti
* [Preferenze] Il file predefinito\_config non viene mai ricreato se viene eliminato
* [Modello Substance] Parametro di riordinamento in caso di arresto anomalo che non viene visualizzato a livello di istanza

### 12.3.1

*(Rilasciato il 24 novembre 2022)*

**Aggiunto:**

* [3DView] Rendering ottimizzato per scene con molti materiali
* [3DView] Visualizzare gli output di un grafico del modello di Substance quando viene rilasciato da Esplora risorse
* [Licenza] Clean legacy system per utenti Linux
* [Onboarding] Aggiorna la trasparenza dello sfondo
* [Modelli di Substance] Visualizza un avviso nella vista Grafico quando l&#39;input e l&#39;output condividono lo stesso identificatore

**Corretto:**

* [Risorse 3D] &quot;Guida > Risorse Substance 3D&quot; è erroneamente destinato a Creative Cloud Desktop su Linux
* [Vista 3D] I materiali non vengono creati quando viene caricata la trama
* [Vista 3D] L&#39;elenco dei materiali viene aperto quando si rilascia il grafico del modello di Substance nella finestra della vista
* [Explorer] Impossibile eliminare la selezione con la tastiera se è incluso un grafico del modello di Substance
* [Explorer] Arresto anomalo all&#39;apertura del menu di scelta rapida di un elemento materiale di una risorsa trama in Mac
* [Grafico] Le istanze le cui immagini di input dipendono da Valori generano risultati errati nei nodi successivi
* [Grafico] Risultato errato quando si utilizza la catena di grafici secondari con la modifica contestuale dei grafici abilitata
* [MDL] Arresto anomalo durante il caricamento di un grafico MDL che fa riferimento a un grafico di composizione con output obsoleti
* [MDL] Il nodo 2D Texture non funziona più
* [Onboarding] Testi ritagliati e non localizzati
* [Onboarding] I pannelli non vengono visualizzati correttamente quando si avvia l’app aprendo un file
* [Preferenze] La cache delle immagini ignora il percorso dei file temporanei impostato dall&#39;utente
* [Proprietà] Le modifiche eseguite nei pannelli di anteprima/predefiniti vengono unite nella pila di annullamento
* [Scelta rapida] La scelta rapida assegnata ai nodi obsoleti crea conflitti e non può essere pulita
* [Substance modelli] Arresto anomalo quando si chiude un pacchetto dopo aver eseguito azioni specifiche
* [Modelli di Substance] I nodi delle istanze e i collegamenti dai pacchetti riposizionati non vengono aggiornati correttamente
* [Modelli di Substance] L&#39;annullamento dell&#39;eliminazione dei grafici secondari non aggiorna i nodi delle istanze e i collegamenti in modo coerente
* [Modelli Substance] Il valore aumenta improvvisamente troppo velocemente sul nodo di trasformazione
* [UI] Le icone di avviso della proprietà &quot;Visible if&quot; non dispongono di una descrizione comandi
* [UI] Il testo delle informazioni sull&#39;immagine è troppo scuro nella finestra della vista di 2D View
* [Annulla] Quando si sposta un widget posizione in modalità di anteprima vengono memorizzati tutti i valori intermedi

### 12.3.0

*(Rilasciato il 6 ottobre 2022)*

**Aggiunto:**

* [Generale] Pannello Onboarding per accogliere nuovi utenti
* [Generale] Novità del pannello per migliorare la ricerca di nuove funzioni
* [Modello Substance] Supporto di sottografi e istanze
* [Modello Substance] Supporto Visibile se per i parametri esposti
* [Modello Substance] Aggiunta del supporto dei nodi di output
* [Modello Substance] Nodo offset curva
* [Modello Substance] Nodo di ripristino della curva
* [Modello Substance] Nodo di arrotondamento della curva
* [Modello Substance] Nodo di suddivisione della curva
* [Modello di Substance] Nodo dell&#39;innesto
* [Modello Substance] Aggiornamento del nodo &quot;Filtra scena&quot;
* [Modello Substance] Rendere individuabili i nodi non atomici nel menu Nodo
* [Modello Substance] Aggiungere l&#39;azione &quot;Apri riferimento&quot; nel menu di scelta rapida di un nodo di variante
* [Substance modello] Aggiungere un&#39;azione &quot;Visualizza in 3DView&quot; nel menu contestuale dei nodi che possono essere inviati a 3DView
* [Substance modello] Visualizza automaticamente le proprietà di un nodo dopo averlo esposto
* [Modello Substance] Finestra Crea &quot;Nuovo grafico modello Substance&quot; con elenco modelli
* [UI] Migliorare la coerenza delle opzioni di salvataggio delle immagini in Vista 2D e Vista 3D
* [UI] Rinomina &quot;Collega > Trama 3D&quot; in &quot;Collega > Scena 3D&quot; nel menu di scelta rapida di Explorer
* [UI] Il ripristino del layout ora si applica a tutte le finestre mobili
* [UI] Usa l&#39;etichetta &quot;Visualizza output in vista 3D&quot; nei menu contestuali per i grafici
* [Library] Supporta i grafici dei modelli di Substance non atomici
* [SBSAR] Descrizione dei grafici di supporto nella SBSAR
* [Shader] Impostate il valore predefinito del fattore di tassellatura su 1 per tutti gli shader
* [UI] Esporre il widget a 2 pulsanti per i parametri booleani
* [Engine] Aggiornamento alla versione 8.6.4
* [Steam] Versione ottimizzata per chipset Apple Silicon (Apple M1 / M2)

**Corretto:**

* [UI] Risoluzione dei problemi di ridimensionamento per schermi ad alto DPI
* [UI] Modello &#39;$(udim)&#39; mancante dall&#39;elenco nella finestra di cottura
* [UI] Arresto anomalo durante la visualizzazione del menu Nodo sul bordo destro dello schermo (solo macOS)
* [UI] Il pulsante dell’estensione nel menu della vista 3D non è visibile
* [UI] Il menu dell&#39;estensione della barra degli strumenti Grafico è incompleto
* [UI] Valore del widget del parametro errato dopo aver annullato l’attivazione dell’intervallo rigido
* [Vista 3D] L&#39;impostazione dello shader non predefinita viene persa su Iray da una sessione a un&#39;altra
* [Bakers] Arresto anomalo durante il caricamento della finestra di cottura con una scena senza trame
* [Funzione] Arresto anomalo quando si copia un’istanza nel grafico a cui fa riferimento
* [Funzione] Correggere un possibile arresto anomalo durante la manipolazione dei nodi
* [Globalizzazione] Il corsivo non è sempre disabilitato correttamente in giapponese, coreano e cinese
* [Grafico] Identificatore fallback errato per i nuovi grafici MDL e Substance modelli
* [Grafico] I parametri ereditati guidati da valori a volte vengono calcolati in modo errato
* [GraphRender] Arresto anomalo durante il cambio di motore durante l&#39;elaborazione del grafico ad alta risoluzione (solo macOS)

### 12.2.1

*(Rilasciato il 4 agosto 2022)*

**Corretto:**

* [Grafico] Risultati errati quando si modifica la dimensione principale del grafico
* [Arresto anomalo] Arresto anomalo durante l’elaborazione di un grafico di composizione Substance a una risoluzione molto elevata
* [Arresto anomalo] Arresto anomalo quando si esaurisce la memoria durante il caricamento del pacchetto
* [Arresto anomalo] Arresto anomalo quando si utilizza la parentesi nelle annotazioni del parametro esposto in un grafico del modello di Substance
* [Arresto anomalo] Migliorare la stabilità del rendering dei grafici di composizione della Substance
* [Iray] Aggiornamento alla versione 2021.1.6

### 12.2.0

*(Rilasciato il 19 luglio 2022)*

**Aggiunto:**

* [Apple] Supporto nativo per Apple Silicon (M1) (solo versione di Creative Cloud)
* [Substance grafico modello] Visualizza descrizioni comandi nodo in vista grafico
* [Substance grafico modello] Visualizza descrizioni comandi nodo nella libreria
* [Substance grafico modello] Aggiungi una voce di menu contestuale per visualizzare in anteprima i nodi
* [Substance grafico modello] Consente all&#39;utente di creare scelte rapide per la creazione di nodi
* [UI] Aggiungi l’opzione &quot;Visualizza output in vista 2D&quot; nel menu di scelta rapida del grafico di composizione
* [UI] Suddividi l&#39;impostazione &quot;Visualizzazione automatica degli output&quot; in impostazioni specifiche della vista 2D/3D
* [UI] Aggiungi freccia a discesa e descrizione comandi al pulsante &quot;Visualizza output&quot; nella barra degli strumenti Visualizzazione 2D
* [UI] Rimodellare e riordinare gli elementi nel pannello Informazioni di Esplora risorse
* [Gestione colore] Aggiungere gli spazi colore di esportazione &quot;Linear Adobe RGB (1998)&quot; e &quot;Adobe RGB (1998)&quot; per Adobe
* [Gestione colore] Aggiungi spazio colore di lavoro &quot;Linear Adobe RGB (1998)&quot; per Adobe
* [Gestione colore] Aggiungi il supporto per i display ICC OCIO
* [Gestione colore] Nascondi lo spazio colore di lavoro di Adobe RGB dalle preferenze ACE
* [Gestione colore] Migliorare la qualità delle LUT 3D al forno in modalità ACE
* [Gestione colore] Utilizza il nuovo back-end GPU nel visualizzatore 3D
* [Localizzazione] Aggiornamento completo della lingua coreana
* [Engine] Aggiornamento alla versione 8.6.0
* [Grafico] Assegna un identificatore grafico predefinito quando la proprietà viene lasciata vuota
* [Library] Disattiva i collegamenti ipertestuali delle descrizioni comandi per i nodi non di istanza
* [NewProject] Aggiorna risoluzione predefinita
* [Modelli] Aggiungi modello CLO
* [API] Esporre la proprietà defaultParentSize per gli oggetti SDSBSCompGraph
* [Dipendenze] Aggiorna Alembic alla versione 1.8.3
* [Dipendenze] Aggiornamento di AXF alla versione 1.9.0
* [Dipendenze] Aggiornamento della versione avanzata alla versione 1.76
* [Dipendenze] Aggiorna FBX alla versione 2020.2.1
* [Dipendenze] Aggiorna IRay alla versione 2021.1.0
* [Dipendenze] Aggiorna OpenColorIO alla versione 2.1.1
* [Dipendenze] Aggiorna OpenEXR alla versione 3.1.5
* [Dipendenze] Aggiorna TBB alla versione 2020.3
* [Dipendenze] Aggiorna USD alla versione 0.22.3
* [Rimuovi] Disattiva la funzione post effetti (Sì)
* [Rimuovi] Rimuovi il comando &quot;Salva rendering su Artstation&quot; dal menu Vista 3D

**Corretto:**

* [Modelli Substance] L&#39;intervallo rigido impostato sul parametro esposto viene salvato quando si annulla l&#39;esposizione
* [Modelli di Substance] L&#39;identificatore non è di facile utilizzo sui nodi costanti
* [Substance modelli] Miglioramento della ricerca in base alla compatibilità dei nodi
* [UI] L&#39;ordine del sottomenu &quot;Nuovo&quot; non è corretto per le risorse della cartella
* [UI] La dimensione predefinita della finestra principale è molto piccola
* [UI] Le barre degli strumenti non sono interessate dall’opzione &quot;Ripristina layout&quot;
* [UI] Griglia di trasparenza visibile sull&#39;icona della risorsa font in Esplora risorse
* [Cooker] I grafici di composizione istanziati nel grafico MDL vengono sempre completamente ricolorati
* [Grafico] Arresto anomalo quando si incolla un nodo copiato da un grafico con identificatore vuoto
* [MDL] Arresto anomalo quando si chiude un grafico MDL specifico
* [Prestazioni] L&#39;applicazione non risponde durante il caricamento di pacchetti di grandi dimensioni
* [Resources] Le risorse Scena 3D possono essere importate in un caso specifico

### 12.1.1

*(Rilasciato il 7 giugno 2022)*

**Corretto:**

* [Content] La risorsa &quot;bluenoise\_256&quot; ha un attributo &quot;colorspace&quot; definito in alcuni nodi
* [Content] I nodi &quot;Ottieni dimensioni&quot; non vengono visualizzati nella libreria e la versione in scala di grigi ha un&#39;etichetta errata
* [Content] Il parametro &quot;Numero colore casuale&quot; nei nodi Voronoi 2D non ha alcun effetto
* [SBSRender] L’esportazione di un grafico in EXR non genera lo stesso bpc di Designer
* [Modelli Substance] &quot;Tipo gamma&quot; non dovrebbe apparire nelle proprietà dei parametri esposti
* [Modelli di Substance] Arresto anomalo quando si utilizza la parentesi nelle annotazioni dei parametri esposti

### 12.1.0

*(Rilasciato il 26 aprile 2022)*

**Aggiunto:**

* [Principale] Nuovo contenuto per i grafici dei materiali
* [Principale] Invio di materiali a Stager
* [Principale] Supporto dei file USD
* [Principale] Miglioramento della segnalazione degli errori nell’interfaccia utente
* [Principale] Nodi di Gestione scene per i grafici dei modelli
* [Contenuto] Aggiungi più opzioni ai Rumori Perlin 3D (affiancatura, assoluto...)
* [Content] Nuovo nodo frattale con disturbo ridotto 3D
* [Contenuto] Nuovo nodo Scostamento texture 3D
* [Content] Nuovo nodo Posizione texture 3D
* [Content] Nuovo nodo superficie di rendering texture 3D
* [Content] Nuovo nodo Volume rendering texture 3D
* [Content] Nuovo nodo Signed distance field texture 3D
* [Content] Nuovo nodo Ritaglio automatico
* [Content] Nuove funzioni di ottimizzazione
* [Content] Nuovi nodi di Extend Shape
* [Content] Nuove Mappe Grunge
* [Contenuto] Nuovo nodo Rotazione non uniforme
* [Contenuto] Nuovo filtro Tabella area sommata
* [Content] Nuovo modulo generatore 2 casuale
* [Contenuto] Nuovo generatore pattern Triangle Grid
* [Content] Nuova versione del nodo Quantizza scala di grigi
* [Content] Nuovi rumori frattali di Voronoi e Voronoi (2D/3D)
* [Content] Threshold: aggiungi modalità di confronto &#39;Lower&#39; e &#39;Lower and equal&#39;
* [Content]&#x200B;[Vista 3D] Aggiungi una trama adatta alla visualizzazione dei tessuti nelle risorse spedite
* [Substance modelli] Nuovo nodo Espandi istanze gruppo
* [Modelli Substance] Nuovo nodo Fuse
* [Substance modelli] Nuovo nodo Rinomina
* [Modelli Substance] Nuovo nodo Reparent
* [Modelli Substance] Nuovo set nodo pivot
* [Substance modelli] Aggiornamento a SDK 1.6.0
* [UI] Migliora il comportamento del menu Nodo quando si fa clic su di esso
* [UI] Apri i grafici secondari nella stessa scheda anche se bloccati
* [UI] Rimuovi il pulsante del perno dalla barra del titolo del pannello Esplora risorse
* [UI] Salva l’opzione &quot;Non visualizzare più&quot; nella schermata di benvenuto nelle diverse versioni
* [ThirdParty] Aggiorna Qt (e QtForPython) alla versione 5.15.8
* [Third Party] Aggiorna Python alla versione 3.9.9
* [ThirdParty] Aggiornamento di OpenSSL a 1.1.1m
* [Vista 3D] Visualizza l&#39;unità della griglia nella finestra della vista quando è attivato l&#39;helper &quot;Asse&quot;
* [Automazione] Fornisci lo strumento da riga di comando sbsbaker con Designer
* [Gestione colore] Implementazione del nuovo back-end GPU per Adobe
* [Cooker] Aggiungi un&#39;opzione per cucinare un pacchetto senza timestamp
* [Grafico] Aggiungere i distintivi nel grafico FxMap
* [Library] Aggiungi un nuovo filtro per le funzioni di regolazione
* [Player] Supporto USD
* [Properties] Aggiunge un errore di avvertenza nel parametro &quot;PKG Resource Path&quot; di un nodo Bitmap quando la risorsa non viene trovata
* [Substance Engine] Aggiornamento alla versione 8.4.1
* [Sì] Avvisa l’utente che gli effetti post di Yebis verranno rimossi nella prossima versione
* [Documentazione] Nuova pagina &quot;Avvisi ed errori&quot;
* [Documentazione] Nuova pagina che descrive l’ereditarietà nei grafici di composizione della Substance
* [Documentation] Aggiornamento della sezione &#39;Iray&#39;
* [Documentazione] Aggiornamento della sezione &quot;Grafici MDL&quot;

**Corretto:**

* [UI] Problemi di ritaglio nelle descrizioni dei modelli nella nuova finestra del grafico
* [UI] Difficile leggere il testo bianco nei nodi quando si utilizza la modalità scura in macOS
* [UI] Problema di layout in alcune finestre di dialogo
* [UI] Il messaggio di avviso viene visualizzato troncato durante la creazione del grafico della funzione Substance in Esplora risorse.
* [UX] Il selettore colore si sposta verso il basso su ogni nuova apertura
* [UX] La finestra dell’editor sfumatura si sposta verso l’alto ogni volta che viene generata
* [UX] Le proprietà del grafico non vengono visualizzate automaticamente per i pacchetti caricati
* [Content] Mappatura Flood Fill: selezione di input errata in un caso specifico
* [Content] Flood Fill: pagina al vivo del testo nei pulsanti dei parametri booleani
* [Contenuto] Intervallo errato per il parametro da multi-angolo a angolo luce primo campione del nodo normale
* [Modelli Substance] Le proprietà del nodo mostrano l&#39;identificatore anziché l&#39;etichetta
* [Substance modelli]&#x200B;[Vista 3D] Problema di aggiornamento durante la riapertura di un progetto
* [Substance models]&#x200B;[3Dview] Problema di aggiornamento quando si utilizza l&#39;anteprima wireframi
* [Parametri] Arresto anomalo quando si eliminano gli input del grafico in rapida successione in un caso specifico
* [Parametri] Arresto anomalo durante la reimpostazione di un parametro di istanza durante la modifica della relativa descrizione di riferimento
* [Bitmap] Il rilevamento UDIM non viene attivato per i file bitmap rilasciati nel grafico
* [Grafico] I nodi Bitmap/SVG non vengono invalidati quando la risorsa viene modificata sul disco dopo aver caricato il pacchetto
* [GraphRender] Perdita di memoria quando la valutazione del grafico Substance viene annullata
* [Localizzazione] La stringa &quot;Ripristina tutte le mappe per questa risorsa&quot; viene visualizzata non localizzata
* [MDL] Parametro esposto inizializzato su 0 se l&#39;input è connesso a un nodo punto non connesso
* [Preferenze] Le descrizioni comandi vengono visualizzate anche quando il cursore si trova in uno spazio vuoto
* [Proprietà] Annullando una modifica del valore dello spazio colore si imposta il valore predefinito anziché in un caso specifico
* [Text] Impossibile annullare il passaggio del font a una risorsa font mancante

## Versione 11

### 11.3.3

*(Rilasciato il 1° febbraio 2022)*

**Corretto:**

* [Modelli di Substance] In alcuni casi gli intervalli possono andare persi
* [Modelli di Substance]&#x200B;[Esporta] La scala varia a seconda del tipo di file
* [Modelli di Substance]&#x200B;[Esporta] Le trame sono duplicate

### 11.3.2

*(Rilasciato il 25 gennaio 2022)*

**Aggiunto:**

* [Documentation] Aggiornamento della sezione &#39;Iray&#39;

**Corretto:**

* [Modelli di Substance] Impossibile pubblicare il pacchetto che contiene grafici di modelli di Substance
* [Substance modelli] Impossibile esportare un grafico modello in alcuni casi specifici
* [Modelli Substance] Rendete più coerenti gli intervalli dei parametri
* [MDL] Arresto anomalo durante l&#39;esportazione del file MDLE
* [MDL] File mdl errato generato quando un grafico MDL contiene nodi punto connessi a parametri esposti
* [Vista 2D] Ottimizzare la visualizzazione degli strumenti di pittura
* [Content] Impostazione incoerente dei parametri relativi alle dimensioni dell&#39;output nei grafici di origine del modello
* [Proprietà] Le etichette degli intervalli soft/hard sono errate nel pannello Proprietà per i nodi esposti dei modelli MDL e Substance
* [Modelli] Aggiorna i valori predefiniti degli input nel modello &quot;Filtro Sampler&quot;

### 11.3.1

*(Rilasciato il 13 dicembre 2021)*

**Aggiunto:**

* [Grafico] Aggiungi un avviso quando si elimina un grafico utilizzato in un altro grafico/pacchetto

**Corretto:**

* [UI] L’editor colore è troppo piccolo quando si utilizza un layout dell’interfaccia utente specifico
* [UI] Arresto anomalo durante l’aggiornamento dell’elenco degli ultimi modelli utilizzati
* [UI] Evidenziazione errata nelle preferenze Scelte rapide
* [UI] La dimensione della finestra principale è troppo piccola dopo il riavvio di una sessione con finestre (solo macOS)
* [UI] Il dock ingrandito non viene ridotto a icona all’uscita (solo Windows)
* [UI] Lo spazio mancante nella descrizione del parametro &#39;Level Out High&#39; [3DView] Axis nella vista 3D è troppo piccolo quando il rettangolo di selezione della scena è sottile
* [UI] Problema di stile su parte del testo nelle impostazioni del progetto per la lingua francese
* [Modelli di Substance] Il blocco sui parametri esposti non viene salvato tra le sessioni
* [Substance modelli] Il modificatore Maiusc è ancora abilitato dopo l&#39;utilizzo della scelta rapida anteprima nodo
* [Substance modelli] Alcuni nodi eliminati rimangono nel modulo SBSM esportato
* [Modelli di Substance] I nodi di destinazione della valutazione si accumulano e non vengono eliminati.[API] Arresto anomalo durante il rendering del nodo Curva, proprietà impostate tramite API
* [Panettieri] Il widget &quot;Colore materiale&quot; non è visibile e non funziona come previsto
* [Content] Nodo di PBR render: calcolo interno non eseguito alla risoluzione del nodo
* [Grafico a funzioni] In alcuni casi i messaggi che visualizzano i tipi previsti sono errati
* [Grafico] Input relativo all&#39;input: i parametri ereditati non sono corretti con le istanze connesse
* [MDL] Le istanze dei grafici a Substance non vengono aggiornate in modo affidabile nei grafici MDL
* [Publish] Grafico di pubblicazione non riuscita che contiene dipendenze circolari
* [Scelte rapide] Maiusc+Spazio non deve essere una scelta rapida da tastiera assegnabile per i nodi
* [Modelli] Formato di output dei modelli personalizzati ignorato

### 11.3.0

*(Rilasciato il 24 novembre 2021)*

**Aggiunto:**

* [Modelli Substance] Aggiungere descrizioni comandi per i parametri dei nodi
* [Modelli Substance] Consente di visualizzare in sovrapposizione nella finestra della vista 3D il risultato di un nodo intermedio
* [Modelli di Substance] Migliorare la visualizzazione della visualizzazione della base
* [Modelli Substance] Mantiene la gerarchia degli oggetti durante l&#39;esportazione di un grafico Modello Substance in .fbx
* [Modelli Substance] Supporto di più materiali nell&#39;esportazione FBX/OBJ dal grafico dei modelli Substance
* [Modelli Substance]&#x200B;[Contenuto] Nodo particelle
* [Modelli di Substance]&#x200B;[Contenuto] Nodo Trasformazione generativa
* [Modelli Substance]&#x200B;[Contenuto] Nodo Pattern organico
* [Modelli Substance]&#x200B;[Contenuto] Particelle dal nodo Istanze
* [Modelli di Substance]&#x200B;[Contenuto] Nodo di potatura delle particelle
* [Modelli Substance]&#x200B;[Contenuto] Nodo tornio
* [Modelli di Substance]&#x200B;[Contenuto] Nodo shell
* [Modelli Substance]&#x200B;[Contenuto] Nodo di proiezione
* [Modelli Substance]&#x200B;[Contenuto] Nodo di rifilo curva
* [Modelli Substance]&#x200B;[Contenuto] Aggiorna nodo Sampler curva
* [Modelli Substance]&#x200B;[Contenuto] Aggiornamento del nodo Sampler mesh
* [Modelli di Substance]&#x200B;[Contenuto] Aggiorna nodo variazione
* Pulsante [UX] per ingrandire la visualizzazione corrente
* [UX] Aggiornare la finestra Nuovo grafico
* [UX] Aggiungi l&#39;opzione &quot;Scarica lettore&quot; nel menu Strumenti e aggrega con &quot;Trova lettore&quot;
* [UX] Aggiungi la voce &quot;Chiudi tutto&quot; al menu del file
* [UX] Applicare maiuscole/minuscole uniformi in tutto il menu principale
* [UX] Visualizza automaticamente le proprietà degli elementi del grafico duplicati
* [UX] Aggiungi pulsanti nella barra degli strumenti del grafico per disabilitare le dimensioni costanti dello schermo per i titoli dei fotogrammi / Commenti / Pins
* [UX] Pulsanti per copiare le informazioni sulle versioni negli Appunti della finestra di dialogo Informazioni su
* Input [Materiali] relativi agli input
* [Content] Aggiungi l&#39;opzione &#39;Tiling&#39; ai rumori di Perlin 3D
* [Content] Nuovo nodo del processo di diffusione
* [Content] Nuova versione del nodo di PBR render
* [Interoperabilità] Ricezione di SBS e SBSAR da Sampler
* [Interoperabilità] Invia SBSM a Stager
* [Vista 3D] Aggiungi un&#39;opzione per disabilitare l&#39;eliminazione del backface
* [Vista 3D] Aggiungere un&#39;opzione per visualizzare lo spazio tangente vertice
* [Esplora] Evidenzia il grafico in Esplora risorse quando si fa doppio clic sullo sfondo della visualizzazione Grafico
* [Esplora] Rimuovi l’opzione &quot;Esplora&quot; dai menu contestuali
* [Panettieri] Nascondi panettieri obsoleti
* [Gestione colore] Aggiungi il supporto per le regole del file di configurazione OCIO v2
* [Libreria] Rinomina le categorie in base ai tipi di grafico
* [Preferenze] Disattiva automaticamente la CPU nelle preferenze hardware di Iray se viene rilevata una GPU CUDA supportata

**Corretto:**

* [Substance modelli] Arresto anomalo di Mac quando si utilizza l’opzione &quot;as sudb&quot; su .fbx
* [Substance modelli] Arresto anomalo durante l&#39;esportazione in SBSM in un caso specifico
* [Modelli di Substance] Errore di esportazione durante l&#39;esportazione di parametri esposti che non sono mai stati creati
* [Modelli di Substance] Arresto anomalo casuale quando si apre un grafico che fa riferimento a più file .fbx
* [Modelli di Substance] Gli intervalli non vengono applicati dinamicamente nei widget dei parametri esposti
* [Modelli Substance] L&#39;opzione Ricarica trama non funziona sul grafico dei modelli di Substance
* [Substance modelli] Le scene non vengono visualizzate in una vista 3D disponibile in un caso specifico
* [UI] L’area di disattivazione è troppo grande nelle opzioni del materiale
* [UI] Problema di stile nella finestra di dialogo &quot;File pacchetto non salvato&quot;
* [UI] Il tasto Tab deve essere premuto due volte per spostarsi tra i valori
* [UI] Lo zoom con il trascinamento del mouse è invertito tra Vista 3D e altre Finestre
* [UI] Il caricamento di un SBS già aperto utilizzando l’elenco &quot;File recenti&quot; attiva in modo errato un messaggio &quot;Pacchetto non trovato&quot;
* [UI]&#x200B;[macOS] Layout di interfaccia predefinito non corretto dopo l&#39;avvio dell&#39;applicazione
* [UI] Impossibile salvare i pacchetti nella directory principale di un&#39;unità (solo Windows)
* [Grafico] L&#39;opzione &quot;Visualizza automaticamente nella vista 2D&quot; non è coerente in un caso specifico
* [Graph] L&#39;opzione &#39;Apri riferimento&#39; è disponibile per i nodi dell&#39;istanza SBSAR
* [Grafico] Le proprietà del pin vengono visualizzate solo quando viene creato un elemento
* [Grafico] Le regole delle stringhe pin vengono applicate in modo incoerente
* [Grafico] Arresto anomalo durante il salvataggio di un grafico vuoto
* [Vista 3D] L&#39;angolo di Anisotropia viene invertito nello shader ASM
* [Vista 3D] ASM Shader: problemi di linearizzazione con le mappe relative a SSS
* [Vista 3D] Rendering OpenGL interrotto dopo la chiusura di viste 3D aggiuntive in un caso specifico
* [Vista 3D] Le posizioni predefinite delle fotocamere non sono corrette nella vista 3D con alcuni file .fbx
* [MDL] &quot;Aggiungi nodo&quot; dal menu di scelta rapida non funziona per i grafici MDL
* [MDL] Bug: la connessione del nodo non riesce quando si utilizzano componenti float2.x e simili (SD 11.1.2)
* [MDL] Arresto anomalo all’apertura di un file .sbs specifico
* [MDL] Unità scena per metro nell&#39;Iray non impostate all&#39;avvio della sessione di rendering
* [MDL] Si blocca quando si modifica un nodo lerp nel grafico MDL
* [MDL] Ordine dei parametri nel codice MDL esportato
* [Esplora risorse] dopo l&#39;annullamento della creazione della risorsa viene creata una cartella risorse vuota
* [Explorer] Solo il primo elemento di un pacchetto può essere spostato nella parte inferiore dell&#39;elenco
* [Content] RT Bent Normal e RT AO attivano il calcolo dei nodi nei grafici nidificati
* [Nodo di input] La bitmap nei nodi di input non viene aggiornata quando si modifica UDIM
* [Iray] Si impiega molto tempo quando si tenta di visualizzare una scena di modelli di Substance con molte istanze
* [Preferenze] Riga vuota quando si annulla l’aggiunta di un file di progetto
* [Editor Python] L’opzione &quot;Chiudi&quot; rimane abilitata dopo la chiusura dell’ultimo script e include ancora il nome æ

### 11.2.2

*(Rilasciato il 28 settembre 2021)*

**Aggiunto:**

* [Proprietà] Aggiungi nuovi tipi di grafici per decalcomanie, atlanti, luci ambiente e trame di luce

**Corretto:**

* [UI] Layout dell’interfaccia non corretto dopo l’avvio dell’applicazione
* [Stabilità] Correzione degli arresti anomali quando si esce dalla modalità di sospensione su Windows e quando si collegano/scollegano le schermate
* [Vista 3D] La creazione di una risorsa Scena 3D da Substance grafica modello Scena non ha alcun effetto
* [Fusione] I valori enum non sono presenti quando si espone il metodo di fusione
* [Esporta] L’esportazione di scene di modelli di Substance genera una geometria duplicata
* [MDL] Arresto anomalo all&#39;apertura di un file SBS specifico
* [Trama] Arresto anomalo quando si collega una trama specifica con geometria difettosa
* [Modelli Substance] L’esportazione non riesce quando il valore predefinito del parametro esposto non è compreso nell’intervallo consentito

### 11.2.1

*(Rilasciato il 27 luglio 2021)*

**Aggiunto:**

* [Modello di Substance] Aggiornamento alla versione 1.0.3
* [Modello Substance] Completare e migliorare la documentazione dei grafici del modello di Substance
* [Substance modello] Visualizza i registri nella console
* [Modello Substance]&#x200B;[ScatterOnCurves] Modifica il valore predefinito per la spaziatura
* [Modello Substance]&#x200B;[ScatterOnCurves] Rimozione del parametro HalfSpaceOddEven non necessario
* [Modello Substance]&#x200B;[Trasforma] Aggiorna intervallo morbido rotazione Eulero
* [Publish] Memorizzare le impostazioni nella finestra di Publish
* [Publish] Avvisa l&#39;utente quando almeno una dipendenza presenta modifiche non salvate
* [Publish] Inizializzare il campo &quot;Percorso file&quot;
* [Publish] Aggiungi feedback visivo durante la pubblicazione
* [Interoperabilità] Aggiungere il comando &quot;Invia a lettore&quot; al menu &quot;Invia a&quot;
* [Interoperabilità] Semplificare il flusso di lavoro di invio/invio a Sampler e Painter
* [API] Aggiungi SDApplication.getVersion() per consentire il recupero della versione dell&#39;applicazione host
* [Esplora risorse] Aggiungere un&#39;azione Apri agli elementi del grafico del modello di Substance
* [Grafico] Disattiva le azioni &quot;Visualizza nella vista 3D&quot; per i nodi delle istanze fantasma

**Corretto:**

* [Substance modello] Arresto anomalo durante l’eliminazione di una sequenza
* [Modello Substance] Le basi non vengono disegnate correttamente in alcuni casi
* [Modello di Substance] Impossibile esportare progetti specifici
* [Modello Substance] Assegnazione del materiale interrotta all&#39;apertura di un progetto con Iray abilitato
* [Modello Substance] L&#39;intervallo rigido minimo non funziona correttamente in determinate circostanze
* [Modello Substance]&#x200B;[Primitivo] Il primo livello di suddivisione dell&#39;icosfera non funziona
* [Modello Substance]&#x200B;[RandomFloat] Gestisce correttamente il caso in cui Min >= Max
* [Vista 3D] Arresto anomalo durante il trascinamento delle mappe
* [Vista 3D] Le stringhe esposte nei materiali MDL utilizzano il widget dello spazio colore
* [Vista 3D]&#x200B;[Pannelli] Gli oggetti principali non vengono gestiti correttamente
* [Vista 3D] Messaggio di avvertenza sul nome di utilizzo &quot;heightScale&quot; per il file .glslfx legacy
* [Content] Avvisi di cottura nel nodo Height Extrude
* [Content] Il nodo Irradianza RT non viene visualizzato nella libreria
* [Content] Ombre RT: messaggi di avvertenza di cottura nella console
* [Grafico] Arresto anomalo quando si apre un file con alcuni nodi disattivati
* [Grafico] Il nodo del punto non funziona correttamente in Grafico MDL quando viene selezionato un collegamento
* [Grafico] La vista del grafico non viene riaperta automaticamente dopo aver ricaricato un pacchetto
* [Interoperabilità] Errore durante la selezione di &quot;Scarica...&quot; durante l&#39;invio al lettore
* [Interoperabilità] Il nuovo invio dopo l’eliminazione di tutti gli output genera errori API
* [Interoperabilità] Il nuovo invio subito dopo la chiusura dell’applicazione di destinazione genera errori API
* [Esplora] [Grafico] Dopo aver ricaricato un pacchetto, il primo grafico aperto non è il primo grafico del pacchetto
* [Esplora risorse] I nuovi grafici in un pacchetto non vengono inseriti nello stesso modo a seconda del tipo
* [Esplora risorse] Impossibile aprire un grafico modello di Substance o una risorsa scena dopo averlo spostato nell&#39;elenco delle risorse
* [Explorer] Arresto anomalo/blocco durante lo spostamento di un grafico del modello di Substance nella gerarchia del pacchetto
* [Library] I file SBSAR rimangono nel percorso dei file temporanei
* [Library] I file XML rimangono nel percorso dei file temporanei
* [Player] Il materiale non ha alcun impatto nella vista 3D quando la lingua è impostata sul giapponese
* [Player] Il collegamento per il download della versione di Substance Player è obsoleto
* [Widget colore] La finestra dell’editor colori si sposta nella parte superiore dello schermo
* [IRay] Correggere il caricamento del modulo IRay su Windows quando la directory dell&#39;app contiene caratteri non ASCII
* [Preferenze] Il pannello MDL viene visualizzato due volte in Project
* [API] I nodi FxMap non supportano getPropertyGraph()

### 11.2.0

*(Rilasciato il 23 giugno 2021)*

**Aggiunto:**

* Il Substance Designer [Branding] diventa Adobe Substance 3D Designer
* [Modelli di Substance] Nuovi grafici per modelli di Substance per creare modelli 3D procedurali
* [Content] Aggiungi nuove mappe ambiente HDR
* [Content] Nuovo nodo normale piegato
* [Content] Nuovo nodo di Occlusione ambiente RT
* [Contenuto] Nuovo nodo Riflessioni personalizzate
* [Contenuto] Nuovo nodo Riflessioni personalizzate
* [Content] Nuovo nodo Irradianza RT
* [Content] Nuovo nodo Ombre RT
* [Interoperabilità] Invia la risorsa a Painter, avvierà Painter e aggiungerà o aggiornerà la tua risorsa nella libreria (richiede un piano Substance 3D per Adobe)
* [Interoperabilità] Invia la risorsa a Sampler, avvierà Sampler e aggiungerà o aggiornerà la tua risorsa nella libreria (richiede un piano Substance 3D per Adobe)
* [Interoperabilità] Sfoglia la tua risorsa in Adobe Bridge, avvierà Bridge nel percorso della risorsa (richiede un piano Substance 3D di Adobe)
* [ASM] Supporto del nuovo Adobe Standard Material (ASM) nel grafico Grafici Substance e MDL
* [ASM] Aggiunta di maschere ASM
* [ASM] Aggiunta dello shader OpenGL per ASM
* [ASM] Impostate lo shader ASM come shader predefinito
* [Generale] Aggrega tutti i file temporanei nella directory temporanea impostata dall&#39;utente
* [Generale] Nuovo comando &quot;Salva una copia con nome&quot;
* [Generale] Menu Aggiorna file
* [Generale] Aggiorna menu?
* [Publish] Nuova finestra di pubblicazione
* [Publish] Aggiungi l&#39;opzione nelle preferenze per non salvare il file SBS durante la pubblicazione di un file SBSAR
* [Proprietà] Aggiungi il campo del tipo di grafico alle proprietà del grafico
* [Proprietà] Riordina le proprietà dei grafici in modo più pertinente
* [Branding] Nuova finestra Informazioni su
* [Branding] Aggiorna stile applicazione
* [GLSLFX] Aggiungere un&#39;etichetta alle tecniche
* [GLSLFX] Aggiungi la possibilità di impostare l’etichetta di uno shader GLSLFX
* [Metadati] Aggiungere metadati nelle risorse del pacchetto
* [Metadati] Consenti edizione metadati per grafici, input, output e risorse
* [Localizzazione] Nuove traduzioni in tedesco, francese e cinese semplificato
* [UX] Inverti zoom nella vista 3D in caso di trascinamento del mouse
* [AXF] Aggiornamento alla versione 1.8.0
* [Registri] Aggiungi i plug-in installati ai registri
* [VFX] Aggiungere la configurazione OpenColorIO ACES 1.2
* [API Python] Aggiungi un metodo per eseguire una query sulla directory tmp specificata nelle impostazioni
* [API Python] Aggiungi un metodo isModified a SDPackage per verificare se un pacchetto è stato salvato
* [API Python] Aggiungi alcuni metodi di conversione del colore a SDColorManagementEngine
* [API Python] Elimina gli oggetti del grafico (Commenti, perni, fotogrammi, ecc.)
* [API Python] Esposizione della proprietà della Dimensioni fisiche per i nodi dell&#39;istanza del grafico
* [API Python] Esponi Salva una copia con nome
* [API Python] Correggere il metodo SDPackageMgr.savePackage
* [API Python] Ottieni un elenco di oggetti grafici selezionati
* [API Python] Introduzione di nuovi nomi di metodi per l’utilizzo delle selezioni dei grafici
* [API Python] I plug-in non possono aggiungere azioni al primo pannello di navigazione creato

**Corretto:**

* [Parametri] I valori negativi nei parametri Integer1 a discesa determinano un comportamento incongruente nell&#39;istanza
* [Parametri] Problema durante l’incremento di un valore su un widget angolo
* [Grafico] Problemi di tempo quando l&#39;output viene visualizzato nella vista 2D o 3D.
* [Internazionalizzazione] Alcuni caratteri specifici vengono trasformati in spazi negli identificatori di file
* [Preferenze] L’etichetta del file &quot;Progetto utente&quot; non viene riconvertita dal giapponese
* [API Python] RecursionError durante l&#39;esecuzione del metodo SDUIMgr.getCurrentGraphSelectedNodes()
* [API Python] SDApplication.getPath(SDApplicationPath.InstallationDir) non restituisce nulla
* [API Python] SDSBSARExporter non invia notifiche di salvataggio dei file

### 11.1.2 (2021.1.2)

*(Rilasciato il 17 marzo 2021)*

**Corretto:**

* [Libreria] Le miniature non vengono aggiornate in modo uniforme
* [Content] La proprietà &#39;Proporzioni pixel&#39; dei grafici &#39;Vector morph&#39; è impostata su &#39;Estendi (assoluto)&#39;
* [Contenuto] Le bitmap utilizzate negli strumenti di pittura vengono visualizzate nel menu Nodo
* [Contenuto] Output NaN per l&#39;input di colore piatto nel nodo Livelli automatici con precisione a virgola mobile
* [Engine]&#x200B;[SSE2] Il valore &#39;Level in mid&#39; diverso da 0,5 genera un output 1,0
* [Miniatura] Le mappe di input vengono ridotte a 256
* [UI] Le descrizioni dei nodi atomici contengono un&#39;interruzione di riga errata

### 11.1.1 (2021.1.1)

*(Rilasciato il 10 febbraio 2021)*

**Corretto:**

* [Vista 3D] Problema di rendering quando si utilizza sbs che hanno alte frequenze nella mappa normale
* [Vista 3D] Le immagini non vengono applicate se la proprietà di output &quot;Component&quot; non è impostata su RGBA o RGB
* [Vista 3D] Le scene non vengono caricate correttamente in alcune situazioni specifiche
* [UI] Il campo di input &quot;File di texture&quot; nell&#39;editor pennelli viene ridimensionato in verticale
* [UI] I pulsanti Blocca e Blocca scompaiono dalla scheda quando la scheda attiva è chiusa
* [Panettieri] Risultato errato quando il riquadro globale delle trame di poli superiori non include l’origine della scena
* [Gestione colore] La proprietà del materiale Texture colore di base sRGB non viene sostituita nello stato Scena personalizzato
* [Console] Il messaggio di registro &quot;GPU disponibili&quot; non elenca le GPU e viene visualizzato in modo casuale
* [Console] Stringa non corretta registrata durante l’utilizzo dell’esportazione in batch
* Il parametro &quot;Input normal format&quot; di [Content] Atlas splitter influisce sul canale rosso anziché sul verde
* [Cooker] Arresto anomalo o output NaN quando si utilizza \*.surface bitmap in SBSAR
* [Engine] I valori di output non compresi nell’intervallo consentito per la mappa sfumatura si aggirano intorno a 0 quando il formato di output ha un intervallo compreso tra 0 e 1
* [Parametri] I cursori Min/Max/Predefinito non si adattano automaticamente nella finestra dei parametri Esposizione
* [SBSAR] Arresto anomalo durante l’importazione di alcuni file SBSAR
* [SVG] Arresto anomalo quando si annulla l’importazione di risorse

### 11.1.0 (2021.1.0)

*(Rilasciato il 28 gennaio 2021)*

**Aggiunto:**

* [Tinte piatte] Supporto dei colori Pantone in Designer
* [Grafico] Disattivare i nodi
* [Vista 3D] Esportare trame tassellate dal riquadro di visualizzazione
* [Internationalization] Aggiorna la versione giapponese
* [Vista 3D] Ottimizzare il consumo di memoria quando non si utilizza Iray
* [API Python] Aggiungere il metodo SDResource.delete() per eliminare un SDResource
* [API Python] Aggiungi il supporto per le tinte piatte all’API Python
* [API Python] Nuova richiamata da attivare alla chiusura di un pacchetto
* [Vista 2D] Convertire il database dei pennelli dal formato SQLite al formato Json
* [Vista 2D] Miglioramento delle prestazioni di rendering e dell&#39;affidabilità (calcolo CPU)
* [Library] Aggiungi l’opzione &quot;Escludi pattern&quot; nelle impostazioni del progetto
* [Library] Rinomina &quot;Escludi pattern&quot; in Escludi estensioni file&quot; nelle impostazioni del progetto
* [UX] Rimuovi il pulsante &quot;?&quot; nelle barre del titolo della finestra in Windows
* [UX] Sposta la scelta rapida Ctrl+E su &quot;Apri riferimento&quot; quando la modifica nel contesto è disattivata
* [Panettieri] Elimina la cache di anteprima quando si elimina un panettiere nell’elenco dei panettieri
* [Prestazioni] Miglioramento del budget della cache delle immagini su hardware con GPU con memoria condivisa
* [Preferenze] Adattare il valore &quot;Limite cache GPU&quot; al pool di memoria disponibile
* [Properties] Visualizza attributo Dimensioni fisiche nell&#39;istanza del nodo
* [Scripting] Contrassegna il sistema di scripting esterno come obsoleto
* [Condividi] Rimuovi le funzioni &quot;Esporta in Substance share&quot;

**Corretto:**

* [Contenuto] Ordine di I/O incoerente nei nodi Materiale
* [Content] L&#39;input primario sui nodi di alterazione non è coerente
* [Contenuto] Risolvi gli avvisi del Cooker dal nodo Sfocatura radiale
* [Esportazione] L’esportazione in batch con il motore CPU utilizza la VRAM per determinare il budget della memoria
* [Export] Se si esporta in un percorso non esistente, le cartelle verranno create
* [Esporta] Il budget di memoria è troppo basso quando si utilizza l’esportazione in batch
* [Vista 2D] Artefatti/bande durante la copia di immagini HDR negli Appunti
* [Vista 2D] L&#39;esportazione di immagini dalle risorse esporta sempre 8 bit
* [Vista 3D] Iray: la modifica del valore normale con l&#39;editor fornisce un risultato strano
* [Vista 3D] Iray: la disattivazione del canale normale non produce il risultato giusto
* [Library] Il filtro in base all’URL non funziona correttamente
* [Library] Le risorse corrispondenti a un pattern escluso dalla libreria non possono essere importate manualmente
* [Panettieri] La ridenominazione di un panettiere non influisce sulla sua voce nell’elenco di anteprima della vista 2D
* [Esplora] Perdita di sincronizzazione tra Esplora risorse e dati del grafico
* [Grafico a funzioni] Arresto anomalo durante l’impostazione del nodo a funzioni con tipo di output non corrispondente come output
* [MDL] I nodi dell&#39;istanza SBS non hanno anteprima, generano 0 e non attivano il calcolo del grafico
* [API Python] Impossibile modificare la proprietà &#39;editor&#39; del parametro di input
* [Python] Il ripristino del layout non reimposta correttamente i dock creati da Python
* [Resources] Impossibile collegare/importare un documento PSD a 32 bit

## Versione 10

### 10.2.2 (2020.2.2)

*(Rilasciato il 17 dicembre 2020)*

**Aggiunto:**

* [Vista 3D] Ripristinare la posizione della videocamera memorizzata in una risorsa Scena
* [Grafico] Rimuovi &quot;nodi di input&quot; nel menu di scelta rapida per FXMap e value processor

**Corretto:**

* [Contenuto] Ordine di I/O incoerente nei nodi Materiale
* [Contenuto] PBR render: campionamento IBL errato per il contributo dello specular
* [Content] PBR render: alcuni pixel sono sempre trasparenti
* [Content] PBR render: output UV non corretto per la forma Cilindro
* [Content] Il parametro &#39;Pattern Specific&#39; di Splatter Circular non ha effetto
* [MDL] Arresto anomalo durante la creazione e la connessione di un nodo
* [MDL] Arresto anomalo durante la duplicazione di un costruttore di array color[] con il relativo input di valore esposto connesso
* [MDL] Arresto anomalo durante la riconnessione di una connessione non valida
* [MDL] Gli MDL esportati hanno parametri duplicati
* [MDL] I parametri esposti non vengono esportati in un file mdl
* [Parametri] Un parametro nodo può essere definito due volte nel SBS in un caso specifico
* [Parametri] Arresto anomalo durante il recupero del tipo di output del grafico della funzione di un parametro
* [Parametri] Arresto anomalo quando si seleziona l’opzione &quot;Modifica input grafico esposto&quot; in assenza di input corrispondente
* [Vista 3D] L’utilizzo dell’ambiente non viene considerato correttamente dal modulo di rendering OpenGL
* [3D View] IOR è 0 e deve essere reimpostato in un caso specifico
* [Vista 3D] Gli UV del piano/piano ad alta risoluzione sono sfalsati
* [Bitmap] Arresto anomalo quando si annulla l&#39;importazione di risorse
* [Bitmap] Arresto anomalo durante la creazione di un nuovo nodo Bitmap con un tipo di file non supportato
* [Dipendenze] Arresto anomalo quando si annulla &quot;Riposiziona&quot; per risolvere un’istanza fantasma
* [Grafico a funzioni] Arresto anomalo all’apertura del grafico a funzioni per un parametro
* [Editore sfumatura] Lo spostamento di cursori e tasti registra troppe azioni nella pila della cronologia
* [License] Arresto anomalo durante l&#39;analisi di un file license.key non valido
* [SBSAR] Impossibile creare nodi di istanza SBSAR dalla libreria se i grafici esposti si trovano nelle cartelle

### 10.2.1 (2020.2.1)

*(Rilasciato il 4 novembre 2020)*

**Corretto:**

* [Generale] Arresto anomalo quando si esce dalla modalità di sospensione di Windows
* [Generale] Arresto anomalo all’annullamento dopo il caricamento di una risorsa Scena 3D
* [Engine] Le linee degli artefatti vengono visualizzate nell&#39;output del nodo Distanza su Direct3D
* [Engine] Arresto anomalo quando si seleziona il nodo Mappa sfumatura in un grafico aggiornato
* [Engine] Nessun avviso quando si immette un valore predefinito diverso da 0 in modalità di compatibilità Engine v7
* [Vista 3D] &quot;Rimuovi tutto&quot; lascia trame con materiali predefiniti senza alcun materiale applicato
* [Vista 3D] L’opzione &quot;Ripristina scena&quot; rimuove tutte le texture dalla trama nell’immagine
* [Vista 3D] OpenGL: la modifica del valore predefinito di un campionatore in un file .glslfx non si riflette correttamente nell&#39;interfaccia utente
* [Vista 3D] Pixel rossi e neri sul bordo più a destra delle immagini renderizzate OpenGL
* [Dipendenze] Impossibile riposizionare le dipendenze mancanti di tipo &#39;Altro&#39;
* [Dipendenze] Arresto anomalo all’uscita quando il Visualizzatore dipendenze è aperto
* [Grafico] Arresto anomalo durante la duplicazione di un nodo di istanza Ghost
* [Grafico] La modifica in contesto è disponibile tramite la sequenza di tasti quando è disattivata in Preferenze
* [UI] Il titolo della finestra di avviso &quot;Individua lettore&quot; non è corretto
* [UI] L&#39;attivazione guidata ha un comportamento errato
* [Explorer] I pacchetti raggruppati sono sempre modificabili in Windows
* [MDL] Arresto anomalo durante il caricamento del grafico da una versione precedente con connessioni ora non valide
* [Proprietà] Il colore predefinito del nodo di input non viene aggiornato quando si annulla
* [SBSRender] I profili ICC delle bitmap iniettate non vengono utilizzati

### 10.2.0 (2020.2.0)

*(Rilasciato il 12 ottobre 2020)*

**Aggiunto:**

* [Content] Aggiungi nodo &quot;Cross Section&quot;
* [Content] Aggiungere la funzione &quot;Cross product vec2&quot; alle funzioni.sbs
* [Content] Aggiungi nodo valore &quot;Get Size&quot;
* [Contenuto] Aggiungere la funzione &quot;Orthogonal vec2&quot; alle funzioni.sbs
* [Content] Aggiungi funzioni Average a functions.sbs
* [Content] Aggiungi filtro Soglia
* [Content] Corrispondenza colori: aggiungete un input maschera per specificare dove applicare il filtro
* [Content] Tile Generator/Sampler: aggiungete nuove opzioni per controllare le dimensioni del pattern
* [Content] Aggiorna il nodo del PBR render con il valore predefinito per gli input dell&#39;immagine
* [Parametri] Aggiungere icone di avvertenza per evidenziare i problemi in Parametri istanza
* [Parametri] Ignora istruzioni If visibili per Input/Output che coinvolgono parametri a cui è applicata una funzione
* [Parametri] Miglioramento dell&#39;esperienza utente per l&#39;associazione dei gruppi
* [Parametri] Rielaborazione del modo in cui esporre un singolo parametro
* [Parametri] Evidenzia parametri esposti
* [Parametri] Miglioramento della pulizia dei parametri non utilizzati
* [Engine] Nodo di curva: nuova opzione per generare la texture della curva
* [Engine] Valori predefiniti sulle immagini di input
* [Engine] Nodo Distanza: nuove modalità di distanza (distanze Manhattan e Chebyshev)
* [Engine] Nodo sfumatura: nuova modalità di interpolazione per un mix più naturale tra i colori
* [UX] Alcuni parametri sono ora disattivati a seconda di altri parametri
* [UX] Accettare colori RGB a 6 cifre nel campo esadecimale del Selettore colore
* [UX] Evita di visualizzare le proprietà dei commenti non appena vengono selezionati
* [UX] Visualizzare i gruppi rilevanti quando si inizia a scrivere un nome di gruppo
* [UX] Scelta rapida per riesportare gli output del grafico
* [UX] Rendi tutte le caselle combinate Dropdown-textfield diverse dalle caselle combinate normali
* [GraphRender] Visualizza le miniature dei nodi uno alla volta e non solo quando vengono calcolate tutte
* [GraphRender] Migliora il ritardo di annullamento durante il rendering del grafico
* [GraphRender] Migliora la precisione della barra di avanzamento del rendering
* [Miniature] Calcolo automatico delle miniature (icona)
* [Miniature] Rielaborazione dell&#39;esperienza utente per aggiungere una miniatura (icona) a un pacchetto
* [Preferenze] Abilita Raytracing GPU per impostazione predefinita per i nuovi utenti
* [Preferenze] 3DView/OpenGL/Qualità: sostituisci il cursore per il conteggio dei campioni con un elenco di opzioni più intuitivo
* [Panettieri] Migliorare le prestazioni post-elaborazione
* [Gestione colore] Mostra lo spazio colore di lavoro corrente nella finestra di dialogo delle preferenze.
* [Iray] Passa automaticamente alla modalità CPU quando non è disponibile una GPU compatibile
* [Prestazioni] Migliorare il tempo di risposta per calcolare il nodo di interesse (ora calcolato per primo)
* [API Python] Nuovo metodo addActionToExplorerToolbar per aggiungere icone alla barra degli strumenti di Esplora risorse
* [Resources] Aggiornamento a FBX 2020.0.1
* [iRay] Aggiornamento a Iray 2020.1.0
* [API] Aggiungi l’accesso Python alle impostazioni e alle proprietà della gestione colore

**Corretto:**

* [Grafico] La modifica delle dimensioni della pagina principale o del riquadro uv non annulla il rendering corrente
* [Grafico] Arresto anomalo quando si sposta una connessione di output e si preme Alt+LMB
* [Grafico] Arresto anomalo durante lo spostamento delle connessioni in modalità Materiale o Materiale compatto
* [Grafico] I nodi di input non possono visualizzare in anteprima le risorse bitmap
* [Grafico] Compatibilità del nodo interrotta sulle istanze
* [Grafico] Troppi nodi sono invalidati quando si modifica un parametro del grafico
* [Contenuto] La forma di output &quot;Estrusione forma&quot; viene capovolta in casi specifici: è necessaria una nuova versione, quella precedente è deprecata
* [Contenuto] Risultato errato con Variazione colore personalizzata nel nodo Corrispondenza colore
* [Content] Il rapporto tra dimensioni X/Y in Atlas scatter ha l&#39;effetto opposto
* [Content] Il rapporto tra dimensioni X/Y nello splatter di forma ha l&#39;effetto opposto
* [Vista 3D] Arresto anomalo durante l’operazione Annulla dopo il caricamento di una risorsa Scena da un pacchetto
* [Vista 3D] Ambiente personalizzato non salvato in SBSSCN se il percorso contiene alias con caratteri speciali
* [Vista 3D] Il passaggio dal formato normale alle impostazioni del materiale genera stati capovolti
* [UI] Il testo del pulsante &quot;Imposta come principale&quot; è in eccesso dall’area di visualizzazione
* [UI] La posizione della finestra principale non viene ripristinata correttamente quando si lavora in modalità finestra
* [UI] Il testo della barra di stato viene scostato quando la finestra è a schermo intero o trascinata vicino al bordo dello schermo
* [Iray] Arresto anomalo con messaggio &quot;Tag non valido&quot; quando si passa da un modulo di rendering all’altro
* [Iray] Facce visibili su superfici non opache
* [Predefiniti] Arresto anomalo quando si applicano predefiniti in istanze di alcuni grafici a Substance Source
* [Predefiniti] nome errato visualizzato dopo l&#39;annullamento sull&#39;istanza sbs
* [Rendering] Rendering errato durante l’ottimizzazione di un parametro in modalità di anteprima
* [Panettieri] L&#39;aggiornamento di più mappe con baking genera avvisi che bloccano alcuni dolci
* [Cooker] La modifica dei nodi SBSAR nelle istanze SBS genera un output pari a 0 dall&#39;istanza
* [Explorer] Gli alias personalizzati non vengono passati quando si utilizza &#39;Salva e apri in Substance Player&#39;
* [Editore sfumatura] La selezione assoluta del colore non influisce su tutti i tasti selezionati

### 10.1.3 (2020.1.3)

*(Rilasciato l&#39;11 giugno 2020)*

**Aggiunto:**

* [Content] Esponi il parametro &#39;Colore mascherino&#39; nel nodo Trasformazione sicura in scala di grigi
* [Content] PBR render: aggiungi un’opzione di input in background personalizzata
* [Contenuto] Nodi luce panorama: nuova opzione per campionare il colore dall&#39;immagine di sfondo
* [Parametri] Nascondere i parametri con il flag &#39;not-supported&#39; dall&#39;elenco della finestra Parametri di esposizione

**Corretto:**

* [Vista 3D] Arresto anomalo durante il cambio di trame personalizzate in un caso specifico
* [Vista 3D] Il formato normale è sempre all’avvio di DirectX
* [Content] Disturbo di Worley 3D: rendering artefatto quando si utilizza un valore elevato per le dimensioni della griglia
* [Content] La fusione del nodo Dissolve non è corretta
* [Contenuto] PBR render: rimuovi avviso cucina
* [Content] PBR render: il risultato contiene colori negativi in alcuni casi
* [Cooker] Problema di inserimento nella cache per nodi di istanze con più output
* [Explorer] Arresto anomalo quando si chiude un pacchetto che contiene un grafico MDL visualizzato
* [Grafico] Cottura a 2 passaggi: la modifica del tipo di nodo non attiva un ricreazione
* [Grafico] Arresto anomalo quando si eliminano input durante l’utilizzo della connessione
* [Grafico] Gli endpoint del collegamento possono essere spostati in uno spazio vuoto
* [MDL] Arresto anomalo durante l&#39;annullamento dell&#39;esportazione MDL dal grafico MaterialX
* [MDL] Errore durante l&#39;annullamento dell&#39;esportazione in MDLE
* [Predefiniti] Arresto anomalo nella scheda Predefiniti dopo la modifica del tipo di parametro incluso nel predefinito
* [Risorse] L&#39;elenco dei materiali è vuoto nel menu di scelta rapida del grafico per le trame collegate come non UDIM

### 10.1.2 (2020.1.2)

*(Rilasciato il 27 aprile 2020)*

**Aggiunto:**

* [Content] Aggiungi modello di filtro Alchemist
* [Content] PBR render: aggiungete i parametri per controllare l&#39;intensità delle ombre di diffusione/specular
* [Content] Nodi luce forma: aggiungete il parametro della posizione della fotocamera
* [News] Lo stile &quot;Freccia&quot; del gruppo viene interrotto la prima volta che la finestra viene visualizzata
* [Baker] Aggiungete il tasto di scelta rapida Z alla vista 2D per visualizzare l&#39;immagine in formato 1:1
* [Project] Nascondi l&#39;alias $(PROJECT\_DIR) dall&#39;elenco
* [Esplora risorse] Non creare risorse personalizzate per le risorse che non sono un file su disco

**Corretto:**

* [Player] Segnala gli alias mancanti durante il caricamento dei pacchetti SBS
* [Player] Visualizza il valore di Numero casuale in base decimale
* [Player] Raggruppa tutte le mappe dell&#39;ambiente incluse nel Substance Designer
* [Player] Arresto anomalo all’uscita da macOS High Sierra
* [Player] Impossibile caricare i pacchetti che utilizzano sbs://
* [Content] Disturbo di Worley 3D: rendering artefatto quando si utilizza un valore elevato per le dimensioni della griglia
* [Content] L&#39;input &#39;majorThanZero&#39; nel nodo &#39;Wave&#39; non è utilizzato
* [Contenuto] Luce piana: la modalità Posizione spazio mondo non funziona
* [Content] Sphere Light: la posizione interna della luce non funziona correttamente
* [Panettieri] Arresto anomalo durante la cottura con la finestra di cottura mentre è in esecuzione una mappa con baking &quot;Aggiorna tutto&quot;
* [Panettieri] La cottura al forno non riesce su Optix per AO da Trama utilizzando Bassa come Alta con una mappa Normale
* [Pannelli] La risoluzione dell&#39;anteprima dei file UVT non corrisponde alle dimensioni dello schermo
* [Vista 3D] La bitmap assegnata viene sostituita durante il caricamento di un file MDL se il valore predefinito non è una texture2d
* [Vista 3D] I widget Proprietà materiali cambiano dopo la reimpostazione di una proprietà
* [Vista 3D] La preferenza globale Formato normale non funziona più
* [MatX] Libreria: la categoria Grafico di MaterialX non visualizza tutti i nodi disponibili
* [MatX] Il menu di scelta rapida di un grafico personalizzato può contenere sottocartelle vuote nella cartella &quot;Aggiungi nodo&quot;
* [SBSAR] L&#39;input principale viene ripristinato al primo input nell&#39;elenco
* [Library] Solo il primo grafico è incluso da SBSAR con più grafici
* [CustomGraph] In alcuni casi i nodi che non fanno parte del tipo di grafico corrente vengono creati automaticamente
* [Iray] Il parametro &#39;Profondità&#39; della proiezione della casella non funziona correttamente
* [Preferenze] Migliorare il layout nelle impostazioni del progetto
* [Parametri] Arresto anomalo quando si sposta un widget posizione dopo aver eliminato un parametro
* [UI] Arresto anomalo durante la modifica della gerarchia degli usi nel nodo di output
* [Grafico] Arresto anomalo quando si utilizza un riquadro di selezione su un commento e un nodo contrassegnato

### 10.1.1 (2020.1.1)

*(Rilasciato il 10 aprile 2020)*

**Corretto:**

* [Vista 3D] L’utilizzo della memoria è troppo elevato quando si lavora sulla composizione del grafico
* [Content] Forme impreviste nell&#39;output non quadrato dei nodi &#39;Polygon&#39;
* [Contenuto] PBR render: la videocamera ortogonale non funziona correttamente quando si utilizza la risoluzione non quadrata
* [Content] PBR render: il bokeh vorticoso aumenta la luminosità del bordo dell&#39;immagine
* [Gestione colore] Il selettore colore nella finestra di dialogo Nuova bitmap non è sottoposto alla gestione del colore.
* [Gestione colore] I selettori colore negli strumenti di disegno e vettoriali nella vista 2d non sono gestiti.

### 10.1.0 (2020.1.0)

*(Rilasciato il 9 aprile 2020)*

**Aggiunto:**

* [Scelte rapide] Gestione scelte rapide per la creazione di nodi
* [Content] Nuovo nodo PBR render
* [Content] Nuovo filtro FXAA
* [Content] Nuovo filtro Hald CLUT
* [Content] Esporre i filtri nei nodi &quot;Ritaglia&quot;
* [Vista 3D] Miglioramento del flusso di lavoro per i parametri Shader e l’assegnazione delle texture
* [Vista 3D] Nuovo shader non illuminato
* [Vista 3D] Aggiungi un &quot;Valore zero scalare&quot; agli ombreggiatori di spostamento
* [Vista 3D] Aggiungi un’opzione per ridurre la risoluzione della finestra della vista quando è attivato il valore elevato di DPI
* [Vista 3D] GLSLFX: consente di impostare le informazioni dell&#39;interfaccia grafica sul campionatore (impostazione predefinita, min, max, guiMin, guiMax, guiStep, guiWidget, guiName, guiGroup)
* [Vista 3D] Aggiungi l’opzione &quot;Carica stato con trama...&quot; nel menu Scena
* [Vista 3D] Aggiungi la trasformazione dell’output con mappatura tonale ACES nella modalità di gestione colore legacy
* [Panettieri] Nuovo metodo di campionamento in AO, curvatura, curvatura normale piegato, panettieri Thickness
* [Panettieri] Nuove opzioni di normalizzazione nei panettieri per Height e Thickness
* [Gestione colore] Integrazione di Adobe (Adobe Color Engine)
* [Gestione colore] Aggiungi opzioni per impostare il comportamento predefinito quando manca il profilo ICC
* [Parametri] Rendete i cursori incrementali coerenti con Substance Painter
* [Packaging] Aggancia il maggior numero di DLL Qt possibile per gli script Python
* [Progetto] Disattiva le impostazioni per i file di progetto di sola lettura e comunica chiaramente tale stato
* [Preferenze] Nascondi impostazioni non chiare specifiche relative alla reattività e ai periodi di calcolo
* [UI] Rinomina Pow2 -> 2Pow
* [Proprietà] Ottimizzare la visualizzazione delle proprietà del grafico di composizione
* [AXF] Aggiornamento a AXF SDK 1.7.1

**Corretto:**

* [Vista 3D] I parametri Luce ambiente non sono visibili anche se è attivato
* [Vista 3D] glslfx: il widget Colore è sempre un vec3 senza alfa
* [Vista 3D] La mappa dell&#39;ambiente impostata da una risorsa non viene salvata nella risorsa scena
* [Vista 3D] Iray: la luce ambiente viene convertita in una luce punto all&#39;origine della scena
* [Vista 3D] glslfx: il widget Colore è sempre un vec3 senza alfa
* [Parametri] L&#39;URL del pacchetto dell&#39;istanza non è corretto nel gruppo di attributi
* [Parameters] Arresto anomalo durante l&#39;esposizione dei parametri
* [Parametri] Le icone non sono allineate correttamente nei parametri dei nodi di Curva
* [Parametri] La stringa del nodo &quot;Testo&quot; viene visualizzata in modalità &quot;Anteprima&quot; solo se esposta
* [Parameters] Arresto anomalo durante la ridenominazione di un parametro di input utilizzato nell&#39;istruzione &#39;Visible If&#39;
* [Parametri] Arresto anomalo durante l&#39;eliminazione di un nodo Livelli con una funzione impostata in uno dei relativi parametri
* [UI] L&#39;icona di avviso nell&#39;elenco dei parametri di input viene posizionata sopra un pulsante esistente
* [UI] Gli avvisi non vengono cancellati in un elemento parametro di input corretto in un caso specifico
* [UI] Impedisce l&#39;utilizzo di &quot;Is mesh UDIM ?&quot; pop-up da visualizzare quando gli UV della trama si trovano rigorosamente nella sezione [0,1]
* [UI] Gli elenchi a discesa Predefiniti possono essere scorsi con la rotellina del mouse con un semplice passaggio del mouse
* [UI] L’opzione &quot;Calcolo output/i&quot; negli attributi del grafico non è denominata correttamente
* [MDL] Arresto anomalo quando si inserisce una risorsa grafico SBS in un grafico MDL
* [MDL] Il nodo SBS con input immagine non funziona correttamente
* [MDL] Associazioni texture e nomi di utilizzo errati
* [Grafico] Il gruppo di valori di input e l’utilizzo vengono ignorati nella modalità di creazione del collegamento &quot;Materiale&quot;
* [Grafico] I valori di input utilizzano il valore predefinito anziché i dati di input per Booleans
* [Panettieri] Normali non corrette in World Space Normals panettiere utilizzando una mappa normale tangente in casi specifici
* [Bakers] Utilizzo eccessivo della memoria durante la cottura con la finestra di anteprima aperta
* [Predefiniti] predefiniti danneggiati causano l’arresto anomalo del rendering
* [Predefiniti] Il parametro booleano del vecchio SBS non è interessato dal predefinito
* [Library] Le risorse del primo pacchetto aperto sono elencate nel menu mobile di creazione del nodo
* [Publish] La pubblicazione su SBSAR restituisce il codice di errore 13 in SBSCooker su macOS
* [Publish] Avviso argomento obsoleto in SBSCooker durante la pubblicazione in SBSAR
* [API] Impossibile ottenere i metadati da un pacchetto proveniente da un file .sbsar
* [Esporta] In modalità Legacy, l’opzione spazio colore torna ai valori predefiniti per output specifici
* [Vista 2D] La copia negli Appunti non tiene conto dello stato di Gestione colore
* [Unix] Designer ignora i segnali di sistema
* [Libreria] Alcuni filtri nella libreria non funzionano correttamente a causa dei tag tradotti
* [Cooker] La radice quadrata di numeri negativi dovrebbe restituire 0 invece di NaN
* [Vista 2D] I canali rosso e blu vengono scambiati dopo aver annullato il primo tratto pennello
* [Console] Troppi messaggi di avviso nella console &quot;QPixmap::scaled: Pixmap è un pixmap null&quot;
* [Content] &quot;Shape Glow&quot;: avvertenza di cottura
* [Dipendenze] L’assegnazione di un grafico situato in un pacchetto diverso a una trama non crea dipendenze
* [Iray] Le proprietà dei materiali diventano inattive dopo aver cambiato la geometria

## Versione 9

### 9.3.3 (2019.3.3)

*(Rilasciato il 14 febbraio 2020)*

**Aggiunto:**

* [Batchtools] Spedizione di profili OCIO predefiniti con strumenti batch

**Corretto:**

* [Contenuto] Atlas scatter: problemi quando si utilizza colore casuale/normale in alcune situazioni

### 9.3.2 (2019.3.2)

*(Rilasciato il 4 febbraio 2020)*

**Aggiunto:**

* [SBSRender] Aggiunta del supporto per la gestione del colore

**Corretto:**

* [Content] Linear sRGB to ACEScg node: le etichette I/O non sono corrette
* [Content] ACEScg al nodo sRGB: le etichette di output non sono corrette
* [Content] Nodi di luce panoramica: regolate l&#39;intervallo di temperatura
* [Grafico] Le prestazioni peggiorano e si bloccano in modo grave quando si modifica un grafico nidificato con &quot;Modifica in contesto&quot; attiva
* [Grafico] Arresto anomalo quando si eliminano più nodi in FX-Map
* [Prestazioni] Il processo di Designer potrebbe rimanere in vita dopo la chiusura

### 9.3.1 (2019.3.1)

*(Rilasciato il 27 gennaio 2020)*

**Corretto:**

* [Grafico] Le prestazioni peggiorano e si bloccano gravemente quando si modifica un grafico nidificato con &quot;Modifica in contesto&quot; attiva
* [Grafico] Impossibile immettere un valore enum compreso tra [0, 99] nella modifica Integer1
* [Grafico] Il commento non viene spostato quando il fotogramma corrispondente viene spostato
* [Grafico] Nomi di input mancanti nel nodo di istanza personalizzato
* [Grafico] Le miniature potrebbero essere renderizzate durante il caricamento del grafico, anche se l&#39;opzione corrispondente è disattivata nelle Preferenze
* [Vista 2D] L&#39;alfa negativa mostra il controllo indipendentemente dall&#39;opzione di visualizzazione
* [Vista 2D] La conversione della superficie da 32f a 8 bit non riesce con valori alti
* [Vista 2D] Inclinazione superiore/sinistra e &#39;Crea quadrato&#39; impostano alcune coordinate su valori enormi nelle matrici di trasformazione in avanti
* [Vista 2D] Gli UV di tutti gli oggetti con trama non vengono visualizzati su set UV diversi da &quot;0&quot;
* [Contenuto] Smusso: la modalità Angular non funziona correttamente su una maschera di affiancamento
* [Contenuto] Flood Fill a sfumatura: il valore pendenza immagine non viene campionato al centro della forma
* [Content] Funzione; &quot;Equality Boolean&quot; è interrotto
* [Panettieri] Artefatti quando si utilizza la mappatura automatica dei toni nel panettiere &quot;Curvatura da trama&quot; in casi specifici
* [Bakers] Arresto anomalo in DXR durante la cottura al forno senza materiale selezionato
* [Baker] Problema di prestazioni nella vista 2D quando si abilita &quot;info&quot;
* [Engine] La funzione &#39;Pow&#39; genera valori enormi quando si utilizza un valore di input molto basso e un esponente elevato sul motore SSE2
* [Engine] Arresto anomalo quando si utilizza una compressione JPG elevata su risorse bitmap
* [Engine] Il processore valori restituisce un valore $size errato quando è all’interno di un grafico secondario
* [Parametri] Viene visualizzata una finestra a comparsa vuota quando si seleziona un nodo di istanza con un numero elevato di parametri
* [Parametri] Il valore intero non viene visualizzato negli elementi dei parametri a discesa
* [Parametri] Il pulsante &quot;Modifica&quot; della Matrice di trasformazione non è disponibile in modalità di anteprima
* [Cooker] $size in ValueProcessor è errato quando si trova all’interno di un’istanza del grafico
* [Cooker] Outputsize non corretto quando il collegamento del valore passa da un nodo punto a un nodo atomico
* [UI] Il pulsante per visualizzare tutti gli elementi nella barra inferiore della vista 2D non è visibile
* [UI] L’anteprima dei valori RGB selezionati mostra numeri errati quando si utilizza Gestione colore
* [Esportazione] Le immagini RGBA 16f vengono esportate come scala di grigi
* [Vista 3D] Impossibile importare OBJ con più spazi
* [Gestione colore] La configurazione OCIO non viene presa in considerazione durante la pubblicazione del file sbsar
* [Color Widget] Gli intervalli dei cursori dei colori possono espandersi in modo esponenziale in un caso specifico
* La sezione [Doc] &quot;paramValue&quot; è incompleta nella Guida di riferimento del formato Sbs
* [MDL] Il widget colore nelle istanze sbsar non è corretto
* [Predefiniti] Arresto anomalo durante l’aggiornamento dei predefiniti in un caso specifico
* [PSD] Errore FreeImage durante il caricamento di file PSD dalle versioni recenti di Photoshop
* [Resources] Arresto anomalo quando si annulla il collegamento bitmap direttamente nel grafico
* [SVG] I nodi SVG non si aggiornano automaticamente quando si utilizzano gli strumenti vettoriali

### 9.3.0 (2019.3.0)

*(Rilasciato il 19 dicembre 2019)*

**Aggiunto:**

* [Generale] Supporto della gestione del colore mediante il file di configurazione OpenColorIO
* [Predefiniti] Migliorare la gestione dei predefiniti
* [Predefiniti] Sincronizzare il gizmo della vista 2D e i cursori di anteprima
* [Predefiniti] Ripristina i valori di anteprima quando si torna alla modalità Anteprima
* [Predefiniti] Mantiene attiva la modalità di anteprima quando si modificano altri nodi, risorse o grafici
* [Predefiniti] L’annullamento funziona in modo uniforme quando si naviga tra le 3 schede dei predefiniti
* [Predefiniti] Consenti di ripristinare i parametri al valore predefinito del grafico o al valore predefinito del predefinito in modalità Anteprima
* [Predefiniti] Migliorare il fissaggio dei parametri
* [Predefiniti] Importa/esporta in un file tutti i predefiniti di un grafico
* [Panettieri] Nuovo panettiere &quot;Curvatura da trama&quot; basato sul ray tracing
* [Panettieri] Aggiungi opzione piano terreno nel panettiere &quot;AO da trama&quot;
* [Panettieri] Aggiungi opzione Corrispondenza per nome per ignorare il backface nel panettiere &quot;AO da trama&quot;
* [Content] Nuovo nodo di Atlas scatter
* [Content] Nuovi nodi e funzioni di conversione dello spazio colore (ACEScg)
* [Content] Miglioramento della coerenza dei nomi per i nodi con versioni a colori/scala di grigi
* [Grafico] Migliorare le prestazioni in modalità Anteprima predefiniti
* [Grafico] Opzione Aggiungi macro $(colorspace) per esportare gli output del grafico
* [Parametri] Quando un parametro è impostato su invisibile, nascondi il gizmo corrispondente nella vista 2D
* [Parametri] Non aggiungere &quot;Gruppo di input grafico&quot; come prefisso quando si espongono i parametri
* [Parametri] Aggiungi descrizione per VisibleIf nei parametri del grafico
* [AXF] Aggiornamento di AXF SDK alla versione 1.6

**Corretto:**

* [Linux] Designer non si avvia su CentOS 8 a causa di un errore di caricamento della piattaforma Qt.
* [Linux] AVVISO: la libreria Freetype è stata rimossa dall&#39;applicazione SD: gli utenti con versione CentOS &lt;= 7.5 devono installarla manualmente.
* [AxF] Arresto anomalo durante l’importazione di file creati con versioni AxF più recenti
* [2DView] Le trame del pennello alimentate da una risorsa non vengono applicate
* [2DView] Arresto anomalo durante la modifica degli input del grafico istantaneo con modifica della posizione
* [3DView] Arresto anomalo quando si annulla il caricamento... azione
* [3DView] Opzione Aggiungi spazio colore per le texture di emissione negli shader GLSLFX
* [Panettieri] Le mappe alimentate tramite risorse vengono ignorate durante la cottura al forno
* [Bakers] Le opzioni &quot;World Space Direction&quot; sono bloccate in modo errato
* [Bitmap] Le bitmap EXR con valori a virgola mobile vengono riprodotte come immagine nera
* [Content] Flood Fill da indicizzare: il rilevamento delle forme non riesce in un caso particolare
* [Content] Ritaglio: problema di campionamento quando il nodo di ritaglio ha una risoluzione inferiore all&#39;input
* [Generale] Arresto anomalo alla chiusura di Designer durante la generazione della libreria
* [Grafico] I nodi bitmap non riflettono la compressione della bitmap associata
* [Grafico] La cache non viene cancellata quando si cancellano le miniature dei nodi dopo il primo rendering
* [Grafico] Dimensione del nodo invalidata in modo errato
* [Grafico] Arresto anomalo quando si esegue l&#39;im in alcuni casi quando si modificano le connessioni di input in un nodo del processore pixel
* [Grafico MDL] Errore durante il ripristino di un valore predefinito della chiamata di funzione
* [Proprietà] I pulsanti &quot;Modifica&quot; e &quot;Matrice&quot; nei parametri della matrice di trasformazione sono confusi

### 9.2.3 (2019.2.3)

*(Rilasciato il 26 novembre 2019)*

**Aggiunto:**

* [MacOS] Autentica il software per soddisfare i nuovi requisiti di distribuzione di MacOS Catalina

**Corretto:**

* [Bakers] Arresto anomalo durante la cottura in forno utilizzando una risorsa mappa di inclinazione con un collegamento non valido
* [Panettieri] I set UV diversi da 0 non sono presi in considerazione su Embree
* [Bakers] &quot;Bent Normals from Mesh&quot; produce risultati errati con set UV diversi da 0 su DXR
* [Panettieri] I parametri &#39;UV Set&#39; vengono reimpostati sul valore &#39;0&#39; quando si riapre la finestra di cottura
* [Pannelli] La &quot;Posizione&quot; genera un&#39;immagine nera con set UV diversi da 0
* [Content] Smart Auto Tile: problema di campionamento in 8k
* [Content] Atlas splitter: il rilevamento della forma in alcuni casi non riesce, il parametro di precisione dovrebbe essere esposto
* [Content] Pow in alcuni casi non restituisce il valore corretto
* [Content] Flood Fill da indicizzare: risultato errato quando pubblicato in sbsar
* [Library] Arresto anomalo durante il caricamento del primo pacchetto SBS della sessione
* [Library] L’impostazione &quot;Mostra risorse nella libreria per impostazione predefinita&quot; viene ignorata per le risorse importate direttamente nel pannello Esplora risorse
* [Console] Messaggio imprevisto nella console quando si utilizza il menu nodo
* [Parametri] Impossibile rimuovere una singola voce nell&#39;elenco Utilizzo output
* [3DView] la scena non viene ricaricata correttamente quando il file della scena viene modificato su disco.[Grafico] I filtri del menu Nodo non sono corretti quando si utilizza l&#39;output dei valori

### 9.2.2 (2019.2.2)

*(Rilasciato il 23 ottobre 2019)*

**Corretto:**

* [Grafico] I filtri del menu dei nodi non sono corretti quando si utilizzano gli output dei valori
* [Grafico] Arresto anomalo durante la visualizzazione del menu del nodo
* [Graph] Viene visualizzato lo strumento di ricerca quando si utilizza la scelta rapida Maiusc
* [Grafico] Arresto anomalo quando i menu dei nodi vengono generati consecutivamente dal connettore di input del valore
* [Grafico] I commenti contenenti stringhe lunghe vengono ritagliati
* [Grafico] L&#39;evidenziazione del flusso non è corretta quando si crea un nodo utilizzando il menu Trascina dal connettore
* [Grafico] Arresto anomalo quando si rimuovono tutti gli elementi del grafico dalla scena durante il caricamento di un grafico diverso
* [Grafico] Arresto anomalo quando si utilizza per creare un nodo mentre si utilizza clic e trascina dal connettore
* [Grafico] Arresto anomalo durante l’utilizzo dello strumento &quot;Ricerca nodi&quot;
* [Grafico] Il colore del pin di output non è corretto nella modalità &quot;Materiale compatto&quot;
* [Cooker] I nodi a valle dei nodi con più output non vengono aggiornati correttamente
* [Cooker] Problema con gli output di valore e i nodi passthrough
* [Cooker] Il processore di valori genera risultati errati quando viene utilizzato solo un nodo &quot;Get&quot;
* [Content] Il nodo &#39;Contrast/Luminosity&#39; genera un valore di Alpha di 1,0
* [Content] Il modello &#39;Studio Panorama&#39; non ha descrizione
* [Content] Flood Fill da indicizzare: risultato errato quando l&#39;input contiene una forma a capo
* [Content] &quot;Unione HDR&quot;: il calcolo dell&#39;esposizione interna non è corretto
* [Nodo punto] Arresto anomalo quando si utilizza un livello e un nodo punto
* [Gestione dipendenze] L’azione &quot;Vai a&quot; non funziona più
* [PSD] Arresto anomalo quando si annulla l’eliminazione di più nodi inclusi in PSD Exporter
* [UI] Arresto anomalo quando si chiude un grafico utilizzando il menu &quot;Finestra&quot; e si apre di nuovo uno mentre uno è bloccato
* [Editore sfumatura] Il pulsante &quot;Rimuovi tasto&quot; è troppo grande
* [Engine] Problema di precisione con sqrt() acos() e asin()
* [Bakers] AO Da trama: il cursore &quot;Angolo di diffusione&quot; presenta un intervallo di valori errato quando viene modificato

### 9.2.1 (2019.2.1)

*(Rilasciato il 20 settembre 2019)*

**Aggiunto:**

* [Modelli] Aggiungi nodi di input predefiniti a Specular/lucidità e ad altri modelli
* [Modelli] Aggiungi modello di Anisotropia PBR
* [Vista 3D] Aumentare le distanze di distanza del piano di ritaglio automatico
* [Vista 3D] PBR Coated: modifica il valore predefinito per l&#39;ereditarietà normale Coat
* [Content] Atlas splitter: aggiungi l&#39;opzione per la funzione &quot;Ritaglio automatico&quot;
* [Menu Nodo] Non filtrare i nodi senza input

**Corretto:**

* [Contenuto] Atlas splitter: alcuni output non vengono ritagliati correttamente quando si utilizza l’opzione &quot;Ritaglio automatico&quot;
* [Contenuto] Fusione Height di materiali: errore di cottura relativo a un parametro inesistente
* [Contenuto] &quot;Luce piana&quot;: la modalità UV del pattern non funziona correttamente
* [Content] &quot;Height a unità normale&quot;: l&#39;input è forzato a 16 bit
* [Contenuto] Forme impreviste quando si utilizza il nodo angular &quot;Smussato&quot; senza affiancamento su forme di piccole dimensioni
* [Library] Le icone per sbsar non sono visibili nella libreria
* [Libreria] L’utilizzo di &quot;\&quot; per filtrare l’URL non funziona più
* [Library] I valori dei filtri fanno distinzione tra maiuscole e minuscole
* [Library] Il filtro di ricerca non funziona quando &quot;Composizione&quot; è selezionato
* [Bakers] Se si fa doppio clic su celle specifiche e si ignora la modifica, queste vengono ripristinate a valori errati
* [Bakers] Il testo dello stato backend nella finestra bakers mostra sempre &quot;Accelerazione GPU: abilita&quot;
* [Cooker] Arresto anomalo durante l&#39;elaborazione di una dipendenza &#39;impostore&#39; in un grafico
* [Cooker] la conversione in scala di grigi ha dimensioni di output errate quando si utilizza il valore
* [Explorer] Arresto anomalo durante l&#39;elaborazione di &quot;Publish su condivisione&quot;
* [Grafico] Arresto anomalo all’apertura di un pacchetto specifico
* [MDL] Arresto anomalo durante l’utilizzo dell’operatore di cast
* [Modelli] Gli identificatori di output non sono corretti nel modello rivestito PBR

### 9.2.0 (2019.2.0)

*(Rilasciato il 29 agosto 2019)*

**Aggiunto:**

* [Contenuto] Nuove forme &quot;Luce panorama&quot;
* [Content] Nuovo filtro &quot;Panorama Nadir patch&quot;
* [Content] Nuovo filtro &quot;Nadir extract panorama&quot;
* [Content] Nuovo filtro &quot;Raddrizza orizzonte panorama&quot;
* [Content] Nuovo filtro &quot;Rotazione panorama&quot;
* [Content] Nuovo nodo &quot;Posizione panorama&quot;
* [Content] Nuovo nodo &#39;Panorama Physical Sun and Sky&#39;
* [Content] Nuovi nodi &quot;Sfumature panorama&quot;
* [Content] Nuovo filtro &quot;Unione HDR&quot;
* [Content] Nuovo filtro &quot;Anteprima HDR&quot;
* [Content] Nuovo filtro &quot;Color temperature adjustment&quot;
* [Content] Nuovo nodo &#39;Blackbody&#39;
* [Content] Nuovo filtro &quot;Esposizione&quot;
* [UI] Menu per la creazione dei nodi: visualizza e gestisci i preferiti nel menu
* [UI] Aggiunge/rimuove un nodo dai preferiti dal menu Creazione nodo
* [UI] Menu per la creazione di nodi: crea un menu facendo clic/trascinando un collegamento da un output
* [UI] Menu per la creazione dei nodi: filtra il contenuto in base al tipo di selezione corrente
* [Vista 3D] Anisotropia di supporto
* [Vista 3D] Supporto dell&#39;effetto di rivestimento
* [Vista 3D] Supporto della dispersione del sottosuolo
* [Grafico] Nodo punto
* [Grafico] Ottimizza il rendering dei grafici memorizzando nella cache i risultati della cottura
* [Preferenze] Modificate il valore predefinito &quot;Limite dimensione cottura&quot; in 8192
* [Preferenze] Aggiungi un interruttore per attivare/disattivare la nuova funzionalità del tasto &quot;Tab&quot;
* [API] Aggiungi metodo SDResource.getPackage()
* [Iray] Aggiornamento a NVIDIA Iray RTX 2019.1.3 SDK (317500.3714)
* [Explorer] Consente di collegare qualsiasi tipo di file come risorsa nel pacchetto
* [GradientNode] Premete ESC per annullare la selezione della sfumatura
* [Parametri] Rimuovi maiuscole automatiche sugli identificatori
* [Project] Aggiungi un&#39;opzione per specificare se i grafici e le risorse sono &quot;Visibili nella libreria&quot; per impostazione predefinita
* [Predefiniti] Blocca automaticamente i parametri modificati

**Corretto:**

* [MDL] Impossibile esportare il modulo a causa di un problema di tipo di parametro
* [MDL] L&#39;Exposedint non è visibile durante il caricamento
* [MDL] Arresto anomalo durante l’esportazione MDL
* [MDL] Arresto anomalo durante la modifica del colore di un nodo di superficie del materiale
* [MDL] MDLGraphNodeControllerSelector vuoto::updateSelectorCurrentMember(const DataMessage&amp; msg) interrotto
* [Grafico] thickness di collegamenti errato nella visualizzazione del grafico
* [Grafico] Troppe invalidazioni vengono attivate quando si modificano i parametri
* [Grafico] Arresto anomalo quando si chiude un pacchetto mentre sono aperte due finestre dello stesso e si utilizza la modifica in contesto
* [Grafico a funzioni] L&#39;avviso non viene visualizzato quando si chiude la vista delle funzioni
* [Vista 3D] Arresto anomalo all’inizializzazione della vista 3D quando la proiezione della videocamera è impostata come &quot;ortogonale&quot; come stato della scena predefinito
* [Vista 3D] La funzionalità DOF post-FX rimane abilitata in Iray
* [Vista 2D] La finestra di selezione del pennello scompare quando si modifica la dimensione del pennello
* [Vista 2D] Pannello Informazioni: i valori vengono ritagliati con un layout specifico
* [Vista 2D] L&#39;immagine viene spostata quando si riduce a icona e si ripristina la finestra principale
* [Panettieri] L’elenco di selezione &quot;Da risorsa&quot; non viene filtrato correttamente
* [Panettieri] Arresto anomalo durante il concatenamento dei panettieri &#39;Color Map from Mesh&#39; e &#39;Normal Map from Mesh&#39; su Embree
* [Panettieri] La curvatura per vertice determina artefatti gravi
* [Explorer] Impossibile importare le risorse UDIM trascinandole in Esplora risorse
* [Esplora risorse] La finestra di Esplora risorse non viene filtrata correttamente quando si collegano trame e font dopo aver collegato formati di file insoliti
* [Explorer] Le risorse sono visibili quando il grafico ha &#39;show in Library&#39; impostato su &#39;no&#39;
* [Content] Gli input &#39;Pow&#39; e &#39;clamp&#39; non sono nell&#39;ordine corretto
* [Content] Gli input del nodo &#39;RGBA Merge&#39; non sono etichettati
* [Cooker] Connessioni non valide di valori numerici valutate comunque
* [Cooker] Asserzione quando si collega un input di immagine a un valore di input
* [UI] In alcuni casi particolari il cursore del mouse si blocca nello stato &quot;ridimensiona&quot;
* [UI] Facendo clic con il pulsante destro del mouse nella vista pacchetto non viene visualizzato il menu corretto su Linux
* [Dipendenze] Il percorso del file delle risorse temporanee non è corretto
* [Dipendenze] L&#39;avviso di risorsa bitmap mancante rimane attivo dopo il trasferimento
* [Libreria] Alcune miniature non vengono generate
* [Library] I file MDL vengono visualizzati nella libreria
* [Parameters] Arresto anomalo durante l&#39;esposizione dei parametri
* [Parametri] Arresto anomalo dopo la ricreazione di un nuovo elemento nell&#39;elenco a discesa
* [Esportazione] L’esportazione batch 8K non riesce
* [Predefiniti] Arresto anomalo quando si applica un predefinito che coinvolge booleani nelle istanze SBS
* [Scripting] La schermata iniziale viene ancora visualizzata quando si utilizza l&#39;argomento della riga di comando &#39;—quit&#39;

### 9.1.3 (2019.1.3)

*(Rilasciato il 19 agosto 2019)*

**Corretto:**

* [Bakers] Arresto anomalo in DXR quando le proporzioni dell’output di cottura e della mappa di inclinazione non corrispondono
* [Panettieri] Il fornaio &quot;Occlusione ambientale da trama&quot; produce risultati errati con Optix o DXR quando si utilizza una mappa normale
* [Baker] Il baker &quot;Curvatura&quot; genera risultati errati quando si utilizza l&#39;impostazione &quot;Per vertice&quot;
* [Bakers] I messaggi di errore indicano il backend che non è riuscito invece della causa dell&#39;errore
* [Bakers] Arresto anomalo durante l’elaborazione di una mappa di dettaglio senza una trama poly elevata
* [Pannelli] La mappa di inclinazione non sembra influire su tutto l’output con DXR abilitato
* [Content] mg\_leaks: errore di battitura nel nome dei parametri
* [Content] &quot;Shape&quot; restituisce un avviso di cottura
* [Content] I poligoni 1 e 2 non supportano funzioni casuali
* [Content] Il poligono 1 e 2 può avere meno di 3 lati
* [Content] Normale alla sede centrale del Height non funziona correttamente in non quadrato
* [Parametri] Parametri di input interi: l&#39;elenco a discesa non mostra i valori

### 9.1.2 (2019.1.2)

*(Rilasciato il 2 luglio 2019)*

**Corretto:**

* [Vista 3D] L&#39;esportazione della vista 3D con la profondità di campo attivata non sembra corretta
* [Vista 3D] Il canale di Alpha delle immagini PSD non è corretto quando si utilizza il rendering di salvataggio
* [Vista 3D] PNG e PSD non funzionano quando si utilizza l’opzione di rendering Salva con Iray
* [Vista 3D] il formato dds non funziona durante il salvataggio del rendering
* [Grafico] I nodi vengono sfalsati quando si combina destra e sinistra e si fa clic sul trascinamento in modi specifici
* [Grafico] Quando si modificano le istanze di una funzione, il risultato del nodo non viene più aggiornato
* [Grafico] Arresto anomalo durante la visualizzazione del menu Barra spaziatrice
* [Contenuto] Estrusione forma: problema di qualità quando la forma non ha rotazione
* [Content] Ombra esterna forma (e scala di grigi) non produce ombre senza affiancamento H e V
* [Contenuto] Problema normale di Ritaglio materiale
* [Bakers] I predefiniti JSON bakers non vengono caricati correttamente
* [Bakers] Arresto anomalo durante la cottura di trame pesanti con Optix o DXR (ora potrebbe non riuscire a causa di Vram insufficiente, ma non si arresta in modo anomalo)
* [Editor bitmap] Gli strumenti di pittura bitmap spostano i tratti e ridisegnano nel rettangolo di selezione del tratto
* [Editor bitmap] Strumenti di pittura bitmap danneggiati in OSX
* [UI] Il menu di alcuni pulsanti è a malapena raggiungibile
* [UI] Arresto anomalo durante il trascinamento di un’istanza di baker
* [SVG] Gli strumenti di modifica di SVG incorporati non sono affidabili
* [Parametri] Arresto anomalo quando si applica un predefinito con parametri booleani in un&#39;istanza SBSAR
* [Rete] A volte si verifica un arresto anomalo quando si verifica un errore in una connessione crittografata SSL

### 9.1.1 (2019.1.1)

*(Rilasciato il 28 maggio 2019)*

**Aggiunto:**

* [PythonIntegration] Salvare e ripristinare lo stato di Gestione plug-in
* [Preferenze]&#x200B;[Dipendenze] Aggiungi un’opzione per determinare come archiviare il percorso del file delle dipendenze
* [Content] Mappatura Flood Fill: aggiungete un&#39;opzione &quot;Adatta casella forma&quot;

**Corretto:**

* [Content] Mappatura Flood Fill: &quot;Rotazione Scala automatica&quot; fa l&#39;effetto opposto
* [Content] L&#39;input &quot;luminance\_offset\_map&quot; non viene utilizzato da &quot;Flood Fill Mapper Color&quot;
* [Content] Il nodo &#39;Mappatura Flood Fill scala di grigi&#39; genera artefatti di incremento
* [Content] Impossibile pubblicare il Height Extrude
* [Parametri] I predefiniti incorporati in sbsar non vengono caricati in Designer
* [Panettieri] Il nome del panettiere non viene visualizzato correttamente nell&#39;elenco panettieri
* [Vista 3D] &quot;Visualizza output in Vista 3D&quot; non funziona per i valori
* [Cooker] Arresto anomalo durante la correzione di un tipo di parametro errato
* [API] La funzione SDResource.setInputPropertyFromId non funziona sui parametri di input SDSBSCompGraph
* [Updater] alcuni sbs non possono essere aggiornati nel 2019
* [Explorer] Arresto anomalo durante l&#39;importazione di un file .obj specifico
* [PythonIntegration] Backslash non eseguito correttamente in Windows durante l&#39;inizializzazione di PYTHONPATH
* [UI] problema di valore con alcuni cursori nei panifici
* [Linux] Designer non può essere eseguito su CentOS &lt; 7.6

### 9.1.0 (2019.1.0)

*(Rilasciato il 9 maggio 2019)*

**Aggiunto:**

* [API] Aggiungi il parametro &#39;updatePackages&#39; al metodo SDPackageMGR.loadUserPackage() per controllare se gli aggiornamenti devono essere applicati o meno durante il caricamento
* [API] Aggiungi la possibilità di disconnettere una connessione SDConnection
* [API] Aggiungi la classe SDSBSARExporter per pubblicare un pacchetto SDP
* [API] Aggiungi la classe SDHistoryUtils per gestire i comandi non eseguibili
* [API] Aggiungere la definizione del nodo di input in scala di grigio nel grafico composizione Substance (sbs::compositing::input\_grayscale)
* [API] Aggiungere la definizione del nodo di input del valore in Substance grafico di composizione (sbs::compositing::input\_value)
* [API] Aggiungere il metodo SDProperty.isFunctionOnly()
* [API] Aggiungi il supporto del parametro di input personalizzato in SDSBSCompNode
* [API] Aggiungi il parametro &#39;reloadIfModified&#39; al metodo SDPackageMGR.loadUserPackage() per controllare se un pacchetto è stato ricaricato se modificato
* [API] Aggiungi metodo SDPackageMgr.getPackages()
* [API] Aggiunta della possibilità di ottenere, aggiungere o rimuovere percorsi radice da SDModuleMgr
* [API] Consente di ottenere il puntatore del buffer dei pixel e l&#39;intonazione di un&#39;estensione SDT
* [API] Consente di recuperare il puntatore di MainWindow.
* [API] Consente di creare menu personalizzati nel menu principale
* [API] Consente di creare DockWidget personalizzati nella finestra principale
* [API] Utilizzare i nomi degli oggetti per trovare i menu nelle barre degli strumenti
* [API] Fornisci il sistema per gestire le notifiche delle applicazioni all’API
* [PythonIntegration] Aggiungi variabile di ambiente predefinita per cercare i plug-in python
* [PythonIntegration] Aggiungi la ricerca di testo e sostituiscilo nell&#39;editor Python
* [PythonIntegration] Instanciare i plug-in Python all&#39;avvio
* [PythonIntegration] Considera variabile di ambiente PYTHONPATH
* [PythonIntegration] Consente la creazione di barre degli strumenti nei widget del grafico
* [PythonIntegration] Supporto dei thread Python
* [PythonIntegration] Aggiungi una gestione dei plug-in (nel menu &#39;Strumenti&#39;)
* [Content] Rotazione vettoriale normale: aggiungete un input immagine opzionale per guidare l&#39;angolo
* [Content] Nuovo filtro Min/Max
* [Content] Nuovo filtro &quot;Flood Fill per indicizzazione&quot;
* [Content] Nuovo filtro &quot;Mappatura Flood Fill&quot;
* [Content] Nuovo filtro Atlas splitter
* [Content] Migliora il filtro Tri Planar
* [Content] Nuovo filtro Non Uniform Directional Warp
* [Content] New Multi Directional Warp (Contenuto)
* [Content] Nuovo filtro Height Extrude
* [Engine] Fxmap: nuovo pattern &quot;Gradazione con offset&quot;
* [Engine] Supporto per l&#39;elaborazione uniforme dei valori (nuovo nodo Processore valori)
* [3D View]&#x200B;[Bakers] Miglioramento delle prestazioni del caricatore OBJ
* [Vista 3D] Aumentare le distanze piane della clip della videocamera
* [Preferenze] Aggiungere impostazioni per i panettieri
* [Grafico] Annullare la convalida più rapidamente evitando i confronti tra stringhe
* [MDL] Supporto di array MDL
* [UI] Miglioramenti dell’interfaccia utente per la selezione del motore
* [IRay] Aggiornamento a IRay SDK 2018.1.4
* [Gestione dipendenze] Utilizzare &quot;ultimo percorso&quot; quando si riposiziona una risorsa
* [Cucinare] Aggiungi il supporto delle etichette booleane nella barra degli strumenti
* Integrazione Di Qt 5.12.2

**Corretto:**

* [Grafico] Le connessioni sono interrotte quando si modifica il nome dell&#39;input
* [Grafico] Troppe invalidazioni vengono attivate quando si modificano i parametri
* [Grafico] L’azione &quot;Copia negli Appunti&quot; non funziona se si fa clic con il pulsante destro del mouse su un badge
* [Grafico] Lo spostamento di un fotogramma utilizzando Alt non è memorizzato nel file .sbs
* [MDL] Il profilo colore non viene aggiornato automaticamente nell&#39;editor MDL
* [MDL] arresto anomalo durante l’esportazione di un modulo che contiene una configurazione specifica
* [MDL] Impossibile esportare un grafico MDL contenente un LightProfile o una risorsa MBSDF
* [UI] Le scelte rapide non vengono più visualizzate nei menu di scelta rapida
* [UI] La finestra mobile diventa ancorabile dopo il riavvio
* [Scripting] L’opzione Annulla non funziona nell’editor Python
* L’opzione [Scripting] &quot;Sì a tutti&quot; nel menu Salva non funziona
* L&#39;elenco a discesa [Parametri] non viene visualizzato correttamente dopo la copia
* [Esplora risorse] Per impostazione predefinita, quando si riposizionano le risorse viene aperto l&#39;ultimo percorso riposizionato
* [Libreria] Il contenuto della libreria viene sempre ricostruito quando si passa da una versione all&#39;altra
* [Library] Le bitmap importate vengono invalidate al salvataggio
* [IRay] Lo spazio tangente non è calcolato correttamente / mappatura normale non corretta
* [Funzione] Arresto anomalo o errore durante la creazione di un nuovo grafico da una selezione
* [API] valore predefinito delle proprietà non definito

## Versione 8

### 8.3.4 (2018.3.4)

*(Rilasciato il 12 aprile 2019)*

**Aggiunto:**

* [Content] Trasformazione normale/Trasformazione materiale: aggiungete un&#39;opzione per abilitare la trasformazione Scala e Inclina

**Corretto:**

* [Content] Il filtro a spirale non funziona correttamente quando vengono utilizzate funzioni casuali nelle funzioni dei parametri
* [Contenuto] Trasformazione normale/Trasformazione materiale: la normale non viene normalizzata dopo una trasformazione di scala
* [Contenuto] Il vortice fornisce risultati errati quando la quantità è casuale
* [Grafico] Arresto anomalo quando si trascina un output tenendo premuto il tasto Maiusc e si passa poi al tasto Ctrl
* [Grafico] Arresto anomalo durante la manipolazione dei punti di divisione
* [Grafico] Calo delle prestazioni durante la visualizzazione dei badge del nodo
* [Scripting] L’utilizzo di azioni personalizzate potrebbe arrestarsi in modo anomalo dopo 30 secondi
* [Preferenze/Progetti] Gli script abilitati da tutti i progetti devono essere eseguiti (nella sezione &quot;Scripting&quot;).
* [MDL] arresto anomalo durante il collegamento di un grafico MDL a un altro grafico MDL
* [Parametri] I nodi non si aggiornano dopo aver impostato il valore di inizializzazione casuale del grafico su un parametro esposto
* [PSD] L’assegnazione del nodo di colore cambia la dimensione della miniatura del livello, ma l’assegnazione di un nodo in scala di grigio non
* [API] Eccezione non gestita con SDNode.getPropertyValueFromId()

### 8.3.3 (2018.3.3)

*(Rilasciato il 19 febbraio 2019)*

**Corretto:**

* [Content] Gli output del Materiale di base PBR non dispongono del nome di gruppo corretto

### 8.3.2 (2018.3.2)

*(Rilasciato il 19 febbraio 2019)*

**Aggiunto:**

* [Bakers] Aggiungi un&#39;etichetta che indica l&#39;impostazione corrente del suffisso per &quot;Corrispondenza per nome&quot;

**Corretto:**

* [Grafico] Arresto anomalo durante la manipolazione dei punti di divisione
* [Grafico] Problema di annullamento convalida quando viene modificata la profondità di bit del nodo di input
* [Grafico] Le opzioni di calcolo delle miniature non funzionano più
* [Grafico] Viene visualizzato uno spazio vuoto sotto il percorso con un layout di interfaccia utente specifico
* [Grafico] Lo stile del collegamento non è corretto nel contesto
* [Grafico] Le miniature non vengono visualizzate correttamente nei grafici a funzione/mdl sugli schermi ad alta risoluzione
* [Contenuto] Colore fusione splatter forma: nessuna opzione per specificare il formato mappa normale
* [Contenuto] Errore ortografico nella descrizione comando dell’interpolazione lineare
* [Contenuto] La Trasformazione normale non gestisce correttamente la trasformazione a specchio e inclinazione
* [Content] Le funzioni Assiale sfumatura, Radiale e Circolare non supportano le funzioni casuali
* [Contenuto] La Sfumatura radiale non funziona correttamente in un non quadrato
* [API] output\_exporter.sbs deve sempre essere aggiornato quando si utilizza lo script export\_output
* [API] Arresto anomalo dopo l’utilizzo dello script export\_output
* [API] Impossibile impostare il valore numerico delle annotazioni sugli input del grafico di composizione
* [Explorer] Arresto anomalo casuale durante il salvataggio di un progetto
* [Explorer] Impossibile aprire sbs con estensione maiuscola
* [UI] Le dimensioni della finestra &quot;Nuova Substance&quot; non sono persistenti
* [UI] Il menu di scelta rapida sull’istanza della funzione non è coerente con la composizione del grafico
* [Panettieri] Arresto anomalo quando si aprono i panettieri su una trama specifica
* [Pannelli] Calcolo errato per panifici DXR quando gli UV hanno un valore di ordinata 0
* [Updater] Arresto anomalo durante l’annullamento del programma di aggiornamento
* [Vista 3D] La sfera primitiva ha i suoi UV sfalsati di 1 unità
* [Cooker] Dithering casuale durante la cottura di bitmap
* [Player] I pulsanti di controllo della finestra sono piccoli
* [Lettore] Le icone dei pulsanti non funzionano

### 8.3.1 (2018.3.1)

*(Rilasciato il 20 dicembre 2018)*

**Aggiunto:**

* [API] Aggiungi SDConnection.getOutputProperty() e SDConnection.getOutputPropertyNode()
* [API] Aggiungi documento su tutte le definizioni di risorse
* [API] Per coerenza, modifica la proprietà di annotazione &#39;visibleif&#39; di SDSBSCompNode in &#39;visible\_if&#39;

**Corretto:**

* [Grafico] Se si preme di nuovo il tasto TAB, il menu Nodo non viene chiuso
* [Grafico] I distintivi della vista 3D non funzionano correttamente in alcune situazioni
* [Grafico] I pacchetti di sola lettura possono essere modificati
* [Panettieri] La barra di avanzamento agisce in modo strano quando si carica una trama poly molto alta
* [Panettieri] Artefatti su trama con normali rivolti verso l&#39;interno
* [Bakers] Impossibile decomprimere l&#39;output Bakers e il widget dei parametri
* [Explorer] Le risorse 3D vengono caricate all&#39;apertura di un pacchetto
* [CmdLineArgs] &quot;—news hide\_changelog:true&quot; non funziona più

### 8.3.0 (2018.3.0)

*(Rilasciato il 5 dicembre 2019)*

**Aggiunto:**

* [Grafico] Aggiungi un percorso di navigazione durante la modifica di sottografi/funzioni
* [Grafico] Aggiungi TAB come scelta rapida per generare il &quot;menu nodo&quot;
* [Grafico] Evidenziatore nodo per i nodi padre della selezione
* [Grafico] Aggiungi Ctrl+E come scelta rapida per aprire la funzione e i grafici secondari del processore pixel
* [Grafico] Collega il nuovo nodo al primo output visibile del nodo selezionato
* [Grafico] Aggiungere il nodo &#39;Distintivi&#39;
* [Grafico] Aggiungere un avviso per la composizione dei nodi tramite i distintivi
* [Grafico] Aggiungi la possibilità di cercare un nodo in base al nome, agli attributi o all&#39;UID
* [API] Consenti di creare e modificare i dati
* [API] Consente di esportare SDPackage e SDMDLGraph nei moduli MDL (vedere SDMDLExporter)
* [API] Consente di recuperare tutti i nodi, le enumerazioni e le definizioni di struct (vedere SDModuleMgr)
* [Vista 3D] Passa a cubi per il modulo di rendering OpenGL
* [Vista 3D] Esportare immagini hdr lineari durante il salvataggio in .exr o .hdr
* [Bakers] Integrazione della tecnologia di ray tracing DXR
* [IRay] Integrazione di IRay SDK 2018.1
* [Engine] Supporto SSE (CPU) Engine per elaborazione immagini a virgola mobile hdr
* [Engine] Aggiungi un&#39;opzione della riga di comando (—gpu x) per specificare il dispositivo GPU dedicato al motore di Substance
* [Content] Nuovo nodo di PBR render
* [UI] Rielaborare le schede e la barra del titolo
* [Gestione dipendenze] Impedisci l&#39;aggiornamento dell&#39;elenco di dipendenze quando le azioni utente non influiscono sulle dipendenze

**Corretto:**

* [Grafico] Arresto anomalo quando si crea un’istanza di un grafico su se stesso
* [Grafico] Nodo duplicato non selezionato
* [Grafico] problema di calcolo quando si utilizza la stessa istanza di nodo in 2 grafici MDL diversi
* [Grafico] Il tasto Z dovrebbe centrare la vista al centro della casella di testo della scena
* [Grafico] Ignora spazio colore nelle regole di connessione quando si utilizza il collegamento materiale
* [Grafico] Evita di aprire gli output nella vista 3D quando si apre un grafico in una console
* [Grafico] L&#39;operazione Incolla nodi è lenta quando l&#39;opzione &quot;Apri nodo appena creato&quot; è abilitata
* [Vista 3D] Asserzione quando si trascina e si rilascia una trama specifica
* [Vista 3D] L’opzione Scala UV abilitata non funziona sulla mappa del height
* [Content] Tri-Planar: Vari problemi relativi all&#39;asse e alle trasformazioni
* [Contenuto] Pendenza scala di grigi sfocatura: uno dei campioni non dispone del metodo di fusione corretto quando si utilizza min o max
* [Contenuto] Risultato errato sfumatura lineare 2 a bassa risoluzione
* [API] SDPackage.findResourceFromUrl() può anche recuperare risorse che si trovano in un altro SDPackage
* [API] SDPackage.getChildrenResources() restituisce sempre il primo elemento in modalità non ricorsiva
* [API] [Documentazione] Gli enumeratori, gli struct che si trovano nella cartella &#39;generate&#39; non sono riportati nella documentazione
* [UI] La larghezza della vista 2D non deve essere vincolata
* [Sfumatura] Arresto anomalo durante il prelievo su Mac
* [Explorer] Arresto anomalo quando si chiude e si riapre un grafico
* [Mac] Il selettore colore non funziona su più schermi
* [Parametri] La casella di selezione sui parametri interi non funziona
* [Cooker] Arresto anomalo durante la creazione di determinati nodi su OSX 10.13
* [Filtro curva] Le chiavi e i punti di controllo possono terminare con un valore -0,0 o un valore &quot;quasi zero&quot; strano nell&#39;editor della curva
* [Vista 2D] Il widget Posizione non è disponibile per i grafici provenienti da sbsar
* [PSD] Problema di livello dopo l’esportazione con dipendenze

### 8.2.2 (2018.2.2)

*(Rilasciato il 4 ottobre 2019)*

**Corretto:**

* [Contenuto] Ombra forma non funziona correttamente quando la suddivisione in porzioni è disattivata
* [Contenuto] In alcuni casi, l’opzione Riempimento a scala di grigi casuale o colore non funziona correttamente
* Il Flood Fill [Content] non è corretto in un elemento non quadrato
* [Contenuto] Il Flood Fill a colore/scala di grigi è interrotto
* [Content] QuadTransform è irregolare nella CPU
* [Content] Star Shape genera un metodo di affiancatura &quot;No Tiling&quot;
* [Contenuto] Risultato colore fusione splatter forma assoluto 32f bitdepth
* [Contenuto] Il colore di fusione dello splatter di forma è lungo da calcolare se il suo formato non è impostato su 32F
* [Grafico] Arresto anomalo quando si collega un’immagine come input di una mappa Fx mentre sono visualizzate le proprietà di iterazione
* [Grafico] Gli intervalli sembrano errati durante la modifica del grafico nel contesto
* [Grafico] Arresto anomalo casuale durante il salvataggio del grafico
* [Grafico] la modalità materiale non funziona con sbsar
* [Vista 3D] L&#39;assegnazione del materiale non viene ripristinata correttamente
* [Vista 3D] Alcune impostazioni del file di stato 3Dview non vengono caricate correttamente
* [Vista 2D] La visualizzazione in Alpha mostra sempre il nero
* [Vista 2D] Il pulsante Visualizza immagine in scala di grigio non funziona per le immagini con alfa
* [UI] il gestore delle dipendenze si attiva all’avvio anche se non è attivato in Mac
* [UI] Alcuni pulsanti eseguono azioni anche quando si rilascia il mouse all’esterno
* [API] Arresto anomalo quando si tenta di mantenere un elemento di array all&#39;esterno dell&#39;ambito dell&#39;array da cui proviene
* [Grafico MDL] Anteprima nodo capovolta
* [Grafico MDL] Lo Spostamento del nodo di anteprima è diverso da quello di 3DView
* [Console] Le prestazioni diventano molto lente quando la console contiene molti messaggi
* [Console] Avvisi Qt all&#39;avvio di Designer su CentOS
* [FX-Map] Arresto anomalo durante l’eliminazione dei collegamenti tra input e FX-map
* [Functions] Impossibile impostare un nodo di tipo stringa come output nella risorsa funzione
* [Preferenze] Il menu Preferenze è vuoto e l&#39;utente può modificare accidentalmente un valore durante lo scorrimento
* Casella combinata Indice immagine di input [FX-Map] non aggiornata correttamente quando si aggiungono o si rimuovono input
* [Dipendenze] Arresto anomalo quando si eliminano le risorse UDIM utilizzate in un grafico
* [API] SDLocationContext.getCurrentGraph() restituisce sempre null
* [Publish] URL errato per la pagina di download Substance Player

### 8.2.1 (2018.2.1)

*(Rilasciato il 17 agosto 2018)*

**Aggiunto:**

* [UI] Aggiungi un messaggio nella barra delle applicazioni quando &quot;Modifica in contesto&quot; è abilitato
* [Preferenze] Riformulare l’etichetta dell’opzione &quot;Modifica in contesto&quot;

**Corretto:**

* [Grafico] Incolla senza scelta rapida collegamento non funziona nel grafico di composizione
* [Grafico] L&#39;annullamento della convalida è molto lungo quando è abilitata la modifica in contesto
* [Grafico] Arresto anomalo durante il collegamento dei nodi
* [Grafico] Arresto anomalo durante il ricollegamento dei nodi
* [Grafico] Arresto anomalo dei fotogrammi in movimento
* [Grafico] Arresto anomalo quando si cambia file UVT nel grafico e la trama non è più udim
* [Grafico] Arresto anomalo quando si utilizza ctrl+z dopo aver incollato i nodi
* [Grafico] Seleziona nodi principali è molto lento
* [Bakers] Lo spostamento delle mappe verso l’alto/il basso consente all’utente di ridimensionare la riga
* [Pannelli] Il percorso per salvare o caricare il predefinito non viene mai salvato
* [Panettieri] La gabbia viene utilizzata anche quando non è selezionata nella finestra di cottura
* [Pannelli] La correzione dell&#39;inclinazione non funziona correttamente
* [Panettieri] Prestazioni molto lente quando è visibile uno spazio UV negativo
* [Panettieri] Facendo clic sul pulsante Annulla non si annulla il caricamento della trama
* [Panettieri] Impossibile cuocere con una gabbia se la mappa di inclinazione è vuota e impostata su true
* Il Flood Fill [Content] è lento in 4K
* [Content] La funzione lineare a sRGB è interrotta
* [Content] Affianca sfondo a gradazioni di grigio casuali è guidato da un float4 invece di un float, impedisce la cottura
* [Content] Splatter forma: il moltiplicatore posizione/mappa vettoriale non funziona correttamente
* [Scripting] Ctrl + o non funziona nell’editor di pitoni
* [Scripting] L’editor Python continua a visualizzare richieste anche dopo la chiusura
* [Scripting] Blocco durante la creazione di più nuovi script
* [UI] Le icone nella libreria sono pixalate
* [UI] I pannelli mobili per impostazione predefinita si comportano in modo errato
* [Explorer] Arresto anomalo durante l’importazione di una trama in CentOS
* [Explorer] La trama UDIM viene caricata due volte
* [Cooker] Nessun intervallo per i nodi nel contesto
* [Cucina] Sovraccarico della pila durante la cottura
* [Licenza] Autenticazione non valida con credenziali valide
* [Licenza] Licenza mobile segnalata più di una volta per lo stesso utente
* [Vista 3D] Il valore V predefinito del materiale per le porzioni UV è errato
* [3D View] Regressione delle prestazioni rispetto al 2018.1.x
* [Preferenze] Arresto anomalo quando si utilizza un file di configurazione da un server
* [Library] Arresto anomalo durante l&#39;eliminazione di un filtro all&#39;interno della libreria
* [SVG] Problema di dipendenza quando si utilizza l’alias
* [Livelli] Le bitmap HDR a 32 bit fanno lampeggiare l’editor di livelli quando si spostano i widget
* [PSD] La finestra Importazione PSD collegata viene visualizzata due volte
* [Iray] La scena viene aggiornata quando viene modificata una luce disattivata
* [MDL] Arresto anomalo durante l&#39;eliminazione di tutti i nodi di un modello MDL
* [Engine] L’enorme quantità di scostamento in FX-Map può bloccare SD
* Arresto anomalo del blocco all’avvio
* La variabile di ambiente Python causa l’arresto anomalo di Designer all’avvio

### 8.2.0 (2018.2.0)

*(Rilasciato il 19 luglio 2018)*

**Aggiunto:**

* [UI] Nuovo stile
* [UI] Nuovi cursori
* [UI] Rendi le finestre mobili davvero mobili mobili
* [UI] Modificare il layout della finestra Preferenze
* [UI] Libreria: rimuovi barra filtro
* [UI] Libreria: rimuovi la sovrapposizione di visualizzazione della selezione
* [UI] Aggiungi un messaggio nella barra delle applicazioni quando l’applicazione sta salvando automaticamente un pacchetto
* [UX] Proprietà: unione dei menu &quot;funzione&quot; e &quot;ripristina predefiniti&quot;
* [Content] Nuovi nodi di splatter forma (+ filtri complementari)
* [Content] Aggiungere Flood Fill ai filtri Colore/Scala di grigio
* [Contenuto] Nuovo supporto Flood Fill: supporta forme con fori
* [Contenuto] Da Flood Fill a sfumatura: aggiungi input da Pendenza e angolo
* [Contenuto] Ottimizza il filtro Livello automatico
* [Contenuto] Nuovo filtro Estrusione forma
* [Content] Trasformazione materiale: aggiungi il supporto per le mappe normali ruotate
* [Content] Nuovi filtri Rotazione vettoriale normale e Trasformazione normale
* [Contenuto] Normale: migliora la qualità dei risultati.
* [Content] Nuovo filtro Trasformazione trapezio
* [Content] Nuovo filtro Quad Transform
* [Content] Aggiungi pattern emisfero al nodo Shape
* [Contenuto] Aggiungere nuove sfumature con i controlli nella vista 2D
* [Content] Aggiungi output UV al nodo &quot;Cube GBuffers&quot;
* [Grafico] Cornice: ignora il testo del titolo più grande della casella della cornice per la selezione
* [Grafico] Aggiungi supporto per l&#39;edizione contestuale di sottografi (sperimentali)
* [Grafico] La creazione di frame/commento dovrebbe influire sul nodo sotto il cursore quando si utilizza RMB
* [Grafico] Cornice: ignora il testo del titolo più grande della casella della cornice per la selezione
* [Grafico] Riutilizzare la scheda esistente quando si apre una funzione già aperta
* [Grafico] Crea una nuova scheda quando viene utilizzato &quot;Apri riferimento&quot;
* [Grafico] Funzione: non visualizzare le proprietà della funzione quando si fa clic sullo sfondo
* [Parametri] Rimuovi il pulsante &quot;Esposizione&quot; dai grafici fxmap
* [Parameters] Livello: aggiungi un pulsante &quot;Inverti&quot;
* [Parametri] Espandere il gruppo &quot;Parametri di input&quot; durante la creazione di un nuovo parametro di input
* [Proprietà] Aggiungi le informazioni sull&#39;URL del pacchetto negli attributi del grafico
* [Proprietà] Aumentare le dimensioni del campo di descrizione per i nodi di output
* [Proprietà] Consente di immettere la funzione Per Pixel di Pixel Processor anche per i pacchetti di sola lettura
* [Scipting] Nuovo editor Python/API Python (prima iterazione)
* [Pannelli] Ottimizzare il trasferimento della geometria durante il rendering
* [Vista 3D] Passa al profilo principale OpenGL
* [Vista 3D] Supporto di tassellatura/spostamento in Mac
* [Functions] Risorsa funzione: elenca gli input dell’immagine nei nodi del campionatore

**Corretto:**

* [Grafico] arresto anomalo durante il collegamento di un nodo a un altro
* [Grafico] il recupero delle variabili nella funzione di inizializzazione casuale del grafico non funziona
* [Grafico] arresto anomalo quando si trascina e si rilascia rumore in un grafico
* [Grafico] arresto anomalo all’apertura di un grafico specifico
* [Contenuto] Il risultato è diverso tra Colore casuale porzione e Scala di grigi
* [Content] Tile Random: il risultato cambia quando si modifica la &quot;Modalità casuale simmetria&quot;
* [Content] Il rilevamento di Edge non funziona con risoluzioni non quadrate
* [Panettieri] Artefatti durante la curvatura con una trama UDIM
* [Panettieri] La mappa di Occlusione ambientale dalla trama viene invertita quando si utilizza una mappa normale
* [Panettieri] L&#39;elenco dei set UV deve essere limitato ai set UV disponibili
* [Esplora risorse] arresto anomalo durante l&#39;eliminazione di risorse durante la cottura al forno
* [Transform2D] Arresto anomalo durante l&#39;esposizione dei parametri del livello della mappa di interpolazione e del colore di sfondo
* [Transform2D] Comportamento errato durante l&#39;esposizione di un Livello mipmap di trasformazione
* [PSDExport] Il modulo di esportazione di PSD non esporta correttamente la scala di grigi 32F
* [Vista 2D] Il calcolo dell&#39;istogramma non funziona con i nodi 16F
* [PSD] PSD collegati non funzionanti
* [Cooker] La funzione nel parametro outputsize non viene valutata correttamente
* [Esporta] Il percorso degli output di esportazione deve essere uguale al percorso del pacchetto
* [Esporta] Il percorso di esportazione non viene salvato utilizzando un pattern vuoto
* [Modelli] Gruppo mancante per posizione nel modello Painter
* [Help] la guida della riga di comando non visualizza —news su Mac
* [Dipendenze] L&#39;esportazione due volte dopo la modifica del nome di una cartella non funziona

### 8.1.2 (2018.1.2)

*(Rilasciato il 31 maggio 2018)*

**Aggiunto:**

* [Vista 3D] Consenti di impostare lo stato predefinito della luce nelle impostazioni del progetto
* [Controllo versione] Rimuovi il timeout di 30s quando si chiamano gli script python

**Corretto:**

* [Contenuto] Base Somma frattale: risultato errato con il terzo livello (è stato aggiunto un nuovo grafico)
* [Contenuto] Il Frattale Disturbo Perlin 3D è forzato a 32 bit
* [Contenuto] La sfumatura lineare 3 non fornisce il risultato corretto quando si utilizza una dimensione non uniforme
* [Content] Sobel normale non supporta le opzioni di suddivisione in porzioni
* [Content] Checker\_1 è forzato a 8 bit
* [Contenuto] Da multiplo a normale: problema di calcolo interno
* [Contenuto] Il motivo Stripe non supporta valori &quot;Maiusc&quot; negativi (arresto del motore)
* [MDL] Arresto anomalo quando si tenta di aprire un progetto MDL specifico
* [MDL] Il grafico MDL non viene calcolato dopo un&#39;operazione chiusa/riaperta
* [Esporta] Gli output di grafici non assegnati vengono esportati utilizzando lo strumento batch
* [Esportazione] L’esportazione di C16F in exr genera un’immagine in scala di grigio
* [Panettieri] Le funzioni di inclinazione non sono disattivate nell’interfaccia utente quando si cucina in gabbia
* [Bakers] Arresto anomalo quando la gabbia non dispone del corrispondente set UV
* [Cooker] sbscooker: errore di cottura relativo a &quot;blend\_switch.sbs&quot;
* [Cooker] Il grafico pubblicato non viene riprodotto correttamente
* [Engine] Trasformazione 2D: il colore opaco non è corretto
* [Explorer] Arresto anomalo durante la reimportazione di una trama FBX
* [Color Widget] Il selettore colore in scala di grigio seleziona solo il valore del canale rosso
* [Vista 3D] L’utilizzo &quot;textcoordN&quot; non funziona più
* [Iray] La mappa normale viene applicata due volte per i dielettrici

### 8.1.1 (2018.1.1)

*(Rilasciato il 12 aprile 2018)*

**Aggiunto:**

* [Vista 3D] Imposta l&#39;intervallo predefinito di &quot;Fattore tasselazione&quot; su [0, 16]

**Corretto:**

* [Vista 3D] Strano artefatto visivo con una GPU AMD specifica
* [Vista 3D] Blocco con GPU AMD specifiche
* [Vista 3D]&#x200B;[Pannelli] Le normali generate da .obj hanno bordi netti sulla giuntura UV
* [Vista 3D] Arresto anomalo durante l&#39;elaborazione di armoniche sferiche
* [Bakers] Impossibile impostare la risorsa come &quot;incorporata&quot;
* [Panettieri] arresto anomalo durante la cottura al forno
* [Panettieri] La cottura di 2 diverse versioni di una mappa dalla trama UDIM è rotta
* [Bakers] arresto anomalo durante il passaggio da un grafico contestuale a uno non contestuale
* [Panettieri] Avere lo stesso panettiere due volte li renderà sincronizzati
* [Bakers] la ridenominazione della macro $(custom) impedisce la corretta esecuzione del baking
* [Bakers] L’aggiornamento di una mappa con baking deve bloccare l’interfaccia utente
* [Panettieri] Aggiorna tutte le mappe con baking crea risorse vuote
* [Bakers] Premendo &quot;Invio&quot; per confermare il valore di un parametro si rimuove il poly alto
* [Contenuto] Tile Generator: errore casuale rotazione quando l&#39;importo X e Y sono diversi
* [Contenuto] alcune mappe grunge contengono istanze fantasma
* [Content] Cubo 3d: l&#39;uso di funzioni casuali nei parametri non fornisce il risultato atteso
* [Contenuto] I rumori frattali non vengono riprodotti correttamente quando il Non square expansion è disattivato
* [Contenuto] Le Celle 2 e 4 non si comportano correttamente quando il Non square expansion è disattivato
* [Grafico] L’aggiornamento di un’istanza sbsar crea un grafico fantasma
* [Grafico] L&#39;assegnazione tramite clic con il pulsante destro del mouse non dovrebbe visualizzare il sottomenu dei riquadri UV per le trame non UDIM
* [Grafico] La barra secondaria ripubblicata non è aggiornata correttamente
* [Grafico] I nodi non vengono invalidati correttamente quando la risorsa cambia
* [Cooker] Il parametro di fusione alfa predefinito non viene recuperato correttamente da sbsar
* Il filtro Livelli [Cooker] non blocca i valori quando viene cotto in una barra spaziatrice
* [Cooker] La trasformazione implicita viene eseguita prima dei nodi FX-Map
* [Explorer] Premendo il tasto del su un pacchetto si chiede all&#39;utente se desidera eliminarlo
* [Explorer]&#x200B;[Bakers] Problema di ricollocazione
* [Curva] Arresto anomalo casuale durante la manipolazione dei tasti nell’editor della curva
* [MDL] Tipo di gamma non impostato correttamente per l&#39;utilizzo personalizzato
* [Parameters] Arresto anomalo durante l&#39;esposizione di un parametro con lo stesso identificatore di un input esistente
* [Proprietà] L&#39;utilizzo dell&#39;output viene modificato con lettere maiuscole e minuscole senza distinzione tra maiuscole e minuscole

### 8.1.0 (2018.1.0)

*(Rilasciato il 9 marzo 2018)*

**Aggiunto:**

* [Panettieri] Ottimizzare la cottura al forno ad alto poli
* [Panettieri] Migliora il risultato sulle cuciture per il panettiere curvatura
* [Bakers] Mappe del forno per la trama basata su UDIM
* [Baker] Aggiungete una vista 2D dedicata nella finestra Baker
* [Grafico] Supporto per UDIM
* [Grafico] Ottimizzare le prestazioni della cucina
* [Grafico] Migliorare la velocità di generazione delle miniature dei nodi
* [Grafico] Mantieni cache nodi solo per i grafici aperti
* [Grafico] Aggiungi la barra degli strumenti nel grafico di composizione per controllare la modalità di generazione delle miniature
* [Vista 3D] Aggiungere una cache della geometria per ottimizzare la visualizzazione delle trame ad alta definizione
* [Vista 3D] Supporto della visualizzazione UDIM (visualizzazione del riquadro corrente)
* [Vista 3D] Aggiornamento del cubo arrotondato con topologia uniforme
* [Vista 3D] Evita di salvare sempre le scene
* [Content] Aggiungi nodi 3D (Perlin, Perlin Fractal, Worley, Simplex)
* [Content] Aggiungi nodo maschera volume 3D
* [Content] Aggiungi nodo di 3D linear gradient
* [Content] Aggiungi nodo Gbuffer cubo 3D (utile per previsualizzare i nodi basati su 3D)
* [Content] Aggiungi nodo proiezione planare 3d
* [Content] (Contenuto) Aggiungi filtro Sfocatura radiale
* [Parametri] Visualizza le proprietà di input/output dell’immagine nelle proprietà del grafico
* [Parametri] Consenti l&#39;edizione del percorso delle risorse
* [Engine] Supporta fino a texture 8k con il motore CPU (SSE2)
* [Engine] Consenti a Convertitore scala di grigi di utilizzare gli spessori HDR per il motore HDR
* [Preferenze] Aggiungi un&#39;opzione per disabilitare la creazione automatica del nodo di conversione
* [Preferenze] Impostate la compressione predefinita per il png su &#39;velocità migliore&#39;
* [UI] supporta il collegamento html nelle proprietà del grafico
* [UI] Centra i pulsanti &quot;Sì / No / Annulla&quot; nella finestra di dialogo di conferma del salvataggio
* [Esplora] Migliora visualizzazione gerarchia trama
* [IRay] Integrazione di IRay SDK 2017.1.4

**Corretto:**

* [Pannelli] L’aggiunta di una macro nel campo del nome di output non la aggiunge alla posizione del cursore
* [Panettieri] Nessun materiale viene visualizzato nell&#39;elenco se l&#39;oggetto non ha materiale
* [Bakers] Premendo Invio per confermare i parametri del baker, aprire un menu a discesa
* [Bakers] Le texture di cottura non devono generare comandi nella pila di annullamento
* [Panettieri] Arresto anomalo durante la cottura di una texture trasferita da una trama senza specificare una texture
* [Explorer] &quot;Salva con nome&quot; deve utilizzare il nome del file esistente invece del nome della prima risorsa
* [Explorer] Comportamento errato quando si trascina una risorsa da un pacchetto a un altro
* [Explorer] Il clic con il pulsante destro del mouse non consente di aprire i dati nelle proprietà
* [Esplora risorse] L’icona degli elementi della scena non ha lo sfondo corretto
* [Grafico] Ctrl + D non funziona su Linux
* [Grafico] A volte la funzione di ricollegamento multiplo collega un solo collegamento
* [Grafico] Ctrl+Maiusc+D dovrebbe rimuovere solo i collegamenti esterni, non quelli interni
* [Grafico] Il collegamento tra scala di grigi e colore non è corretto
* [Vista 3D] Impossibile impostare una risorsa come mappa env
* [Vista 3D] Lo shader delle informazioni sulla trama non visualizza i risultati nello spazio cromatico corretto
* [Parametri] I parametri non esponibili possono essere esposti utilizzando CTRL+P
* [Parametri] I campi di testo non vengono aggiornati correttamente in caso di annullamento/ripetizione
* [Content] Artefatti in Grunge Mappa 003
* [Content] L&#39;input primario della scala di grigi vettoriale morphing non sembra corretto
* [Cooker] sbscooker genera un errore quando manca una risorsa
* [Cooking] Arresto anomalo con overflow dello stack quando la catena dei nodi è troppo lunga
* [UI] Il pulsante &quot;Esci&quot; nella gestione licenze non funziona

## Versione 7

### 7.2.5 (2017.2.5)

*(Rilasciato il 19 febbraio 2018)*

**Aggiunto:**

* [Content] Errori di battitura nella funzione.sbs
* [Contenuto] Riduci l&#39;intervallo predefinito di disturbo perlin e disturbo gaussiano
* [Vista 3D] Regola l&#39;intervallo predefinito per il parametro &quot;Scala Height&quot;
* [AXF] Aggiorna modelli mdl

**Corretto:**

* [Vista 3D]&#x200B;[Pannelli] Le normali non vengono ricalcolate se il modello non ha normali
* [Grafico] Una volta creata l&#39;istanza, la risorsa bitmap non quadrata è vuota
* [Content] Il rumore di Perlin dà risultati diversi tra la CPU e il motore GPU

### 7.2.4 (2017.2.4)

*(Rilasciato: 8 febbraio 2018)*

**Aggiunto:**

* [Importazione AXF] Consente di specificare la modalità di filtro sulle bitmap di input
* [Vista 2D] Non modificare le proporzioni dell&#39;immagine nella vista 2D quando la dimensioni fisiche è abilitata

**Corretto:**

* [Library] arresto anomalo quando si abilita/disabilita il percorso nelle preferenze
* [Baker] La corrispondenza per nome ignora alcune trame con nomi specifici
* [Content] Il filtro Premult to Straight rimuove il canale alfa

### 7.2.3 (2017.2.3)

*(Rilasciato il 19 gennaio 2018)*

**Corretto:**

* Tipo [Content] nel nodo &quot;PBR Basecolor Validate&quot;
* [Contenuto] Il parametro del disturbo è interrotto nelle Celle 2
* [Content] Cella 3 invertita quando si utilizzano valori specifici nei parametri
* [Content] Poligono 2: artefatti visivi con impostazioni specifiche
* [Contenuto] Per impostazione predefinita, la scala di grigi del Tile Generator è a 8 bit
* [Content] Campionatore porzione: il parametro casuale specifico del pattern non funziona
* [Contenuto] Mappatura forme: le funzioni casuali non possono essere utilizzate per guidare Quantità pattern, Raggio, Larghezza e così via
* [Contenuto] Poligono 2: impossibile utilizzare funzioni casuali per aumentare la quantità dei lati
* [Contenuto] Alcuni rumori/generatori di pattern generano avvisi nella console
* [Contenuto] La trasformazione non quadrata della scala di grigi genera una dimensione dei pixel errata
* [Content] Il filtro a spirale non considera la modalità di suddivisione in porzioni
* [Grafico] Il trascinamento della risorsa bitmap sul nodo di input dell&#39;immagine non funziona più
* [Grafico] CTRL+R (ricarica) non funziona più
* [Grafico] Problema quando si utilizza un fotogramma in un altro fotogramma
* [Grafico] Arresto anomalo durante lo spostamento di fotogrammi contenenti perni
* [Grafico] L&#39;istanza &quot;Shape (Legacy)&quot; viene trasformata in &quot;Shape&quot; al salvataggio
* [Baker] arresto anomalo quando si utilizza un computer senza alimentazione di 2 immagini
* [Pannelli] Colore da trama: l&#39;ID poligruppo o sottorete restituisce sempre un&#39;immagine nera
* [Panettieri] AO da trama: la distanza di occlusione è bloccata a 1 indipendentemente dal valore di input
* [Iray] Arresto anomalo durante il passaggio a Iray
* [Iray] Il valore Tiling deve influire sull&#39;intensità della scala heigh
* [Iray] Impossibile caricare IRay sul computer Windows in cui non era presente VCCOMP110.dll
* [Vista 3D]&#x200B;[Pannelli] Gli UV non possono essere decodificati dall&#39;oggetto esportato da Modo
* [Vista 3D] Le intensità di Spostamento non sono coerenti tra Opengl e Iray
* [Vista 3D] L&#39;intensità dell&#39;Occlusione Spostamento/Parallasse è il doppio di quella prevista
* [Vista 2D] offset durante la visualizzazione dell&#39;immagine alfa
* [Cooker] Impossibile trovare il parametro Constant ($tiling) se utilizzato all’interno di un’istanza del grafico
* [Cooker] Valutazione errata della variabile nelle istanze concatenate
* [Parametri] Il percorso di risorsa PKG bitmap non deve essere modificabile
* [Parametri] I parametri di uno stesso gruppo sono invisibili se un solo parametro ha la sua visibilità su false
* [PSD] Impossibile importare o collegare un file PSD da una cartella denominata con caratteri speciali
* [Funzioni] I parametri nelle funzioni non devono avere un&#39;opzione di visibilità
* [LicenseService] Eccezione generata durante il recupero di informazioni sui nodi
* [UI] Se selezioni il testo nel campo descrizione, questo viene mantenuto evidenziato

### 7.2.2 (2017.2.2)

*(Rilasciato il 23 novembre 2017)*

**Corretto:**

* [Content] Composizione &quot;Direzionale ...&quot; nodi
* [Content] Vari errori di battitura
* [Content] Tile Sampler è impostato su &quot;Absolute 32 bit&quot;
* [Contenuto] Mappatura forme: in alcuni casi, artefatti visibili sul bordo della forma
* [Content] i parametri di affiancamento e &quot;Espansione non quadrata&quot; nel poligono 1 sono danneggiati
* [Content] &quot;Numero casuale&quot; e &quot;Espansione non quadrata&quot; non funzionano con Disturbo anisotropo
* [Content] Istanza &quot;Shape&quot; danneggiata in alcune mappe di Grungi
* [Vista 3D] Il ridimensionamento UV non viene applicato se la scala height è 0
* [Vista 3D] La riflessione con il blinn dello shader non funziona più
* [2D View] Il layout della finestra delle informazioni è interrotto
* [Grafico] problema durante il controllo delle dimensioni di output con la funzione su un&#39;istanza bitmap collegata creata in un grafico
* [Funzione] Il grafico non viene invalidato quando viene eliminato un collegamento
* [Library] I preferiti non funzionano
* [Esportazione PSD] Il contenuto del file PSD cambia ogni volta che viene eseguita un’esportazione
* [Sfumatura] Arresto anomalo durante la manipolazione dei tasti nell’editor della sfumatura
* [Modelli] La mappa della posizione per i modelli di Substance Painter non è corretta
* [AxF] height fisico errato
* [MDL] Il ridimensionamento UVW da dimensioni fisiche è invertito nei nodi SBS MDL
* [Panettieri] $custom non funziona più
* Arresto anomalo di [Preferenze] all’avvio in Mac

### 7.2.1 (2017.2.1)

*(Rilasciato il 20 ottobre 2017)*

**Corretto:**

* [Engine] Arresto anomalo durante il rendering del testo con il motore GPU
* [Content] Affianca Sampler: l&#39;ID riga/colonna non funziona correttamente con non quadrato
* [Content] Affianca colore Sampler: la parametrizzazione del colore è errata
* [Content] Affianca Sampler: valore predefinito errato per la quantità di pattern X / Y
* [Esporta] Metadati mancanti nel PSD esportato

### 7.2.0 (2017.2.0)

*(Rilasciato il 19 ottobre 2017)*

**Aggiunto:**

* [Content] Aggiungi Floodfill e i filtri associati (converti una maschera in bianco e nero in sfumature, colori casuali, ecc.)
* [Content] Aggiungi nuovi generatori di Disturbo, Mappe Grunge e Pattern che supportano il formato non quadrato (la vecchia versione è contrassegnata come &quot;Legacy&quot;)
* [Content] Aggiunto nuovo Splatter Circular con molte più funzionalità
* [Content] Aggiungi nuovo generatore di Scratches
* [Content] Aggiungi filtro vortice
* [Content] Aggiungi selezione istogramma
* [Content] Aggiungi pattern a stella
* [Content] Aggiungi filtro Mappatura forme
* [Content] Aggiungi filtro morphing vettoriale
* [Contenuto] Aggiungi sfumatura lineare 3
* [Content] Affianca casuale / Tile Generator: aggiungi modalità simmetria (h+v, h, v)
* Tile Generator [Content]: aggiungete più immagini
* [Content] Rinomina &quot;Unione RGB-A&quot; in &quot;Unione Alpha&quot;
* [2D View] (Visualizzazione 2D) visualizza l&#39;output del nodo dello switch utilizzando il tasto C
* [Vista 2D] Ottimizza il layout istogramma/info in base al rapporto di visualizzazione
* [Vista 2D] Aggiungere un pulsante per attivare/disattivare la visualizzazione in porzioni
* [3DView] Ottimizzare la velocità di calcolo delle armoniche sferiche
* [Vista 3D] Aggiornate gli shader PBR per utilizzare il campionamento di Fibonacci invece di Hammersley
* [Vista 3D] Aggiungi un&#39;opzione per salvare lo stato della scena corrente come predefinito
* [3D View]&#x200B;[Bakers] Serializza i dati in un formato leggibile
* [Baker] Aggiungere predefiniti di esportazione/importazione (json)
* [Publish] Crea l&#39;archivio sbsar come non solido
* [Publish] Memorizza l’immagine o la miniatura del grafico nel database
* [Publish] Visualizza una barra di avanzamento quando viene pubblicato un pacchetto
* [Dipendenze] Visualizzare il file sbs che richiede una dipendenza nella finestra &quot;Dipendenze mancanti&quot;
* [Dipendenze] Finestra del report: visualizza un&#39;icona verde quando il problema è stato risolto
* [Dipendenze] Aggiungi un&#39;opzione per aprire le dipendenze personalizzate del pacchetto nell&#39;elenco delle cartelle dei pacchetti
* [Preferenze] Aggiungete un’opzione per impostare lo stato predefinito della scena nelle impostazioni del progetto
* [Preferenze] Aggiungi un’opzione per abilitare/disabilitare il percorso della libreria
* [Grafico] Aggiungi un&#39;opzione per creare una schermata (in scala 1:1) del grafico
* [Grafico] Rimuovi descrizione comandi dallo sfondo della composizione dei grafici
* [Scripting] Callback Add onBeforeFileLoaded e onAfterFileLoaded
* [Engine] Aggiungi un parametro di base per regolare la modalità Proporzioni pixel
* [Console] Migliorare le prestazioni della console
* [Parametri] Widget Nuova posizione (XY)
* [Iray] Aggiornamento a IRay SDK 2017.1
* [PSD] Salva lo stato del widget PSD come testo anziché come binario
* [Library] Utilizza i pollici dalla barra delle applicazioni, se esiste
* [Explorer] Rinomina &quot;Dipendenze&quot;. voce in &quot;Gestione dipendenze&quot;
* Importazione file AXF

**Corretto:**

* [MDL] Impossibile esportare il modulo MDL se la texture è connessa a un parametro esposto
* [MDL] Provare a registrare la dipendenza per le variabili stringa MDL (nodo costante)
* [MDL] arresto anomalo dopo la chiusura del pacchetto
* [MDL] arresto anomalo durante la connessione di un float 3 a un nodo di colore
* [MDL]: impossibile aprire la libreria nodi durante il rilascio di un nodo di collegamento in un frame
* [MDL] arresto anomalo quando si utilizza una texture di file
* [MDL] Il comportamento delle dipendenze registra troppi operandi
* [Grafico] I nomi dei connettori sono disattivati dopo la modifica FX-Map
* [Grafico] arresto anomalo quando si annulla
* [Grafico] Comportamento anomalo con collegamenti tra nodi
* [Grafico] I nodi compressi si dispersione e si scollegano quando si annulla
* [Grafico] L&#39;istanza della funzione non viene aggiornata quando viene modificato il riferimento
* [Controllo versione] Il pacchetto viene ricaricato quando viene attivata un&#39;azione personalizzata di Controllo versione
* [Controllo versione] Gli spazi di lavoro disattivati per il controllo delle versioni sono ancora disponibili nel menu di scelta rapida di un pacchetto
* [Controllo della versione] Rimuovi azione personalizzata non rimuoverla dal menu di scelta rapida di un pacchetto
* [Proprietà] L&#39;anteprima del parametro non viene aggiornata quando si utilizza il gizmo
* [Iray] Problema di visualizzazione del tempo massimo
* [Iray] Problema di opzione Pausa
* [Panettieri] arresto anomalo durante la cottura convertire UV in SVG utilizzando la traduzione coreano/giapponese
* [Panettieri] cambiare il percorso dopo una prima cottura non funziona
* [PSD Exporter] problema di annullamento
* La cartella [PSD] e i livelli sono bloccati in Photoshop CS5
* Il cursore colore [UI] è sempre impostato sul bianco quando viene creato un nodo di colore uniforme
* [UI] Se apri una scheda esistente, dovrebbe visualizzarla invece di duplicarla.
* [Predefiniti] arresto anomalo quando si modifica il tipo di parametro utilizzato in un predefinito
* [Vista 3D] i campionatori con lo stesso utilizzo vengono uniti
* [Vista 2D] Le informazioni sui pixel non funzionano per le immagini la cui risoluzione non è una potenza di 2
* Problema [Libreria] durante la ridenominazione dei filtri
* [Data] Correggere vari errori di battitura nei file SBS
* Nodo di livello [Parameters] - problema di precisione a livello automatico
* [Preferenze] I pulsanti delle directory dei modelli devono essere disattivati per &quot;Progetto predefinito&quot;

### 7.1.4 (2017.1.4)

*(Rilasciato il 2 ottobre 2017)*

**Aggiunto:**

* [Panettieri] Aggiungi la curvatura dal retro della trama
* [Controllo nuova versione] Aggiungere un&#39;opzione della riga di comando per disabilitare il controllo della nuova versione (—news hide\_changelog:true)
* [Scripting] Disabilita timeout Qprocess

**Corretto:**

* [I fornai] non possono cambiare il colore del materiale in UV in SVG
* [UI] non può chiudere la vista del grafico usando il clic della rotellina
* [Contenuto] Alcuni rumori sono in 8 bit invece di 16 bit
* [Contenuto] Curvatura arrotondata restituisce un risultato errato quando la suddivisione in porzioni è disattivata
* [Text] arresto anomalo durante il ridimensionamento di font specifici

### 7.1.3 (2017.1.3)

*(Rilasciato il 31 agosto 2017)*

**Corretto:**

* [Vista 3D] arresto anomalo quando si tenta di visualizzare le opzioni della vista 3D su Mac 10.10.5
* [Vista 3D] Le informazioni sul testo non vengono visualizzate nella vista 3D quando si utilizza lo schermo con valori elevati di dpi
* [Vista 3D] La preferenza globale per OpenGL/DirectX non viene considerata quando si reimposta il materiale
* [Contenuto] Height normale: il valore normale viene invertito quando si utilizza Sobel sampling
* [Contenuto] L&#39;Occlusione ambiente (hbao\_2) non si comporta correttamente se impostata su non quadrato
* [Contenuto] Gli input dei generatori di maschere non sono nello stesso ordine di &quot;Combinazione dati trama&quot;
* [Vista 2D] Istogramma: le informazioni sulla selezione non vengono aggiornate alla modifica dell&#39;immagine
* [Vista 2D] Istogramma: le informazioni sull&#39;intervallo utilizzato non vengono visualizzate per le immagini in scala di grigio
* [Predefiniti] arresto anomalo durante la ridenominazione di un predefinito di un grafico utilizzato in un altro grafico
* [Grafico] X e Y vengono invertiti nella barra degli strumenti Dimensione principale

### 7.1.2 (2017.1.2)

*(Rilasciato il 3 agosto 2017)*

**Corretto:**

* [Contenuto] Problema di filtro nei filtri &quot;Smart Auto Tile&quot; e &quot;Crop Grayscale&quot;
* [Content] I filtri libreria non tengono conto della preferenza OpenGL/DirectX
* [Content] Impossibile cucinare SBSAR con non\_square\_transform
* [Content] Forma Panorama: il punto attivo viene riflesso nel canale RGB
* [Content] Tile Sampler: la parametrizzazione del colore della posizione non è normalizzata
* [Contenuto] Affianca Sampler: i pattern sono invisibili se l&#39;affiancatura è disattivata
* [Grafico] L&#39;opzione $normal\_map\_format non funziona quando si utilizza il menu libreria/barra spaziatrice
* [Graph] Formato errato nel nodo bitmap durante il trascinamento di una risorsa RGBxxF
* [Panettieri] Il colore della trama con il colore del materiale è interrotto
* [Vista 3D] ogni modifica nella vista 3D genera azioni in una pila di annullamento
* [Dipendenze] arresto anomalo quando per un grafico mancano risorse nella libreria personalizzata
* [Iray] arresto anomalo all’avvio nella versione OSX precedente alla 10.11

### 7.1.1 (2017.1.1)

*(Rilasciato il 18 luglio 2017)*

**Aggiunto:**

* [Baker] Aggiungere un&#39;azione &quot;Ripristina&quot; nei campi delle risorse
* [Panettieri] Usa il colore nero se non viene trovato alcun colore di vertice
* [Predefiniti] Nascondi il widget dei predefiniti sulle istanze quando non sono disponibili predefiniti
* [Preferenze] Rimuovi l’opzione &quot;Calcola binormale per frammento&quot; nelle impostazioni del progetto (ora questa opzione viene gestita nel plug-in fotogramma tangente)
* regolazioni di sbsupater.exe

**Corretto:**

* [Bakers] Il sistema &quot;error&quot; non funziona più
* Serializzazione delle opzioni [Bakers]: le chiavi precedenti restano invariate
* [Panettieri] arresto anomalo quando si cambia il nome di un panettiere
* [Bakers] Problemi di interfaccia utente
* [Content] Filtro Corrispondenza colori - differenza tra CPU e GPU
* [Contenuto] Alcuni GrungeMaps generano immagini a 8 bit invece di 16 bit
* [Grafico] Arresto anomalo quando si utilizzano i &quot;collegamenti switch&quot; X sul nodo fx-map
* [Vista 3D] Arresto anomalo casuale durante l&#39;apertura della vista 3D
* [Vista 3D] Il binormale viene sempre calcolato per frammento, indipendentemente dal plug-in dello spazio tangente
* [Updater] Errore XML quando si utilizza un font specifico
* [Cooker] modulo su numero negativo non restituisce lo stesso risultato del motore
* [UI] problema dell’interfaccia quando si utilizza la sfumatura selettiva su uno schermo con DPI elevato
* [MDL] Il nodo del colore non mantiene il valore
* [Packaging] Plug-in spazio tangente Mikkt Unreal mancante

### 7.1.0 (2017.1.0)

*(Rilasciato il 29 giugno 2017)*

**Aggiunto:**

* [Bakers] Nuova interfaccia utente
* [Baker] Mantenere una cache mesh ad alta definizione fino a quando la finestra del baker non viene chiusa
* [Panettieri] Aggiungi un’opzione per correggere la deformazione dell’inclinazione utilizzando una maschera in scala di grigio
* [Panettieri] Supporta l&#39;uso-alto-poli-a-basso-poli in panettieri a trama
* [Panettieri] Rendi non modale la finestra Panettieri
* [Bakers] Memorizza lo stato nel file .sbs in un formato leggibile
* [Parametri] Copiare/incollare parametri da un grafico a un altro
* [Parametri] Aggiungere un&#39;opzione per copiare un singolo parametro di input e incollarlo in seguito
* [Parameters] Rimuovere il pulsante di funzione sul parametro &quot;Color Mode&quot;
* [Parametri] Modificare/salvare/visualizzare i parametri predefiniti incorporati
* [Parametri] Consente all&#39;utente di copiare gli attributi dei parametri quando un pacchetto è bloccato
* [Vista 3D] Non memorizza più le impostazioni della vista 3D dell&#39;ultima sessione nel Registro di sistema
* [Vista 3D] Crea nuova risorsa 3D dalla scena corrente
* [Vista 3D] Non memorizza più lo stato della vista 3D da una sessione all’altra nel Registro di sistema
* [Vista 3D] Unione dei menu &quot;Scena&quot; e &quot;Geometria&quot;
* [Vista 3D] Conversione sRGB separata dallo shader del frammento (sarà necessario aggiornare gli shader personalizzati!)
* [Vista 3D] Aggiungere un&#39;opzione per creare una nuova risorsa 3D dallo stato corrente
* [Vista 3D] Migliora il messaggio di errore generato quando #include non riesce in un codice shader
* [Vista 3D]&#x200B;[Esplora] Creare una scena 3D dalle forme di base
* [Vista 3D] Visualizza il numero di riga corretto quando la compilazione dello shader GLSL non è riuscita e il codice contiene istruzioni #include
* [Grafico] Ridimensionare una cornice da tutti gli angoli/bordi
* [Grafico] Memorizza le informazioni relative alle dimensioni padre nella risorsa grafico anziché nel Registro di sistema locale
* [Grafico] ottimizzazione della velocità di generazione delle miniature dei nodi
* [Grafico] Esporre il budget della cache di memoria nelle Preferenze
* [Grafico] Aggiungere un&#39;opzione &quot;Ripristina e visualizza nella vista 3D&quot; sui nodi
* [Contenuto] Convertitore PBR: aggiungete nuovi predefiniti Arnold 4/5, Corona 1.6 e Renderman
* [Content] Ottimizzazione del nodo AutoLevel e supporto dell&#39;input HDR
* [Contenuto] Ottimizza il filtro HBAO quando Ottimizzazione GPU è disattivata, aggiungi 16 versioni di esempio
* [Cooker] SVG di output con funzionalità non supportate nel registro
* [Cooker] Non eliminare tutte le risorse SVG se una sola funzione non è supportata
* [UI] Aumenta dimensioni blocco descrizione
* [UI] Aggiungi informazioni sul percorso del file nelle istanze del grafico
* [Funzioni] Aggiungere &quot;Apri riferimento&quot; alle istanze di funzione
* [Funzioni] Visualizza l&#39;elenco dei grafici delle funzioni quando si trascina .sbs in un grafico delle funzioni
* [Esplora risorse] Crea nuova risorsa 3D da primitiva
* [Engine] Aggiungi variabile $tiling
* [Curva] Aggiungete le opzioni per riflettere in orizzontale/verticale la curva
* [Gestione colore] Lettura del profilo ICC nelle bitmap
* [Esportazione] Aggiungere &quot;Etichetta&quot;, &quot;Gruppo&quot; e &quot;Dati utente&quot; nell&#39;elenco delle macro di tipo Pattern
* [Preferenze] aggiungete la possibilità di modificare il percorso per i file temporanei
* [Doc] Aggiungere il formato grafico MDL alla documentazione del formato SBS

**Corretto:**

* [Grafico] Problema di cache: la visualizzazione degli output nella vista 3D non funziona più
* [Grafico] Problema di cancellazione della cache
* [Grafico] Le richieste di generazione delle miniature dei nodi non vengono annullate quando il grafico viene invalidato
* [Grafico] Problemi di risoluzione dopo l&#39;utilizzo di F5
* [Grafico] visualizzazione grafico mancante all’avvio
* [Graph] La modifica di un parametro genera più chiamate di rendering
* [Grafico] arresto anomalo quando si utilizza un modello personalizzato che contiene mappe con baking
* [Grafico] Arresto anomalo quando i nodi collegati in una funzione del grafico
* [Vista 3D] Caricamento parallelo in corso con ProgressManager
* [Vista 3D] Rendering con iray a risoluzione personalizzata dell&#39;immagine non full frame
* [3D View]&#x200B;[Iray] La definizione del materiale non viene mantenuta
* [Vista 2D] L&#39;istogramma è vuoto sulle immagini LDR
* [Vista 2D] Problema di visualizzazione quando è attivata la modalità di suddivisione in porzioni
* Parametri [MDL] non esposti
* [MDL] arresto anomalo durante lo spostamento di un file MDL da un pacchetto a un altro durante il rendering
* [MDL] Non chiedere dove assegnare l&#39;MDL quando si fa doppio clic sul grafico
* [Bakers] Arresto anomalo durante il salvataggio di un file .obj specifico
* [Panettieri] La texture trasferita dalla trama / normale dà un risultato errato
* [Transformation 2D] Impossibile utilizzare i tasti freccia per modificare l&#39;offset nel nodo di trasformazione 2D
* [Transformation 2D] problema artefatto a bassa risoluzione
* [Updater] Il report di aggiornamento non viene visualizzato utilizzando Ctrl+o/apri
* [Proprietà]&#x200B;[Formato] Alcuni caratteri sono preceduti da escape due volte in UserTags
* [Nodo bitmap] Ctrl Z non funziona sulla vista 2D
* [Preferenza] Spazio vuoto inutilizzato nella scheda Alias
* [Programma di installazione] L’installazione di una versione precedente non funziona la prima volta
* Elenco a discesa [Parametri]: l&#39;inserimento di alcuni spazi nell&#39;ultima etichetta di valore blocca SD a tempo indeterminato
* [UI]&#x200B;[MAC] &quot;informazioni sulla versione di Substance&quot; visualizza le informazioni Iray
* [SVG] arresto anomalo durante l’importazione di un SVG specifico
* [Contenuto] Filtro HBAO: il parametro Radius si comporta in modo diverso in funzione della risoluzione (è stato aggiunto un nuovo hbao\_2.sbs, il vecchio hbao.sbs è ora deprecato)

## Versione 6

### 6.0.4

*(Rilasciato il 21 giugno 2017)*

**Corretto:**

* [Grafico] arresto anomalo con la scelta rapida X
* [Graph] si arresta in modo anomalo dopo l&#39;eliminazione di un collegamento tra nodi
* [Grafico] L’eliminazione di un punto di divisione provoca l’arresto anomalo di SD
* [Contenuto] Errore di battitura in mg\_surface\_brush
* [Contenuto] Qualità inferiore su HBAO rispetto a 6.0.2
* [Libreria] Le icone dei filtri personalizzati non vengono salvate
* [Explorer] Arresto anomalo quando si apre una risorsa 3D che fa riferimento a un file mancante
* [Pannelli] Trasferisci texture da trama viene riflessa se l’opzione &quot;Normale&quot; è abilitata

### 6.0.3

*(Rilasciato: 1 giugno 2017)*

**Aggiunto:**

* [Esporta] Salva dimensioni fisiche come dpi nelle texture esportate
* [Vista 2D] Visualizza l&#39;etichetta dei parametri della matrice nel menu Trasformazione

**Corretto:**

* [Content] Tile Sampler: la parametrizzazione del colore della posizione non è normalizzata
* [Content] Ritaglio: grafico fantasma nel processore pixel
* [Content] Forma Panorama: il punto attivo viene riflesso nel canale RGB
* [Content] Il filtro HBAO può generare una risoluzione negativa
* [Content] Il filtro Corrispondenza colori non viene visualizzato correttamente in alcune situazioni
* [Content] &quot;Pre-moltiplicato per semplice&quot; rimuove il canale alfa
* [Content] Errori di battitura in varie etichette
* [Grafico] Le informazioni sulla Profondità di bit vengono tagliate quando il ridimensionamento DPI è impostato su 125.1520 o 175%
* [Grafico] Quando una selezione contenente una cornice viene incollata, la cornice non viene selezionata
* [Grafico] Quando una selezione contiene un commento, gli elementi incollati vengono spostati nel grafico
* [Grafico] problema di suddivisione dei punti
* [Grafico] Alcuni connettori a perno non si agganciano al passaggio del mouse
* [Grafico] visualizzazione grafico mancante all’avvio
* [Esporta] bitmap mancanti dopo l’esportazione
* [Export] Non esporta le dipendenze dalla versione a vapore
* [Panettieri] arresto anomalo con trama che ha troppi set UV
* [Panettieri] Arresto anomalo del panettiere con mappa UV durante la cottura di trame senza set UV
* [Engine] Bug di Sampler con Fxmap+HDR
* [Engine] arresto anomalo con immagini jpeg ad alta risoluzione
* [Vista 2D] Widget Trasformazione mancante nella vista 2D quando è attivata la modalità di anteprima in porzioni
* [Vista 3D] L’istanza del grafico con utilizzo personalizzato non viene inviata correttamente alla vista 3D
* [Preferenze] Percorso errato per mikktspace.dll
* [Explorer] quando si sposta una risorsa bitmap in un pacchetto, compare il menu &quot;link/embed&quot;
* [Parameters] arresto anomalo quando si utilizza &#39;tiling&#39; come nome di parametro
* [MDL] nessun collegamento colorato tra nodi
* [Linker] Processore pixel: generazione degli shader GLSL errata
* Problema di Profondità di bit di [Cooker]

### 6.0.2

*(Rilasciato il 17 marzo 2017)*

**Aggiunto:**

* [Engine] Integrazione del motore più recente con l&#39;ottimizzazione della decompressione jpeg

**Corretto:**

* [Contenuto] La patch clone non funziona più
* [Content] L&#39;output del Height non fa parte del gruppo di materiali nei modelli
* [MDL] Arresto anomalo durante l&#39;eliminazione di un&#39;istanza del grafico
* [MDL] Nessun avviso tra nodi in conflitto
* [MDL] Messaggi di avviso inutili durante l&#39;esportazione
* [Curva] L’esposizione dei parametri di indirizzamento non deve essere esposta
* [Engine] Arresto anomalo durante l’importazione di un file sbsar che contiene una bitmap HDR
* [Nodo di testo] La specifica del font genera un file XML non valido
* [Editore sfumatura] I valori non vengono bloccati correttamente
* [Vista 3D] Arresto anomalo quando si utilizza un HDRi personalizzato (ad alta risoluzione) come ambiente

### 6.0.1

*(Rilasciato il 3 marzo 2017)*

**Aggiunto:**

* [Bakers] Miglioramento della gestione delle attività in corso
* [Pannelli] Modifica la descrizione comandi di errore quando non è selezionata alcuna trama
* [Proprietà] I parametri degli effetti Post di DView devono essere disattivati quando &quot;Post-elaborazione&quot; è disattivato in Preferenze
* [Licenza] Consenti di specificare un percorso personalizzato per la licenza del Substance Designer 6
* [Sfumatura] Disattiva il cursore &quot;precisione&quot; se non è stato effettuato alcun selettore sfumatura
* [Cooker] Ignora risorsa mancante nell&#39;input dell&#39;immagine per evitare problemi di cottura
* [Vista 3D] Modificare la gestione delle perdite di riflessi di specular
* [Grafico] Aggiungere altri parametri per la compatibilità del motore v6

**Corretto:**

* [Bakers] La mappa normale dalla trama (spazio mondo) viene capovolta sull&#39;asse Y
* [Panettieri] La cottura di una trama senza UV non segnala errori
* [Panettieri] La media normale non funziona
* [Bakers] SD si arresta in modo anomalo quando si esegue la cottura di AO con una trama specifica
* [Bakers] Il formato di output non viene ripristinato correttamente
* [Text] il font personalizzato non funziona nel lettore
* [Text] Avviso di font non valido quando riapri un pacchetto con font nelle risorse
* [Text] L&#39;input di testo non funziona in modalità di anteprima
* [Text] È possibile esporre il parametro Font
* [Text] blocco/arresto anomalo durante la creazione di una funzione nel parametro text
* [Text] Si arresta in modo anomalo quando si espongono le dimensioni del font
* [Vista 2D] La percentuale di zoom non viene visualizzata correttamente quando si utilizza il tasto &quot;F&quot;
* [Vista 2D] L&#39;immagine viene spostata quando si cambia la dimensione
* [Vista 2D] Discontinuità durante la visualizzazione della suddivisione in porzioni
* [Vista 2D] Il guizmo di trasformazione non è visibile/modificabile in modalità di anteprima
* [Vista 3D] Dimensioni fisiche non presa in considerazione dallo shader PBR Parralax
* [Vista 3D] L&#39;impostazione della frequenza di aggiornamento non viene ripristinata correttamente da una sessione all&#39;altra
* [Graph] multiangle\_to\_normal impedisce la pubblicazione
* [Grafico] La dimensione dell&#39;output del filtro di attivazione è bloccata
* [Graph]Impossibile creare un&#39;istanza dei file .sbsar
* [Curva] Interfaccia utente ritagliata
* [Curva] I numeri sono leggermente ritagliati
* [Curva] Il widget scompare quando la barra degli strumenti viene ridimensionata
* [Contenuto] Il nodo del bagliore è interrotto
* [Contenuto] Affianca Sampler: i pattern sono invisibili se l&#39;affiancatura è disattivata
* [Content] MG Mask Builder - Parametri di contrasto curvatura invertiti
* [Content] Color Equalizer: parametri personalizzati del gruppo\_color\_variation non connessi
* [Contenuto] Toppa clone: area della patch non visibile quando posizionata negli angoli
* [Explorer] Il ricaricamento di un pacchetto mentre è aperta la relativa dipendenza interrompe il pacchetto di dipendenze
* [Explorer] Impossibile importare una risorsa PSD a 32 bit
* [Publish] errore di cottura (ERR:No ereditarietà (assoluta))
* [Sfumatura] La sfumatura dovrebbe essere visualizzata come lineare quando sRGB è deselezionato
* [Transformation2D] Crea un effetto di scostamento quando si sposta un guizmo con vincolo di asse
* [Parametri] Lo stato attivo del mouse viene rubato dal menu a discesa
* [Engine] Nessuna porzione non ha effetto sul nodo distanza sul motore GPU
* [Esportazione] Arresto anomalo durante l’esportazione di output come TGA
* [MDL] il predefinito di esportazione non funziona

### 6.0.0

*(Rilasciato il 14 febbraio 2017)*

<b>Aggiunto:</b>

* [Engine] Nuovo nodo curva
* [Engine] Nuovo nodo di testo
* [Engine] Composizione profondità di bit 16f/32f
* Istanza [Engine] per GPU FX-maps
* [Engine] Aggiungi funzione log2
* [Panettieri] 8k mappa cottura
* [Panettieri] Cuocere per materiale / &quot;Set di texture&quot;
* [Bakers] Visualizza il messaggio di caricamento quando l&#39;output bitmap viene codificato/scritto su disco
* [Panettieri] Aggiungi un’opzione di annullamento durante la cottura
* [Nodo sfumatura]: aggiungi regolazioni globali per più chiavi selezionate
* [Nodo sfumatura] Semplificare le opzioni del selettore sfumatura
* [Grafico] Aggiungete un&#39;opzione per modificare le dimensioni predefinite della pagina principale
* [Grafico] Visualizza profondità pixel immagine sotto il nodo
* [Preferenze] Preferenze globali per DirectX/OpenGL
* [Preferenze] Usare le schede nell’interfaccia utente di Preferenze/Progetto
* [Preferenze] rimuovere il parametro MaxTextureSize che si trova nelle preferenze &quot;3DView&quot;
* [Preferenze] Visualizza una breve guida sul salvataggio automatico
* [Preferenze] Opzioni per il formato Esposizione immagine
* [Preferenze] Per impostazione predefinita, aggiungi un&#39;opzione per nascondere la mappa dell&#39;ambiente nella vista 3D
* [Preferenze] Aggiungete un&#39;opzione per l&#39;opzione alfa predefinita del filtro mappa normale
* [Vista 2D] Aggiungete la possibilità di eseguire il panning lontano dai limiti della texture
* [Vista 2D] Interpretare il rapporto dimensioni fisiche X/Y
* [Vista 3D] Miglioramento della gestione delle texture
* [Vista 3D] Disattiva Post Effects per impostazione predefinita (per evitare l’arresto anomalo nella gpu di fascia bassa)
* [Grafico MDL] Gestione del flag nascosto nel parametro IRay
* [Grafico MDL] Consente di impostare il costruttore &#39;material()&#39; come nodo principale
* [Grafico MDL] Anteprima nodo istanza Crea grafico SBS
* [Content] Aggiungi nuovi filtri per l’elaborazione della scansione
* [Content] Aggiungi nuovi filtri di regolazione (Blocca, Poa, Visualizzatore intervallo HDR)
* [Content] Aggiungi disturbo blu (approssimazione rapida)
* [Contenuto] Aggiungi nuovi effetti forma (Bagliore, Ombra esterna, Traccia)
* [Publish] Aggiungi un&#39;azione &quot;Esporta come precedente&quot; per ripubblicare l&#39;ultimo pacchetto selezionato
* [Publish] Miglioramento della generazione SBSAR quando si utilizzano bitmap ad alta risoluzione
* [Publish] Avvisa l’utente quando l’impostazione del grafico non è &quot;relativa alla pagina principale x1&quot; durante la pubblicazione o il caricamento su Condividi
* [Properties] Aggiungere l&#39;attributo &quot;Dimensioni fisiche&quot; ai grafici SBS
* [Parametri] Rimuovere le azioni di funzione nei percorsi delle risorse PKG
* [Parametri] Rimuovi la finestra a comparsa &quot;Anteprima valori modificati&quot;

<b>Corretto:</b>

* [Grafico] L&#39;utilizzo della memoria aumenta regolarmente ogni volta che viene aperto il menu di scelta rapida
* [Graph] [In SSE2] I nodi del poligono non visualizzano le forme quando il parametro &quot;Scale&quot; è in negativo
* [Grafico] Arresto anomalo durante il passaggio da &quot;Intero&quot; a &quot;Mobile&quot; su un parametro esposto
* [Grafico] Lo spostamento di nodi mentre è selezionato un punto di divisione consente di ricalcolare i nodi
* [Grafico] I punti divisi non supportano l’opzione &quot;Annulla&quot;
* [Grafico] descrizione vuota visualizzata quando la descrizione del grafico contiene caratteri non stampabili
* [Grafico MDL] Arresto anomalo quando il nodo corrente visualizzato nella visualizzazione delle proprietà viene eliminato
* [Grafico MDL] Il grafico MDL che utilizza la funzione di costruzione material() come root non viene renderizzato correttamente nella vista 3D
* [MDL] Impossibile esportare il modulo MDL quando si utilizza l&#39;operatore condizionale con il parametro di esposizione booleano uniforme
* [MDL] Arresto anomalo durante il caricamento di un modello di grafico MDL due volte
* [Archivio MDL] I materiali che utilizzano una texture non vengono gestiti correttamente
* [Vista 3D] Il materiale IRay non viene modificato quando cambia il nodo principale di MDLGraph
* [Vista 3D] arresto casuale quando si chiude la Vista 3D mentre è in corso il caricamento di una trama
* [Vista 3D] Yebis non viene riattivato dopo il salvataggio del rendering
* [Vista 3D] File PSD non valido generato durante il salvataggio del risultato di rendering di una scena iray
* [Vista 3D] la luce 1 del punto non si illumina
* [UI] L&#39;area di rilevamento delle caselle di controllo è troppo ampia nei parametri &quot;Pannelli da trama&quot;
* [UI] Problema estetico nei parametri &quot;Bakers from Mesh&quot;
* [Mac] L’apertura di SD con doppio clic su un file sbs non invia l’output alla vista 3d
* [Mac] [Iray] Il rendering del cluster Photoreal non funziona su MacOS
* [Engine] Atan2(0, 0) provoca l&#39;arresto del motore
* [Engine] Problema critico di sincronizzazione
* [Panettieri] Impossibile disattivare la normalizzazione automatica per il panettiere di Height
* [Parametri] quando si converte la scala di grigi in rgba, il valore di alfa deve essere 255
* [Funzioni] È possibile impostare una funzione come nodo di output anche se non compatibile
* [Esporta] Dipendenze non valide dopo l&#39;esportazione di un pacchetto con risorse PSD
* [Console] Se si cancella la console, SD si arresta in modo anomalo

## Versione 5

### 5.6.2

*(Rilasciato: 8 febbraio 2017)*

**Corretto:**

* [Preferenze] Lo shader predefinito non viene considerato
* [Vista 3D] Arresto anomalo se lo shader predefinito viene modificato in fase di runtime
* [Engine] ottieni problema $size

### 5.6.1

*(Rilasciato il 17 gennaio 2017)*

**Aggiunto:**

* [Vista 3D] Imposta dimensioni di base su 100 cm
* [Content] Aggiungere &quot;Filtro input immagine&quot; a &quot;Circolare splatter&quot; e &quot;Splatter&quot;
* [Panettieri] &quot;Curvatura da trama&quot; Aggiungi avvisi console sotto il canale &quot;Controllo di integrità trama&quot;

**Corretto:**

* [Vista 3D] Scompare se non ancorata
* [Grafico] I parametri &quot;Disturbo&quot; e &quot;Precisione&quot; della Mappa sfumatura non funzionano più
* [Vista 3D] ALT+R non funziona dopo il salvataggio del rendering
* [Panettieri] Arresto anomalo &quot;Curvatura da trama&quot; con alcune trame ZBrush

### 5.6.0

*(Rilasciato il 15 dicembre 2016)*

**Aggiunto:**

* [Content] Aggiunto nuovo filtro &quot;AO (Horizon Base Ambient Occlusione)&quot;
* [Content] Aggiunto nuovo filtro &quot;Fusione Height&quot;
* [Content] Aggiunto nuovo filtro &quot;Height to Normal (world units)&quot;
* [Content] Aggiunto il nuovo filtro &quot;Fusione Height di materiali&quot;
* [Content] Aggiunto nuovo filtro &quot;Copertina Snow&quot;
* [Content] Aggiunto nuovo filtro &quot;Water Level&quot;
* [Content] Aggiunto nuovo filtro &quot;Corrispondenza colore&quot;
* [Content] Aggiunto nuovo filtro &quot;Istogramma Scan (Non uniforme)&quot;
* [Preferences] [UI] Aggiungi un’opzione nelle Preferenze per disabilitare il rilevamento dell’impostazione Alta DPI
* [Vista 3d] Aggiungere un&#39;opzione &quot;reimposta posizione fotocamera&quot;
* [Iray] Integrazione di IRay SDK 2016.2 per il supporto dell&#39;architettura Pascal
* [Grafico] Aggiungere l&#39;opzione &quot;Copia informazioni nodo negli Appunti&quot; nel menu di scelta rapida

**Corretto:**

* [MDL] la radice del materiale alghe non viene rimossa dal predefinito esportato
* [Grafico MDL] i collegamenti per la risorsa mancante non vengono eliminati nel grafico MDL
* [Library] La creazione di un nuovo filtro crea due condizioni di base
* [Library] Folders non filtra più il contenuto della libreria
* [Panettieri] Barra di avanzamento continua
* [Panettieri] Una risorsa gabbia inesistente impedisce di cuocere
* [Contenuto] Vari errori in &quot;Functions.sbs&quot;
* [Esporta] Il formato del file è sempre reimpostato su png
* [UI] Problema di ridimensionamento dell’interfaccia utente di Substance Designer
* [Grafico] Arresto anomalo quando si sposta il pacchetto originale di un’istanza del grafico
* [Preferenze] se non viene trovato il plug-in shader/tangente predefinito, utilizzate quelli definiti nel progetto predefinito
* [Parametri] I cursori hanno molta precisione su Mac
* [Explorer] Lo spostamento della trama 3D da una cartella a un&#39;altra danneggia questa risorsa
* La chiusura della finestra non interrompe il processo SD
* La finestra di dialogo Apri file non visualizza i file con filtro &quot;Tutti i formati&quot;

### 5.5.3

*(Rilasciato il 28 ottobre 2016)*

**Corretto:**

* [Shelf] Arresto anomalo durante la creazione della cartella
* [Panettieri] World\_Space\_Direction non funziona più

### 5.5.2

*(Rilasciato il 18 ottobre 2016)*

**Aggiunto:**

* [Grafico MDL] Propaga i valori predefiniti del grafico SBS all&#39;istanza del nodo del grafico SBS nel grafico MDL
* [MDL] Supporto per trascinamento del grafico SBSAR
* [IRay] aggiornamento a SDK 2016.1.6 (261500.16187)
* [sbsrender] Ottimizza la gestione della memoria del sbsrender in base alle prestazioni del lettore
* [Vista 3D] Consente di ridurre le dimensioni del widget rispetto alla barra dei menu superiore
* [Console] Consenti di copiare alcune righe negli Appunti

**Corretto:**

* [Player] Arresto anomalo durante la riproduzione di un pacchetto direttamente in Designer tramite il pulsante di riproduzione
* File nvcuvid.dll mancante nella visualizzazione popup [Avvio]
* [Inizializzazione ambiente] quando si fa doppio clic su un file .sbs, questo non viene caricato in SD
* [Esportazione] Esportazione con dipendenze in arresto anomalo
* [MDL] Problema di sincronizzazione tra un grafico e la relativa istanza
* [MDL] I nodi dell&#39;istanza sbsar stanno eseguendo l&#39;output della texture\_return anziché dei valori
* [Vista 3D IRay] Nel modulo di rendering Iray il &quot;Canale di Height&quot; non viene aggiornato correttamente quando si cambia la mappa del height
* [IRay 3D View Undocked] &quot;Fotocamera>Salva rendering&quot; non funziona dopo aver nascosto l&#39;app nella barra delle applicazioni di Windows
* [Mac IRay] GPU NVIDIA non più rilevata da IRay
* [Panettieri] Arresto anomalo della texture trasferita dalla trama durante la cottura di texture non PENTOLA
* [Arresto anomalo] Arresto anomalo durante l’esportazione di un grafico nel Substance share
* [Grafico] Arresto anomalo quando si seleziona un’istanza fantasma
* [Vista 3D] Impossibile spostare (Zoom in o Zoom out) la videocamera ortogonale in modalità Iray
* [UI] Il selettore colore non gestisce la visualizzazione ad alto valore DPI
* [Graph] (MacOS 10.11.06) Calcolo infinito con nodo di fusione multimateriale
* [Grafico] Copia/Incolla il contenuto del grafico ==> incolla nel contenuto e anche un riferimento a quel grafico
* [Grafico] Diverse fusioni di materiali multipli nella scena, seleziona automaticamente gli output errati
* [Grafico] L&#39;Edge Wear metallico blocca il PC
* [Library] I file &quot;SBSAR&quot; visualizzano il logo &quot;S&quot; invece delle miniature
* [Library] La cartella all&#39;interno di .sbsar viene visualizzata nella libreria

### 5.5.1

*(Rilasciato: 8 settembre 2016)*

**Aggiunto:**

* [Iray] Aggiunta della modalità &quot;IQ&quot; per il rendering cloud
* [Iray] Aggiornamento a Iray SDK 2016.1.5

**Corretto:**

* [MDL] La vista in Vista 3D non funziona correttamente la prima volta
* [MDL] la sfumatura\_interpolation\_linear non viene esportata con il percorso completo
* [MDL] il riquadro in basso a destra appena creato è esattamente allineato al nodo correlato
* [MDL] In alcuni casi la miniatura del materiale principale non viene aggiornata
* [MDL] Arresto anomalo quando si eliminano e si ripristinano tutti i nodi
* [MDL] Prestazioni lente nel grafico rispetto al Grafico Substance
* [MDL] Impossibile esportare il modulo MDL a causa del parametro IOR
* [MDL] I parametri visualizzati non corrispondono al nodo selezionato
* [Vista 3D] Il materiale MDL proveniente da un grafico MDL non viene reimpostato quando viene eliminato il nodo principale
* [Vista 3D] L’inquadratura predefinita della fotocamera viene persa dopo aver caricato la trama fbx
* [Vista 3D] L&#39;assegnazione della texture non viene mantenuta quando si passa a Iray
* [Iray] Messaggio di avviso da IRay durante lo spostamento della fotocamera
* [Iray] Arresto anomalo quando si passa a Iray
* [Iray] Password VCA non salvata
* [Grafico] Arresto anomalo durante l&#39;eliminazione dei nodi
* [Grafico] Premere CTRL per copiare il collegamento non funziona con la modalità Materiale
* [Grafico] Arresto anomalo durante l&#39;eliminazione del nodo di output in un materiale del nodo di istanza
* [Pannelli]&#x200B;[Vista 3D] Impossibile caricare la trama ad alta definizione
* [Mac]&#x200B;[Vista 3D] Arresto anomalo quando si tenta di ripristinare le finestre scollegate sul monitor secondario
* [Parametri] Impossibile modificare un valore in uno spinboxedit senza rimuovere il suffisso
* [UI] Usa &quot;Annulla&quot; quando si chiude SD dovrebbe interrompere la finestra di messaggio
* Arresto anomalo all’apertura di due viste 3D
* Arresto anomalo in Alg::Scripting::Engine quando si utilizzano molte condizioni VisibleIf
* I file vengono eliminati dal salvataggio automatico se esiste un file algautosave

### 5.5.0

*(Rilasciato il 25 agosto 2016)*

<b>Aggiunto:</b>

* Il Substance Designer è ora disponibile su Linux
* Nuovo editor MDL (Material Definition Language)
* [Panettieri] Nuova curvatura dal panettiere mesh
* [Library] Utilizza icone SVG anziché file bitmap
* [Library] Aggiungi un&#39;opzione per filtrare il risultato per MDL, Composizione, Funzione e Fxmap
* [Grafico] Estendere &quot;Visualizza nodo appena creato&quot; per copiare/incollare/duplicare i nodi
* [Nuovo documento] Creare un widget di selezione dei modelli durante la creazione di un nuovo grafico MDL
* [3D View]&#x200B;[Iray] Visualizza i nodi Modalità rendering + VCA accanto a iterazioni/tempo
* [Vista 3D] Migliorare le prestazioni del menu &quot;materiale&quot; all&#39;apertura
* [3DView]&#x200B;[Bakers] Aggiornamento a FBX SDK 2017
* [Vista 3D] Consente di mostrare/nascondere le informazioni di rendering (risoluzione, iterazioni, ecc.). nel menu di visualizzazione di Vista 3D
* [Iray] Esporre i parametri di tassellatura alla modifica della scena
* [Project] Aggiungi alias generato automaticamente per la directory dei file di progetto
* [Progetto] Specifica la texture di ambiente predefinita nelle impostazioni del progetto
* [Content] Aggiunto nuovo studio HDRi
* [Content] Aggiungi il nodo di trasformazione non quadrato alla libreria
* Avvia SD con un file .sbscfg specifico

<b>Corretto:</b>

* [Grafico] Gli input non si collegano automaticamente agli output con lo stesso utilizzo.
* [Grafico] Gli input dei nodi inseriti non sono collegati correttamente
* [Grafico] Deselezionando dovrebbe anche essere selezionato un nodo sotto il mouse
* [Grafico] L&#39;inserimento del nodo non si connette a tutti i collegamenti
* [Panettieri] Diffusione errata nel panettiere curvatura
* [Bakers] &quot;Texture trasferita da trama&quot; si arresta in modo anomalo se la trama ad alta definizione non ha UV
* [UI] L’icona della funzione nei parametri non viene modificata quando viene definita una funzione
* [UI] Suggerimenti per i parametri tagliati
* [Vista 3D] nella scena sono visualizzate più di 1000 luci
* [Vista 3D] Lo shader Lambert GLSL non gestisce correttamente la texture srgb
* [Vista 3D] Parametri di affiancatura mancanti quando si collegano le sostanze in Iray
* [Iray] L’esportazione dei predefiniti di mdl non funziona quando gli spazi nel nome
* [Iray] I parametri di suddivisione non sono presi in considerazione
* [Parametri] L&#39;identificatore del parametro non è più visualizzato
* [Parametri] Arresto anomalo quando si modifica l’URL della risorsa da &quot;Da risorsa...&quot; azione
* [Parametri] Conversione errata di &amp; character
* [Explorer] Quando si fa doppio clic su un grafico &quot;grande&quot;, spesso non si apre nella vista del grafico
* [Explorer] I SVG incorporati risultano mancanti in Esplora risorse
* [Explorer] Arresto anomalo durante la ridenominazione di un elemento con il carattere &quot;&amp;&quot;
* [Contenuto] L&#39;affiancamento della sfumatura 1 è errato quando si utilizza la rotazione a 90/180°
* [Perforce] L’integrazione non sembra funzionare se l’area di lavoro si trova nella directory principale dell’HDD
* [Data] UID generato per i nodi non univoco
* [Preferenze] L&#39;aggiunta di un alias che ha come destinazione la directory principale del disco rigido comporta la modifica dei percorsi in sbsprj
* [PERDITA DI MEMORIA] Alcuni QDialog non vengono distrutti quando vengono chiusi

### 5.4.0

*(Rilasciato il 29 aprile 2016)*

**Aggiunto:**

* Aggiungi un collegamento a Substance Store
* [UI] Supporto per risoluzioni DPI elevate
* [UI] Consenti di riordinare le schede
* [Vista 3D] Consente di esportare il rendering in ArtStation
* [Vista 3D] Aggiungete lo shader predefinito nell&#39;elenco dello shader
* [Grafico] Visualizza il nome della risorsa sopra il nodo bitmap
* [Grafico] Migliorare l&#39;ordine di elencazione del menu di ricerca della barra spaziatrice
* [Panettieri] Nuovo panettiere &quot;Posizione dalla trama&quot;
* [Panettieri] Nuova impostazione &quot;mappa normale&quot; per il panettiere Trasferimento texture
* [Panettieri] Nuova impostazione &quot;Tangente&quot; e &quot;Binormale&quot; per World Space Normal baker
* [Scripting] Consente di eseguire script durante le azioni Salva, Esporta e Publish
* [Dipendenze] Aggiungi un&#39;opzione Comprimi/Espandi in base alla selezione
* È stato aggiunto un avviso relativo ai conflitti di estensione della shell

**Corretto:**

* Arresto anomalo all’uscita
* Il processo di Substance Designer può essere ancora in esecuzione dopo l&#39;uscita
* [Iray] Gli output non vengono inviati ai materiali mdl quando si cambia modulo di rendering
* [Content] Campionatore porzione: la rotazione casuale del pattern non deve ruotare la forma

### 5.3.5

*(Rilasciato il 6 aprile 2016)*

**Corretto:**

* [Vista 2D] Opzione di menu di scelta rapida Trasformazione 2D disponibile su qualsiasi nodo
* [Vista 2D] trasformazione 2d gizmo ancora modificabile dopo l&#39;eliminazione del nodo di trasformazione
* [Vista 3D] Il percorso dell&#39;ambiente non deve essere visualizzato in Parametri ambiente
* [Vista 3D] I parametri degli effetti post non vengono salvati nelle risorse 3D
* [Vista 3D] Il menu della barra degli strumenti non si comporta come un menu normale
* [Preferenze] Impossibile impostare il &quot;Limite cache motore&quot; su un valore superiore a 4095
* [Preferenze] L’impostazione di uno shader predefinito non viene considerata
* [Iray] I parametri del colore non vengono recuperati correttamente
* [Iray] I colori dei materiali MDL vengono reimpostati
* [Iray] Le bitmap non vengono esportate insieme al predefinito MDL
* [IRay/Mac] Il ridimensionamento della vista 3D provoca l&#39;arresto anomalo della workstation Mac
* Il documento [Graph] PSD non viene esportato
* [Grafico] Dimensione del nodo visualizzata non corretta
* [Grafico a funzioni] L&#39;immagine di input del nodo di esempio non è modificabile se è collegata una sola immagine
* [Engine] Arresto anomalo durante l&#39;elaborazione del grafico Fxmap
* [Engine OGL] Errore nella generazione del processore pixel
* [Sfumatura] Il selettore sfumatura non funziona sul Mac
* [PSD] Immagine a 8 bit non convertita correttamente in 16 bit
* [Parametri] Il widget Istogramma livello non ha lo stesso height nel colore e nella scala di grigi
* [Console] Facendo clic su una cella si scorre la vista orizzontalmente
* [Esplora risorse] Le risorse 3D riposizionate non vengono aperte correttamente nella vista 3D

### 5.3.4

*(Rilasciato il 16 gennaio 2016)*

**Corretto:**

* [Iray] tangente/binormale non sono presi correttamente in considerazione
* [Explorer] Il pacchetto è contrassegnato come salvato subito dopo l&#39;apertura
* [Vista 3D] Il riflesso diffuso IBL è troppo forte
* [Vista 3D] Arresto anomalo durante il trascinamento di un&#39;immagine a 8 bit da Esplora risorse a Vista 3D
* L’applicazione si blocca dal 1° gennaio 2016

### 5.3.3

*(Rilasciato il 10 novembre 2015)*

**Aggiunto:**

* [Content] Aggiungi &quot;White Noise Fast&quot; (basato sul processore pixel)
* [Content] Aggiungi &quot;Offset global horizontal/vertical&quot; sui campionatori porzione

**Corretto:**

* Arresto anomalo durante la creazione di una nuova Substance in alcune situazioni
* [Bakers] Arresto anomalo quando la mappa con baking aggiorna il grafico
* [Bakers] L&#39;OBJ proveniente da zbrush deve utilizzare il nome file per Corrispondenza per nome
* [Parameters] Arresto anomalo durante l&#39;esecuzione di Annulla/Ripeti/Annulla nel grafico delle funzioni
* [Grafico] I punti di divisione non vengono incollati nella posizione corretta

### 5.3.2

*(Rilasciato il 30 ottobre 2015)*

**Aggiunto:**

* [Contenuto] Aggiungi controllo filtro per input pattern su Tili Generator

**Corretto:**

* [Vista 3D] Punto di interesse non inizializzato correttamente
* [Vista 3D] Piano della clip distante errato quando si cambia più volte le risorse della trama 3D
* [Vista 3D] Breve artefatto di rendering durante il caricamento di una trama
* [Vista 3D] La mappa dell&#39;ambiente è nera quando non è possibile trovare il file -> fallback all&#39;envmap predefinita
* [Vista 3D] Arresto anomalo dopo l’utilizzo di un’immagine personalizzata per la latitudine e la longitudine
* [Vista 3D] Arresto anomalo durante il caricamento di un file obj specifico
* [Vista 3D] il caricamento automatico della trama non funziona correttamente
* [Iray] Impossibile assegnare la texture su un mdl esterno
* [Iray] Impossibile assegnare texture al canale di anisotropia dopo il ripristino del materiale
* [UI] Viene visualizzato il menu di scelta rapida di Windows quando viene rilasciato il pulsante destro del mouse dopo lo spostamento in 3DView
* [Vista 2D] Lo strumento Informazioni non restituisce il valore del colore del pixel sotto il cursore
* [Pannelli] Le immagini in scala di grigio vengono salvate come indicizzate con il formato tga
* [Grafico] Visualizza output in vista 3D dovrebbe reimpostare i canali prima di inviare gli output in vista 3D
* [Parameters] Il nome di input del parametro è vuoto quando viene esposto da &quot;Exposé node parameters&quot;
* [Prestazioni] Impostare il callback onSubstanceCallbackProfileEvent sul motore SOLO se gli intervalli sono abilitati

### 5.3.1

*(Rilasciato il 21 ottobre 2015)*

**Aggiunto:**

* [Vista 3D] Visualizza il nome della trama nella scena/modifica invece di &quot;Entità&quot;
* [Vista 3D] Ripristina il colore predefinito quando viene aperta una nuova vista 3D
* [Vista 3D] Messa a fuoco della fotocamera quando si passa da scena a primitiva
* [Vista 3D] Visualizza la risoluzione della finestra della vista di rendering quando si utilizza la risoluzione personalizzata
* [Iray] Regola presentazione dei parametri di suddivisione
* [Iray] Trasmette le informazioni di log IRay al log SD
* [Bakers] Leggi correttamente i file OBJ per rendere compatibile la corrispondenza per nome

**Corretto:**

* [Vista 3D] Visualizzazione errata di trame con una scala diversa da 1.0
* [Vista 3D] Il calcolo automatico del piano vicino alla clip non funziona bene per gli oggetti grandi
* [Vista 3D] La modalità Wireframe visualizza fili troppo spessi
* [Vista 3D] La finestra Salva rendering non viene visualizzata se gli effetti post sono disattivati
* [Vista 3D] Arresto anomalo quando si cambia geometria
* [Vista 3D] Messaggio &quot;QOpenGLWidget: Cannot make uninitialized widget current&quot; nel registro
* [Vista 3D] L&#39;illuminazione non viene calcolata se la mappa dell&#39;ambiente viene modificata mentre Iray è in esecuzione
* [Vista 3D] Arresto anomalo durante la visualizzazione della trama 3D
* [Vista 3D] Prestazioni OpenGL molto cattive dopo aver utilizzato Iray
* [Vista 3D] I piani delle clip non vengono calcolati correttamente
* [Vista 3D] La modifica della mappa dell&#39;ambiente non aggiorna la vista 3D
* [Vista 3D] Le texture non vengono aggiornate al cambio del grafico
* [Vista 3D] I campionatori GLSLFX nascosti sono ancora visualizzati nel menu di selezione
* [Vista 3D] Materiale non ripristinato correttamente all&#39;apertura della risorsa mesh
* [Vista 3D] Perdita di memoria RAM/VRAM quando si aprono varie trame e si assegnano più grafici su di esse
* [Vista 3D] L&#39;attivazione non tiene conto della lunghezza focale
* [Iray] nvcuvid.dll mancante (disinstallare la versione precedente per eliminare il messaggio)
* [Iray] Il pulsante &quot;...&quot; della finestra di dialogo Esportazione predefiniti non apre la finestra di dialogo
* [Iray] La rifrazione/dispersione non funziona correttamente in specular\_diffuso\
* [Iray] Impossibile trovare il mdl predefinito (colore magenta)
* [Iray] Non collegate le texture predefinite al materiale mdl per attivare la modalità valore in Modifica materiale
* [Iray] Descale non viene attivato quando si aggiorna una texture
* [Panettieri] Worldspace fornaio normale rende un&#39;immagine nera
* [Bakers] Arresto anomalo durante la cottura di una mappa normale con vista 3D non ancorata
* [Bakers] Il funzionamento in baking con il metodo &quot;Embedded&quot; mentre è impostato un percorso non valido per &quot;link&quot; impedisce il salvataggio della risorsa
* [Baker] Il funzionamento in baking con il metodo &quot;Embedded&quot; e la modifica del formato del file non modifica l&#39;estensione sul disco
* [Bakers] I nomi casuali per le risorse incorporate hanno tutti un nome XXX..
* [Pannelli] Più oggetti in .obj non vengono importati correttamente
* [Content] Fusione materiale: l&#39;output del colore di base non viene nascosto quando il canale è disattivato
* [Contenuto] Bianco\_disturbo e derivati non vengono riprodotti correttamente in 8k
* [Grafico] Prestazioni lente nel grafico
* [Grafico] Arresto anomalo quando si trascina un elemento di funzione dalla libreria al grafico delle funzioni
* [Grafico] &quot;Visualizza output nella vista 3D&quot; dovrebbe inviare solo l&#39;output visibile del nodo nella vista 3D
* [Preferenze] L’utente predefinito\_project ha un &quot;Suffisso nome&quot; vuoto per la funzione di aggiunta nome
* [Engine] La conversione a colori -> in scala di grigi produce perdita di precisione
* [Console] Console/Log è inquinato da molti messaggi
* [Condividi] Arresto anomalo quando si tenta di condividere un pacchetto
* [UI] La descrizione è bloccata sopra il menu File recenti
* Arresto anomalo all’uscita

### 5.3.0

*(Rilasciato il 1° ottobre 2015)*

<b>Aggiunto:</b>

* [Vista 3D] Aggiungere il modulo di rendering Nvidia Iray
* [Vista 3D] Ruota l&#39;ambiente utilizzando CTRL+MAIUSC+RMB
* [Vista 3D] Esegui il rendering della vista 3D a una risoluzione personalizzata (Ogl / Iray)
* [Vista 3D] Rendere asincrono il caricamento della scena
* [Vista 3D] Visualizza la scena globale nel Visualizzatore scene
* [Vista 3D] Disattiva la griglia per impostazione predefinita
* [Vista 3D] Aggiungi attenuazione distanza quadrata inversa per luci di punti
* [Vista 3D] Visualizza il parametro del colore in RGB anziché in RGBA
* [Vista 3D] Impostazioni Luci/Videocamera/Ambiente separate
* [Condividi] Miglioramenti per la finestra di caricamento del Substance share

<b>Corretto:</b>

* [Vista 3D] Errore nella normalizzazione degli shader PBR
* [Vista 3D] Arresto anomalo quando si fa clic con il pulsante destro del mouse sulla cartella principale nell&#39;elenco scene
* [3D View] Ombreggiatori PBR: risparmio energetico e punti di interesse diffusi rispetto alle specifiche
* [Vista 3D] Rendi &quot;Materiale/Ripristina&quot; anche ripristinando i canali al colore predefinito
* [Panettieri] Posizione con normalizzazione sfera non centrata
* [UI] Stato mobile di Windows non salvato alla chiusura dell’applicazione
* [Cooker] Impossibile pubblicare quando l&#39;sbs si trova in un percorso contenente un carattere speciale
* [Pubblicazione] Premendo &quot;invio&quot; nel campo del nome dopo la pubblicazione, la finestra di dialogo viene annullata
* [Condividi] L’esportazione sbs non mantiene l’alias sbs://

### 5.2.5

*(Rilasciato il 15 settembre 2015)*

**Aggiunto:**

* [Condividi] Publish di un pacchetto al Substance share
* [UI] Collegamento Aggiungi Substance share nel menu Aiuto

**Corretto:**

* [Cooker] &quot;Dimensione fuori dai limiti&quot; è un errore invece di un avviso
* [Cooker] &quot;Impossibile trovare l&#39;output del grafico secondario&quot; è un errore invece di un avviso
* [Vista 3D] Diffusione/specifica PBR preferisce il colore di base invece della diffusione
* [Vista 3D] La suddivisione in porzioni non funziona correttamente con gli ombreggiatori a tassellatura
* [Engine] Arresto anomalo durante la creazione di un&#39;istanza di un file sbsar specifico
* [Engine] Le funzioni Sizelog2 / pow2 non funzionano correttamente
* [Engine] L’opzione &quot;set&quot; (Imposta) nella dimensione di output non funziona
* Il Livello mipmap [Engine] non è bloccato per valori negativi
* [Content] Impossibile pubblicare un grafico contenente un filtro triplo

### 5.2.1

*(Rilasciato il 27 agosto 2015)*

**Corretto:**

* [Grafico] Arresto anomalo durante l’elaborazione di una sbsar specifica
* [Grafico] Arresto anomalo durante la creazione di un’istanza di fxmap con più input di immagine
* [Engine] Arresto anomalo con sizelog2
* [Engine] Il valore predefinito del parametro esposto viene ignorato con il motore DX10
* [Library] Il calcolo delle miniature è interrotto quando il progetto contiene un alias non valido
* [Cooking] Impostate &quot;unknown\_parameter&quot; e &quot;duplicated parameter&quot; come avvertenza invece di errori
* [Preferenze] Il limite di cache del motore è bloccato a 4095 Mb
* [Function] l&#39;etichetta del parametro di input viene interpretata come identificatore

### 5.2.0

*(Rilasciato il 18 agosto 2015)*

**Aggiunto:**

* [Libreria] Aggiungi un’opzione nelle preferenze per nascondere/visualizzare i livelli PSD
* [Parametri] Consenti dati utente su più righe
* [Grafico] Aggiungi un’opzione di preferenza per eseguire il rendering dei commenti a dimensioni costanti
* [Grafico] Aggiungere un&#39;opzione di preferenza per disattivare la visualizzazione di nuovi nodi nella vista 2D
* [Prestazioni] Le prestazioni del processore pixel aumentano con il motore DX10
* [Vista 3D] Aggiungere tassellatura agli shader PBR
* [Vista 3D] Aggiungi opacità semplice agli shader PBR (nessun ordinamento dei volti)
* [Content] Aggiungi le destinazioni Vray/Corona/Redshift/Arnold al filtro di conversione PBR (per convertire le mappe per questi renderer)
* [Content] Aggiungi la tecnica &quot;Detail Oriented&quot; al filtro di combinazione Normale

**Corretto:**

* Arresto anomalo all&#39;apertura di sbs con dipendenza vuota
* Il collegamento ai livelli PSD viene interrotto dopo il ricaricamento del pacchetto
* [Funzioni] Funzioni nidificate interrompono la sicurezza del tipo
* [Funzioni] Le etichette, i gruppi e le descrizioni non vengono visualizzati
* [Funzioni] Arresto anomalo quando si copia/incolla da una funzione eliminata
* [Grafico] Collegamento materiale interrotto con grafici a barre
* [Grafico] La creazione di più nodi bitmap dalle risorse rende il nodo sovrapposto tra loro
* [Grafico] elemento commento non creato nella posizione corretta quando è figlio di un nodo
* [Grafico] Selezione area blocco commenti lunghi
* [Panettieri] Mappa normale dello spazio tangente rende nero su Mac
* [Parametri] Visibile Se non funziona quando il nome di input contiene &quot;-&quot;
* [Parametri] Valore passo in Parametri di input ignorato se inferiore a 0,01
* [Library] Il tag &quot;Visible in library&quot; non viene preso in considerazione per sbsar

### 5.1.1

*(Rilasciato il 4 giugno 2015)*

**Aggiunto:**

* [Grafico] Riduzione dello spazio tra due nodi quando si utilizza la connessione automatica
* [Grafico] Disattiva la connessione automatica quando si utilizza il trascinamento nel grafico
* [Grafico] Far sì che la cornice si agganci sulla griglia
* [Grafico] Disattiva inserimento nodo sopra/su collegamento selezionato per collegamento materiale
* [Preferenze] Imposta il valore massimo per Dimensione massima texture su 8192
* [Content] Aggiungi opzioni di simmetria al nodo &quot;Trasformazione sicura&quot;

**Corretto:**

* [Grafico] Il nuovo nodo non è allineato sulla griglia
* [Grafico] Lo scambio di collegamenti può generare loop/arresti anomali
* [Grafico] Problema di visualizzazione quando le dimensioni del nodo e gli intervalli sono disattivati
* [Panettieri] Arresto anomalo durante la cottura in forno in una risorsa che utilizza lo stesso nome della scena
* [Bakers] Il nome della risorsa predefinito non viene ricavato dal file di progetto corretto
* [Engine] Problema di funzione Pow2/log
* [Engine] Errore nella valutazione della funzione
* [Fxmaps] Arresto anomalo quando si ripristina il parametro ai valori predefiniti
* [FxMaps] Valutazione della funzione non valida
* [Preferenze] Facendo clic sulla scheda del progetto si arresta in modo anomalo SD
* [Vista 3D] L’utilizzo personalizzato viene convertito in lettere minuscole
* [Parametri] Impossibile riordinare gli elementi negli elenchi a discesa
* [Explorer] Arresto anomalo durante lo spostamento di un grafico delle funzioni in Esplora risorse

### 5.1.0

*(Rilasciato il 28 maggio 2015)*

**Aggiunto:**

* [Grafico] Cerca/visualizza il contenuto dalla libreria tramite il menu della barra spaziatrice
* [Grafico] Visualizza/apre il nodo appena creato
* [Grafico] reindirizzamento collegamenti (alt+maiusc)
* [Grafico] seleziona nodi principali
* [Grafico] Scambia 2 collegamenti (X)
* [Grafico] Inserire un nodo su un collegamento mediante trascinamento
* [Grafico] Crea un grafico da una selezione di nodi
* [Grafico] Elimina collegamento quando si utilizza Alt + LMB su una puntina del nodo
* [Grafico] Non connettere il nuovo nodo al precedente utilizzando Maiusc
* [Grafico] Aggiungi una barra degli strumenti per i filtri di base
* [Grafico] Migliorare la griglia (aggancio e risoluzione)
* [Grafico] Spostare il commento/fotogramma/puntina nel menu di scelta rapida
* [Grafico] Crea un nodo su un collegamento selezionato
* [Grafico] Aggiungere icone alle voci di funzione
* [Grafico] Modificare i colori dei perni nel grafico delle funzioni
* [Grafico] Usa Maiusc per disabilitare la connessione automatica del nodo
* [Grafico] Fare in modo che il collegamento selezionato venga disegnato sopra gli altri collegamenti
* [Grafico] Aggiungere icone ai nodi Fxmap
* [Grafico] Aggiungi un interruttore per disegnare collegamenti curvi o rettangolari
* [Funzione] Rendi più distinto il diverso tipo di vettore nel grafico delle funzioni (colori pin/link)
* [Funzioni] Aggiungi icone sui nodi e visualizza valori per costante / set / get
* [Funzioni] Aggiungere colori al titolo del nodo
* [Funzione] Migliorare le prestazioni per la valutazione delle funzioni (utilizzare il codice generato dall&#39;SSE)
* [Function] Visualizza un avviso se il nodo Set/Get è vuoto
* [Bakers]&#x200B;[Grafico] Dithering bitmap durante la conversione in 8 bpc
* [Bakers] Media delle normali dei vertici nel file OBJ se la trama non contiene alcun valore
* [Bakers] Corrispondenza per nome: usa il suffisso come separatore
* [Parametri] Aggiungi l’opzione per passare da RGB a HSV nel widget colore
* [Parametri] Pulsante Aggiungi contagocce nel widget colore
* [Libreria] Aggiungi una categoria per il contenuto di base (nodi di composizione, fxmap, funzione...)
* [Vista 2D] Informazioni: aggiungi visualizzazione in [0, 1] intervallo e HSV
* [Vista 3D] Aggiunta del supporto mipmap per l&#39;ambiente
* [Dipendenze] Pulisci le dipendenze inutilizzate con il programma di aggiornamento
* [Updater] Non salvare automaticamente i pacchetti

**Corretto:**

* [Arresto anomalo] alla chiusura del pacchetto
* [Arresto anomalo] quando si apre gestione dipendenze su un pacchetto non salvato
* [Arresto anomalo] Esempio di bug colore
* [Motore] deadlock dell&#39;area di distribuzione FxMap
* [Engine] problema di precisione con il motore SSE con sfocatura e/o nodo di fusione
* [Engine] Il calcolo non si arresta quando viene diviso per 0
* [Explorer] arresto anomalo durante l&#39;esportazione di un pacchetto con dipendenza se contiene cicli di dipendenza
* [Esplora risorse] Il trascinamento delle risorse spesso non funziona
* [Panettieri] La normale cotta è resa nera se è superiore a 256\*256
* [Bakers] Il salvataggio di un pacchetto nella stessa posizione del percorso di esportazione interrompe il percorso
* [Bakers] Percorso di destinazione predefinito errato quando il pacchetto non è ancora stato salvato
* [Engine] Risultato pixelsize errato quando ereditato dalla funzione padre
* [Dipendenze] La dipendenza non utilizzata non viene rimossa
* [Dipendenze] arresto anomalo all&#39;apertura della finestra delle dipendenze del pacchetto che contiene i cicli del pacchetto
* [Grafico] la selezione della selezione viene ridimensionata in funzione dello zoom
* Il collegamento [Grafico] non &quot;scatta&quot; all&#39;input/output più vicino
* [Grafico] Stack di annullamento errato (potrebbe generare arresti anomali)
* [Grafico] La connessione multipla con Ctrl non funziona se il pin è già collegato
* [Vista 3D] Il colore della griglia è influenzato dal colore di sfondo
* [Vista 3D]&#x200B;[Grafico] il nodo di output contenente più utilizzi non viene inviato correttamente alla vista 3D
* [Vista 3D] Tasselation shader : bug di compilazione nelle GPU AMD
* [Vista 2D] Problema di sistema del pin
* [Funzioni] Bug di compilazione delle funzioni (in caso contrario)
* [Preferenze] suffisso alto/basso non letto correttamente da sbsprj
* [Libreria] Se trascini una cartella su un’altra, la rimuovi
* [Windows] È possibile eseguire più sessioni di SD
* [Licenza] La vecchia licenza non viene mantenuta
* [Content] Problema con il filtro Edge Detect

### 5.0.3

*(Rilasciato: 01 aprile 2015)*

**Aggiunto:**

* [Preferences]&#x200B;[Bakers] Aggiungete un’opzione per calcolare la tabulazione per vertice o pixel in modo che corrisponda all’UE4
* [Libreria] Usa filtro bilineare per le miniature
* [Pannelli] Consente il ridimensionamento della finestra a meno di 800 px al height
* [3DView] Equalizza l&#39;esposizione della mappa dell&#39;ambiente / normalizza la rotazione per ottenere un fulmine uniforme
* Collegamento all&#39;applicazione Nome con versione principale

**Corretto:**

* [Grafico] Arresto anomalo quando si eliminano alcuni nodi fantasma
* [Grafico] il nodo ancorato rimane ancorato durante la duplicazione del nodo
* [Grafico] Arresto anomalo durante l&#39;eliminazione dei nodi
* [Grafico] Le impostazioni per gli output di esportazione non sono memorizzate per grafico
* [Grafico] Stato di ancoraggio del nodo non valido durante l&#39;eliminazione del nodo
* [Bakers] Gli errori non vengono più visualizzati in una finestra di dialogo
* [Panettieri] La risorsa mancante non viene visualizzata come mancante nella finestra di cottura
* La finestra [Pubblicazione] non riuscita non deve essere modificabile
* [Pubblicazione] Sbsar Risultato non corretto
* [Vista 3D] I materiali multipli delle trame FBX aggiornate non vengono ricaricati correttamente
* [Vista 3D] In alcuni casi, la SH diffusa può produrre valori negativi negli shader PBR
* [Vista 2D] La profondità di bit visualizzata per le immagini delle risorse è sempre di 8 bpc
* [Parametri] I parametri non vengono sempre visualizzati nelle proprietà del grafico
* [Menu] &quot;Esporta file di registro...&quot; azione non gestire per individuare il file log.txt
* [Batchtools] Errore subsmutator
* [Explorer] Il caricamento dei pacchetti mantiene l&#39;evidenziazione
* [Proprietà] Arresto anomalo durante la cancellazione di una funzione su un parametro enum
* [Preferenze] Il plug-in dello spazio tangente Mikkt non è impostato sull&#39;impostazione predefinita in utente\_progetto
* [Valutazione/Attivazione] Impossibile valutare/attivare online su Windows
* Elaborazione della barra di stato: sposta l&#39;interfaccia durante l&#39;aggiornamento
* Avvia più SD contemporaneamente
* Aggiorna URL lettore quando .exe non viene trovato
* La modifica dei file sul disco non è stata rilevata correttamente

### 5.0.2

*(Rilasciato il 17 marzo 2015)*

**Aggiunto:**

* [Libreria] Aggiungi il controllo normale nel materiale\_adjustment\_blend
* [Libreria] Aggiungi opzione di fusione per normale nel materiale\_color\_blend
* Aggiornamento a Qt 5.4.1

**Corretto:**

* [Arresto anomalo] OSX 10.9 e 10.10 in FreeImage
* [Arresto anomalo] Quando si apre un file fbx che contiene elementi senza vertici
* [Grafico] Problemi di trascinamento
* [Grafico] La scelta rapida Cancella cache è interrotta
* [Grafico] TGA appare nero/trasparente in SD
* [Library] Input normale scala di grigi triplanare errato
* [Library] Il nodo di rilevamento di Edge non funziona correttamente con il motore della CPU
* [Parametri] Intervallo del cursore non corretto per float2/3/4
* [Parametri] Se si esegue &quot;Esporta parametri&quot; due volte, Designer si arresta in modo anomalo
* [Console] non è ridimensionato correttamente
* [Console] Duplicazione nell&#39;elenco dei canali: View3D e 3DView
* [3DView] L&#39;ordine dei parametri definito in glslfx non viene mantenuto nella GUI
* [Esplora risorse] Arresto anomalo durante l’aggiornamento delle texture mancanti sul disco
* [Funzione] Modifica del valore e modifica causa l’arresto anomalo
* [Baker] Arresto anomalo quando si apre la finestra di cottura su una risorsa 3D mancante
* [PSD] Arresto anomalo di Psdparse (MSVCR120.dll mancante)
* [Informazioni sulla finestra] Interruzione di riga mancante con la versione di Steam
* [Sbs] Nuove funzioni inutilizzate del motore in sbs
* [Sbsar] Nuove funzioni non supportate in SD
* [Interfaccia] La barra di avanzamento non viene cancellata al termine di un&#39;esportazione con dipendenze
* vcomp100.dll non trovato quando si avvia SD su un Windows 7 appena installato

**Problemi noti:**

* [Windows 8] Il trascinamento non funziona al primo avvio. Riavviare SD per risolvere il problema.

### 5.0.1

*(Rilasciato il 5 marzo 2015)*

**Corretto:**

* È stato corretto un bug durante l’esportazione di bitmap in Windows.

### 5.0.0

*(Rilasciato il 4 marzo 2015)*

**Aggiunto:**

* [Esporta] elimina il canale di Alpha per TGA e BMP quando è completamente opaco
* [Vista 3d] Impostare lo shader PBR per impostazione predefinita
* [Vista 2D] Passa alla visualizzazione dell&#39;immagine come alfa premoltiplicata
* [Parametri] Dimensione: Aggiungi un blocco di larghezza/Height / valori di visualizzazione negli elenchi a discesa
* [Dipendenze] Nuovo gestore dipendenze
* [Dipendenze] visualizza/trova l&#39;istanza del nodo corrispondente a una dipendenza
* [Dipendenza] Aprire un pacchetto di dipendenze in Esplora pacchetti
* [Engine] Fusione: supporta il parametro Opacità quando viene utilizzata una maschera
* [Engine] Fusione: Aggiungi nuovi metodi di fusione (sovrapposizione, schermo, softlight, divisione)
* [Engine] Fusione: supporta la fusione alfa retta
* [Motivo] Nuovo nodo Sfumatura dinamica
* [Engine] Nuovo nodo Distanza
* [Engine] Nuovo nodo Pixel Processor
* [Engine] Fxmap: supporta la funzione dinamica per le immagini di input
* [Engine] Funzione Sampler: supporto del campionamento bilineare
* [Engine] Fxmap: supporta il filtro bilineare/più vicino per le immagini di input
* [Engine] Fxmap: supporta l&#39;immagine di input dritta/premoltiplicata alfa
* [Pannelli] Aggiungete un&#39;opzione per abbinare la geometria in base al nome della trama tra trame a bassa e ad alta definizione
* [Modelli] Creazione di una sostanza modello per Substance Painter
* [Panettieri] Nuova mappa texture da panettiere
* [Grafico] Aggiungere una &quot;verifica di compatibilità&quot; per evidenziare i nodi non compatibili con il motore precedente
* [UI] Regolazioni del menu Aiuto
* [Preferenze] impostate il plug-in Mikkt Tangent Space come predefinito (ripristinate le preferenze predefinite se è installato SD4)
* [Library] Aggiungi nuove mappe hdr
* Nuova Substance da modello
* Passa a Qt5
* Aggiornamento del sistema di licenze a SD5

**Corretto:**

* [Solo Mac] Problema del selettore colore con lo schermo della retina
* [Solo Mac] Anche trascinando sulla vista 3D in Mac OS si ruota la vista
* [Bakers] Se si esegue il baking di una mappa senza una cartella di output, si ottiene una texture vuota
* [Grafico] I nodi ancorati nella cornice si spostano in modo strano
* [Parametri] Percorso libreria personalizzato non caricato dai file sbsprj
* [Vista 3D] CTRL+R per ricaricare tutti gli shader attiva anche la reimpostazione della vista 3D
* [Vista 3D] Inv. Mipmap height uniforme passa all&#39;impostazione predefinita durante il caricamento dello shader
* [Vista 3D] Shader PBR : tipo diffuso rispetto a baseColor
* [Library] I percorsi libreria non ricorsivi interrompono le texture collegate nei pacchetti
* [Library] Mappe ambiente non visualizza .hdr
* [Explorer] &quot;Copia/Incolla&quot; sulla sostanza non dovrebbe essere possibile
* [Explorer] Fare clic con il pulsante destro del mouse sull&#39;opzione &quot;Incolla&quot; ancora disponibile su un grafico
* Descrizione comando [Function] del campionatore errata
* [Grafico] In modalità compatta, le istanze non mostrano tutti i nomi dei collegamenti quando vengono espanse automaticamente per aggiungere un convertitore in scala di grigi
