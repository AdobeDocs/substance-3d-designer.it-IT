---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-11-3.html"
breadcrumb-title: ''
description: Consulta le note sulla versione per Substance 3D Designer versione 11.3 per informazioni sulle nuove funzioni, i miglioramenti e le correzioni di bug.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 11.3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 1%

---


# Versione 11.3

**Substance 3D Designer**

Data di pubblicazione: *24 novembre 2021*

## Caratteristica principale

### Nuove funzionalità per grafici modello

![](../../assets/banner-model.jpg)

Sono stati aggiunti molti miglioramenti al grafico del modello per espandere le funzionalità di modellazione:

* <b>Nuovo flusso di lavoro particelle</b>\
  Il nuovo flusso di lavoro di modellazione delle particelle consente di creare nuvole di punti per manipolare la geometria. Possono essere utilizzati per creare molte nuove forme complesse e/o ripetitive come le piastrelle del tetto sull&#39;immagine appena sopra.\
  Per ulteriori informazioni sul nuovo flusso di lavoro delle particelle, consultate le seguenti pagine della documentazione:

  * Tipi di elementi in una scena
  * Particelle
  * Sfoltimento particelle
  * Particelle da istanze

  ![](../../assets/particle-pruning.gif)

* <b>Nuovi nodi di modellazione e deformazione</b>\
  Sono stati aggiunti nuovi nodi per creare forme più complesse. Fare clic su ogni nodo per ulteriori informazioni:
  * Trasformazione generativa
  * Pattern organico
  * Tornio
  * Taglio curva

* <b>Miglioramenti generali\
  </b>Il flusso di lavoro intorno al grafico di modellazione è stato migliorato con:
  * Nuovi suggerimenti sui parametri dei nodi per facilitarne l&#39;apprendimento.
  * La gerarchia dei modelli 3D viene ora mantenuta durante l’esportazione in FBX
  * L&#39;assegnazione dei materiali può essere esportata con i formati di file OBJ e FBX.
  * Visualizzare in anteprima i nodi intermedi nella finestra della vista in modalità di sovrapposizione.

### Migliore interoperabilità

![](../../assets/banner-sendto.jpg)

Le azioni send-o sono state ampliate, con due nuove possibilità:

* **Invia SBSM (file del modello Substance) a Stager**\
  I modelli 3D procedurali possono ora essere inviati a Stager e modificati da lì con i parametri esposti.

* **Ricezione SBS/SBSAR da Sampler**\
  Ora è possibile ricevere i file di Substance generati da Sampler direttamente in Designer.

### Varie

![](../../assets/banner-misc-3.jpg)

Sono stati apportati diversi miglioramenti alla qualità della vita:

* **Input relativi agli input**\
  Gli input del grafico impostati in Relativo agli input erediteranno ora la dimensione del nodo connesso invece di quella predefinita del grafico principale. Questo semplifica notevolmente la gestione delle diverse risoluzioni tramite input di dimensioni diverse.

  ![](../../assets/relative-to-inputs.jpg){width="400px"}

* **Nuova finestra del grafico**\
  La nuova finestra grafica è stata rielaborata e ora consente di visualizzare meglio i dettagli di un modello specifico e di creare un nuovo grafico direttamente in un pacchetto esistente.

  ![](../../assets/new-graph.png){width="400px"}

* **Chiudi tutti i pacchetti**\
  Una piccola azione che rende meno noiosa la gestione di molti pacchetti in Esplora risorse. Utilizza **File** > **Chiudi tutti** per chiudere tutti i pacchetti attualmente aperti.

  ![](../../assets/close-all-packages.png)

* **Ingrandisci visualizzazione corrente**\
  Utilizzate la nuova barra del titolo **icona** o la scelta rapida **MAIUSC+spazio** per espandere una finestra a schermo intero. Può essere utilizzato anche su finestre mobili.

* **Miglioramenti della vista 3D**\
  La vista 3D presenta nuove impostazioni di visualizzazione che consentono di attivare o disattivare la visualizzazione delle facce posteriori di un modello 3D, nonché la visualizzazione di vertici, tangenti e bitangenti.

### Contenuto

![](../../assets/render-content.jpg)

Questa versione aggiunge nuovi nodi di diffusione e miglioramenti per il nodo del PBR render:

* <b>Nodi di diffusione</b>\
  I nuovi nodi UV Diffusione colore, Scala di grigi diffusione e Diffusione consentono di generare sfumature di sanguinamento morbide basate su una maschera di input.

  ![](../../assets/diffusion-normal.jpg){width="230px"}

  ![](../../assets/diffusion-grayscale.jpg) ![](../../assets/diffusion-uv.jpg)

* **Nodo di PBR render migliorato**\
  Questo nodo presenta le seguenti modifiche:
  * Nuovo metodo UV cubico per la forma Sfera.
  * Nuovo supporto per la dispersione del sottosuolo.
  * L&#39;Anisotropia segue ora il modello Strand di Adobe (Material 5ASM).
  * L’illuminazione basata sulle immagini è stata migliorata con il supporto del campionamento di importanza.
  * L’illuminazione a emissione è stata migliorata con il supporto del campionamento di importanza.

## Note sulla versione

### 11.3.0

*(Rilasciato il 24 novembre 2021)*

**Aggiunto:**

* [Modelli Substance] Aggiungere descrizioni comandi per i parametri dei nodi
* [Modelli Substance] Consente di visualizzare in sovrapposizione nella finestra della vista 3D il risultato di un nodo intermedio
* [Modelli di Substance] Migliorare la visualizzazione della visualizzazione della base
* [Modelli Substance] Mantiene la gerarchia degli oggetti durante l&#39;esportazione di un grafico Modello Substance in .fbx
* [Modelli Substance] Supporto di più materiali nell&#39;esportazione FBX/OBJ dal grafico dei modelli Substance
* [Modelli Substance][Contenuto] Nodo particelle
* [Modelli di Substance][Contenuto] Nodo Trasformazione generativa
* [Modelli Substance][Contenuto] Nodo Pattern organico
* [Modelli Substance][Contenuto] Particelle dal nodo Istanze
* [Modelli di Substance][Contenuto] Nodo di potatura delle particelle
* [Modelli Substance][Contenuto] Nodo tornio
* [Modelli di Substance][Contenuto] Nodo shell
* [Modelli Substance][Contenuto] Nodo di proiezione
* [Modelli Substance][Contenuto] Nodo di rifilo curva
* [Modelli Substance][Contenuto] Aggiorna nodo Sampler curva
* [Modelli Substance][Contenuto] Aggiornamento del nodo Sampler mesh
* [Modelli di Substance][Contenuto] Aggiorna nodo variazione
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
* [UI][macOS] Layout di interfaccia predefinito non corretto dopo l&#39;avvio dell&#39;applicazione
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
