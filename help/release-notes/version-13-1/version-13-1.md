---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/release-notes/version-13-1.html"
breadcrumb-title: ''
description: Consultate le note sulla versione per Substance 3D Designer versione 13.1 per informazioni sui miglioramenti del grafico dei nodi e sul supporto per l'esportazione di AxF.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 13.1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1289'
ht-degree: 1%

---


# Versione 13.1

<b>Substance 3D Designer 13.1</b> aggiunge molti miglioramenti alla qualità della vita del grafico dei nodi, principalmente per quanto riguarda i fotogrammi, per migliorare l&#39;esperienza di creazione del materiale. Inoltre, l&#39;esportazione AxF permette agli utenti di utilizzare il formato AxF con un workflow interoperabile.

*Data di pubblicazione: 12 dicembre 2023*

![Banner per Substance 3D Designer 13.1](version-13-1.resources/24-library-hero-1920x620.png "Banner per Substance 3D Designer 13.1")

## Miglioramenti per le cornici

Le cornici sono uno strumento obbligatorio per mantenere il grafico ben organizzato e leggibile. Ecco perché abbiamo deciso di rifinirla in questa nuova versione.

### Espandi automaticamente

Man mano che il grafico cresce, potrebbe essere necessario riorganizzare il contenuto delle cornici. I nodi potrebbero spostarsi per fare spazio ad aggiunte o potrebbe essere necessario spaziare di più i contenuti per promuovere la leggibilità. Per facilitare queste regolazioni, è ora possibile espandere automaticamente una cornice quando si spostano gli oggetti inclusi: tenete premuto <b>Maiusc</b> in qualsiasi punto mentre spostate un oggetto in modo che i bordi della cornice vengano regolati automaticamente per mantenere l&#39;oggetto entro i limiti.

![espansione automatica](version-13-1.resources/autoexpand.gif)

### Adatta dimensione a contenuto

Man mano che apportate le regolazioni nel grafico, una cornice potrebbe non essere più adattata correttamente al suo contenuto. Questo nuovo comando consente di regolare automaticamente la posizione e le dimensioni della cornice in modo che si adatti all’estensione del suo contenuto, con una spaziatura interna di una cella della griglia media. Se la cornice ha una descrizione, questa viene regolata in modo da utilizzare eventuale spazio vuoto accanto alla descrizione, se possibile.

![dimensioni_filtro](version-13-1.resources/fitsize.gif)

### Descrizioni migliorate

Il codice HTML consente ora di formattare il testo nella descrizione di una cornice. Questo vale anche per i commenti.

![testo RTF](version-13-1.resources/description-3.png)

### <b>...e molto altro!</b>

Sono state ripensate molte cose, come l&#39;appartenenza a regole più tolleranti, le zone di interazione per ridimensionare facilmente i fotogrammi, l&#39;aggancio di regole per non disallineare i nodi sulla griglia e l&#39;aspetto visivo per dare un po&#39; di freschezza. Per ulteriori informazioni, visitate la [documentazione](../../interface/the-graph-view/graph-items/frame/frame.md) dei frame.

## Miglioramenti della qualità della vita

* <b>Miglioramenti del menu Nodo: </b>per risparmiare tempo durante la ricerca del nodo necessario, è stato migliorato leggermente il menu Nodo. La ricerca è ora più indulgente e vi darà un risultato anche se non c&#39;è una corrispondenza perfetta. Inoltre, è ora possibile utilizzare la freccia su per accedere direttamente all&#39;ultimo elemento dell&#39;elenco.
* <b>Posizionamento dei nodi: </b>se desiderate disporre di un layout perfetto per il grafico, queste due piccole modifiche vi faranno piacere. Quando si copiano o incollano nodi da un grafico all&#39;altro, i nodi incollati vengono ora allineati alla griglia principale. E quando aggiungete un nodo su un collegamento lungo, questo verrà posizionato al centro della parte visibile del collegamento, in modo da renderlo visibile in ogni situazione.
* <b>Opzioni di visualizzazione 2D: </b>se si è un utente intensivo della [visualizzazione 2D](../../interface/2d-view/2d-view.md), si risparmierà tempo in quanto le opzioni &#39;Mostra scacchiera&#39;, &#39;Mantieni dimensione visualizzazione&#39;, &#39;Usa dimensioni fisiche&#39; e &#39;Mostra affiancamento&#39; sono ora salvate, quindi non è necessario impostarle nuovamente quando si crea una nuova visualizzazione 2D o anche quando si riavvia Designer.

