---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/release-notes/version-12-2.html"
breadcrumb-title: ''
description: Consulta le note sulla versione per Substance 3D Designer versione 12.2 per informazioni sulle nuove funzioni, i miglioramenti e le correzioni di bug.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 12.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 12.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: ba25885fb45039d7cbdc79af4792a1fa0f83564a
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# Versione 12.2

<b>Substance 3D Designer 12.2</b> offre il supporto nativo dei computer con chip Apple (M1), alcuni miglioramenti per i grafici dei modelli Substance e altri piccoli aggiornamenti. In questa pagina verranno descritti tutti i dettagli relativi a questa nuova versione.

Data di pubblicazione: *19 luglio 2022*

![](version-12-2.resources/final3.png)

## Funzioni principali

### Supporto nativo per chip Apple Silicon (M1)

La versione 12.2 di Designer è la prima con il supporto nativo completo dei nuovi computer Apple basati su chip M1. Anche se in precedenza Designer poteva essere eseguito tecnicamente sui dispositivi Apple Silicon, il supporto nativo ti offrirà un&#39;esperienza più veloce ed efficiente. Come si può vedere nell&#39;immagine seguente, il calcolo è *fino a due volte più veloce* con questa nuova versione su questi computer.

![](version-12-2.resources/ds-perf-applem1.png){width="600px"}

### Miglioramenti per i grafici dei modelli Substance

* <b>Suggerimenti sui nodi\
  </b>Non è sempre possibile spiegare le operazioni eseguite da un nodo solo con un&#39;icona e un titolo, per cui è ora disponibile una descrizione con *descrizione completa del nodo* quando si è nella libreria o nella vista Grafico. Ti aiuterà a trovare il nodo che stai cercando o a capire meglio quali sono le sue funzionalità. ![](version-12-2.resources/tootlipnode.png)

* <b>Scelte rapide per la creazione di nodi\
  </b>Per velocizzare la creazione dei nodi più utilizzati, è ora possibile definire scelte rapide personalizzate nelle Preferenze, come per gli altri tipi di grafici.![](version-12-2.resources/shorcuts.png)

* <b>Anteprima del nodo dal menu di scelta rapida del nodo\
  </b>Nell&#39;ultima versione è stata aggiunta la possibilità di visualizzare in anteprima un nodo nella vista 3D grazie a una scelta rapida da tastiera da tastiera (*MAIUSC + clic* su un nodo). Questa funzionalità è ora disponibile anche nel menu contestuale *nodo* per renderla più individuabile.

  ![](version-12-2.resources/previewnode.gif){width="600px"}
* <b>Ricerca basata sulla compatibilità dei nodi\
  </b>Quando si cerca un nodo dal menu del nodo (accessibile premendo *Barra spaziatrice* nella vista Grafico), i nodi vengono ora filtrati correttamente per visualizzare solo quelli *compatibili con quello attualmente selezionato* nel grafico. Consente di trovare rapidamente il nodo che si sta cercando.

### Varie

* <b>Miglioramenti ai vista 2D</b>\
  Nelle versioni precedenti era possibile visualizzare gli output del grafico nella vista 3D tramite il *menu contestuale* del grafico Substance, ma non era possibile visualizzare un output del grafico nella vista 2D. Questa opzione è stata aggiunta a questo menu, con un sottomenu che elenca tutti gli output del grafico da visualizzare nel vista 2D.\
  Anche il pulsante &quot;Visualizza output&quot; nella barra degli strumenti di vista 2D è stato aggiornato con una freccia rivolta verso il basso e una descrizione comandi per rendere più chiaro il suo comportamento.\
  Infine, l’opzione &quot;Visualizzazione automatica degli output del grafico durante il caricamento di un grafico&quot; nelle Preferenze è stata *divisa in due impostazioni separate* - rispettivamente per il vista 2D e il vista 3D - per consentire di controllare quale visualizzazione deve essere aperta e popolata automaticamente quando si carica un grafico.

* <b>Modello CLO</b>\
  Per migliorare l&#39;interoperabilità con il software CLO, è stato aggiunto un *nuovo modello dedicato*. Aggiungerà automaticamente al grafico tutti i *metadati* necessari per importare correttamente il materiale in CLO.

  ![](version-12-2.resources/clo.png){width="600px"}

* <b>Requisiti per la piattaforma di riferimento VFX</b>\
  Ogni anno, la piattaforma di riferimento VFX pubblica un elenco di strumenti e librerie di versioni da utilizzare in ogni software per il settore VFX al fine di ridurre al minimo le incompatibilità tra i software. Come al solito, *aggiorniamo tutte le nostre dipendenze* al fine di rispettare tutte queste raccomandazioni.

## Note sulla versione

### 12.2.0

*(Rilasciato il 19 luglio 2022)*

<b>Aggiunto:</b>

* [Apple] Supporto nativo per Apple Silicon (M1) (solo versione di Creative Cloud)
* [Grafico del modello Substance] Visualizza le descrizioni dei nodi nella vista Grafico
* [Grafico del modello Substance] Visualizza le descrizioni dei nodi nella libreria
* [Grafico del modello Substance] Aggiungi una voce di menu contestuale ai nodi di anteprima
* [Grafico del modello Substance] Consenti all&#39;utente di creare scelte rapide per la creazione di nodi
* [UI] Aggiungi l’opzione &quot;Visualizza output in vista 2D&quot; nel menu di scelta rapida del grafico a Substance
* [UI] Suddividi l’impostazione &quot;Visualizzazione automatica degli output&quot; in impostazioni specifiche per vista 2D/vista 3D
* [UI] Aggiungi freccia a discesa e descrizione comandi al pulsante &quot;Visualizza output&quot; nella barra degli strumenti di vista 2D
* [UI] Rimodellare e riordinare gli elementi nel pannello Informazioni di Esplora risorse
* [Gestione colore] Aggiungi gli spazi colore di esportazione &quot;Linear Adobe RGB (1998)&quot; e &quot;Adobe RGB (1998)&quot; per l&#39;esportazione di ACE
* [Gestione colore] Aggiungi spazio cromatico di lavoro &quot;Linear Adobe RGB (1998)&quot; per ACE Adobe
* [Gestione colore] Aggiungi supporto per display ICC OCIO
* [Gestione colore] Nascondi lo spazio colore di lavoro di Adobe RGB dalle preferenze ACE
* [Gestione colore] Migliorare la qualità delle LUT 3D eseguite i baking in modalità ACE
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

<b>Corretto:</b>

* [Modelli Substance] L&#39;intervallo rigido impostato sul parametro esposto viene salvato quando si annulla l&#39;esposizione
* [Modelli di Substance] L&#39;identificatore non è di facile utilizzo sui nodi costanti
* [Substance modelli] Miglioramento della ricerca in base alla compatibilità dei nodi
* [UI] L&#39;ordine del sottomenu &quot;Nuovo&quot; non è corretto per le risorse della cartella
* [UI] La dimensione predefinita della finestra principale è molto piccola
* [UI] Le barre degli strumenti non sono interessate dall’opzione &quot;Ripristina layout&quot;
* [UI] Griglia di trasparenza visibile sull&#39;icona della risorsa font in Esplora risorse
* [Cooker] I grafici delle Substance istanziati in un grafico MDL vengono sempre completamente ricostituiti
* [Grafico] Arresto anomalo quando si incolla un nodo copiato da un grafico con identificatore vuoto
* [MDL] Arresto anomalo durante la chiusura di un grafico MDL specifico
* [Prestazioni] L&#39;applicazione non risponde durante il caricamento di pacchetti di grandi dimensioni
* [Resources] Le risorse Scena 3D possono essere importate in un caso specifico