## Esportazione AxF

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icona file AxF](version-13-1.resources/axf-file-icon.png "Icona file AxF")

</td>
<td width="100.00%" style="border: 0;" valign="top">

AxF è un formato di [X-Rite](https://www.xrite.com/axf). Consente di acquisire, archiviare, modificare e comunicare caratteristiche di materiale complesse utilizzando dati numerici durante il flusso di lavoro di progettazione digitale. Nelle versioni precedenti di Designer, era possibile [importare file AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) e quindi migliorare la suddivisione in porzioni o aggiungere effetti procedurali, ma in seguito si era vincolati a esportare le modifiche come un nuovo file .sbsar.

In questa nuova versione, viene introdotta la possibilità di modificare i materiali AxF in posizione, quindi [esportare le modifiche](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) come nuovo livello nel file AxF importato.

</td>
</tr>
</table>

![Esporta AxF](version-13-1.resources/exportaxf.gif)

## API

Infine, questa versione 13.1 continua a migliorare l’API Python aggiungendo altre due possibilità:

* <b> proprietà &#39;Visible if&#39;: </b>è ora possibile impostare questa proprietà per i parametri grafici, gli input e gli output.
* <b>Ordine dei grafici Input/Output:</b> utilizzare sdsbscompgraph::reorderGraphInput e sdsbscompgraph::reorderGraphOutput per organizzare i parametri in base alle esigenze.

>[!NOTE]
>
> Designer 13.1 è l’ultima versione principale basata su Qt5, le prossime versioni principali verranno aggiornate a Qt6. Potrebbe avere un impatto sui plug-in personalizzati.

## Note sulla versione

### 13.1.0

*(Rilasciato il 12 dicembre 2023)*

### Aggiunto

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
* [UX] Impostare l&#39;elenco dei menu Nodo su loopN
* [AxF] Supporto dell&#39;esportazione AxF
* [AxF] Disattiva AxF su Linux
* [API] Imposta la proprietà &quot;Visible if&quot; dei parametri del grafico, degli input e degli output utilizzando l’API Python
* [API] Imposta l’ordine di I/O del grafico utilizzando l’API Python
* [Dipendenze] Aggiorna Incremento a 1.80.0
* [Dipendenze] Aggiornare OpenSubdiv alla versione 3.5.x
* [Dipendenze] Aggiornate FBX SDK al 2020.3
* [Dipendenze] Aggiorna NGL in 1.35.0.20
* [Gestione colore] Aggiungi il supporto per i display ICC OCIO
* [Livelli] Aggiungi un modo per ripristinare l’istogramma
* [Python] Avvisa gli utenti se non è possibile importare QtForPython
* [Vista 2D] Salva lo stato delle opzioni di visualizzazione
* [Vista 3D] Tecnica Aggiungi posizione allo shader delle informazioni sulla trama
* [Esporta] Aggiungi un pulsante &quot;Salva impostazioni&quot; per salvare le modifiche alle opzioni di esportazione

### Correzioni

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

### PROBLEMI NOTI

* [AxF OpenGL Shader] Ward errato per distribuzione anisotropica
* [AxF OpenGL Shader] Rugosità predefinita errata
* [AxF OpenGL Shader] Rotazione base ombreggiatura errata
* [AxF OpenGL Shader] Raggio errato sotto emisfero rilevamento
* [AxF OpenGL Shader] Rilevamento contributo errato
* [AxF] I valori della mappa &quot;Colore Specular&quot; non sono corretti durante l&#39;esportazione
* [AxF] L’anteprima e le texture non vengono visualizzate correttamente nella finestra di dialogo &quot;Importa AxF&quot;
* [AxF] La proprietà &quot;cc no refraction&quot; non viene inserita correttamente nel modello da AxF a AxF
