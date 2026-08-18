---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/preferences-window.html"
breadcrumb-title: ''
description: Accedete alla finestra Preferenze di Substance 3D Designer per personalizzare le impostazioni e il comportamento dell’applicazione.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Preferenze
user-guide-description: ''
user-guide-title: ''
source-git-commit: b1b28e909a4d3c19c1dbc28e5ed25b3adc327ac3
workflow-type: tm+mt
source-wordcount: '2030'
ht-degree: 1%

---


# Finestra Preferenze

![Finestra Preferenze](../../assets/image2021-6-22-20-56-1.png "Finestra Preferenze")

Questa pagina presenta la finestra <b>Preferenze</b> e tutte le relative impostazioni.

Puoi trovare la finestra Preferenze nel menu <b>Modifica</b> nella barra superiore principale dell&#39;applicazione. Questa finestra di dialogo consente di regolare diverse impostazioni. È organizzato in schede che coprono diverse aree di comportamento e funzionalità.\
Ti consigliamo di rivedere tutte queste impostazioni per comprendere meglio come funziona l’applicazione e come può essere adattata al tuo flusso di lavoro.

>[!NOTE]
>
> Per ulteriori informazioni su come archiviare queste preferenze e su come integrarle in un ambiente di produzione, è possibile fare riferimento alla pagina [Preferenze utente - Automazione dell&#39;installazione](../../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) della documentazione.

## Generale

### Documenti recenti

|  |  |
| --- | --- |
| <b>L&#39;elenco dei documenti recenti contiene</b>  *Impostazione predefinita: 10* | Ciò consente di selezionare il numero di documenti da elencare nella voce <b>Pacchetti recenti</b> dell&#39;elemento <b>File</b> nel [menu principale](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html). |

### Cronologia

|  |  |
| --- | --- |
| **Dimensione stack cronologia** *Impostazione predefinita: 200* | Indica il numero di operazioni di annullamento disponibili in un dato momento nell&#39;elemento <b>Modifica > Annulla</b> del [menu principale](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html).  **Attenzione:** maggiori sono le operazioni di annullamento necessarie, maggiore sarà la quantità di memoria richiesta dall&#39;applicazione. |

### Lingua

|  |  |
| --- | --- |
| **Scegliere la lingua dell&#39;applicazione** *Impostazione predefinita: System* | Questa impostazione definisce la lingua utilizzata nell&#39;interfaccia dell&#39;applicazione. L&#39;opzione &#39;*Sistema*&#39; rileva automaticamente la lingua dalle impostazioni della lingua di sistema. Le lingue disponibili sono elencate in [Requisiti di sistema](../../getting-started/system-requirements/system-requirements.md).  **Nota:** la modifica di questa impostazione avrà effetto solo dopo il riavvio dell&#39;applicazione. |

### Viste

|  |  |
| --- | --- |
| <b>Inverti zoom nelle visualizzazioni</b>  *Impostazione predefinita: deselezionata* | Se selezionata, i controlli di zoom verranno invertiti nelle [viste 2D](../../interface/2d-view/2d-view.md), [viste 3D](../../interface/3d-view/3d-view.md) e [grafiche](../../interface/the-graph-view/the-graph-view.md). |

### Percorsi

|  |  |
| --- | --- |
| <b>Salva/Esporta percorso</b>  *Impostazione predefinita: ultimo percorso* | Determina se il percorso di salvataggio/esportazione suggerito è l&#39;ultimo percorso selezionato o il percorso del [pacchetto SBS](../../getting-started/overview/overview.md). L’ultimo percorso selezionato viene salvato tra le sessioni. |
| <b>Cartella temporanea</b>  *Impostazione predefinita: percorso a seconda del sistema operativo di sistema* | Quando i dati immagine di un grafico superano il pool di memoria allocato (vedere di seguito <b>Memoria > Cache immagini</b>), i dati in overflow vengono scritti sul disco. Questa impostazione consente di definire la posizione in cui vengono scritti i dati della cache delle immagini in overflow.   Questa posizione viene utilizzata anche per archiviare una copia del pacchetto SBS attualmente aperto con le ultime modifiche dall&#39;ultimo salvataggio manuale. |

### Memoria

#### Cache immagini

L&#39;applicazione mantiene nella cache una *immagine non compressa ad alta risoluzione* per ogni nodo sottoposto a rendering nel grafico corrente.\
I nodi di istanza genereranno queste immagini per tutti i nodi del grafico a cui fanno riferimento e le elimineranno una volta calcolati i relativi [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). Solo gli output vengono mantenuti in memoria in quel punto.

Potete impostare la dimensione massima della cache allocata alle miniature e alle immagini nella memoria di sistema e verificare l&#39;utilizzo corrente. Se i dati della cache superano il pool allocato, i dati in eccesso vengono scritti nella <b>cartella temporanea</b> (vedere sopra <b>Percorsi > cartella temporanea</b>).

|  |  |
| --- | --- |
| <b>Budget memoria</b>  *Predefinito: Automatico* | Questa allocazione viene calcolata automaticamente su circa il 75% del pool totale di memoria di sistema. Per impostare questo valore manualmente, selezionare l&#39;opzione &#39;*Personalizzato*&#39; e impostare un valore nel campo di input adiacente. |

Si noti che la scrittura su disco è *più lenta* rispetto alla scrittura nella memoria di sistema. Di conseguenza, il tempo di rendering del grafico *aumenterà in modo esponenziale* poiché i dati in overflow devono essere scritti nella cartella temporanea.\
Per evitare che ciò accada, si consiglia di esaminare i suggerimenti per la riduzione dell&#39;ingombro di memoria di un grafico nella sezione [Linee guida per l&#39;ottimizzazione delle prestazioni](../../best-practices/performance-optimization/performance-optimization-guidelines.md) della documentazione.

#### Pianificazione lavori

Durante attività specifiche, ad esempio le conversioni delle immagini per le miniature o la [vista 2D](../../interface/2d-view/2d-view.md), verranno creati e distribuiti processi separati tra i core di elaborazione del sistema per una maggiore efficienza. Ogni processo scriverà i dati nella memoria di sistema per eseguire le operazioni.\
Questa impostazione consente di definire il pool di memoria allocato per *tutti i processi simultanei*. Quando questo pool viene utilizzato completamente, i nuovi processi verranno accodati fino al completamento di quelli correnti.

|  |  |
| --- | --- |
| <b>Budget memoria</b>  *Predefinito: Automatico* | Questa allocazione viene calcolata automaticamente su circa il 10% del pool di memoria di sistema totale. Per impostare questo valore manualmente, selezionare l&#39;opzione &#39;*Personalizzato*&#39; e impostare un valore nel campo di input adiacente. |

### Interfaccia utente

|  |  |
| --- | --- |
| **Disattiva valore DPI alto** *Impostazione predefinita: deselezionata* | La modalità <b>High DPI</b> manterrà un ridimensionamento coerente del testo e degli elementi dell&#39;interfaccia utente *indipendentemente* dalle impostazioni di visualizzazione e ridimensionamento del sistema.   Disattivando (ad esempio, la casella di controllo *compilata*) questa impostazione consente di ridimensionare l&#39;interfaccia, il che risulta in un testo più grande e più leggibile su alcuni schermi, ma può anche creare incongruenze nelle dimensioni del testo, oltre ad altri problemi di layout.  **Attenzione:** Designer acquisisce la scala specifica degli elementi dell&#39;interfaccia utente *dal sistema operativo*. Pertanto, qualsiasi regolazione del ridimensionamento dell&#39;interfaccia utente deve essere effettuata nelle impostazioni di visualizzazione del sistema operativo. Per garantire che le impostazioni di visualizzazione vengano applicate correttamente in Designer, *esci* dalla sessione utente del sistema operativo ed effettua nuovamente l&#39;accesso dopo aver modificato queste impostazioni.  **Nota:** la modifica di questa impostazione avrà effetto solo dopo il riavvio dell&#39;applicazione. |

### Backup automatico

Per impostazione predefinita è inclusa una funzione di salvataggio automatico che crea copie dello stato corrente dei [pacchetti SBS](https://docs.substance3d.com/display/DRAFTDESIGNER/.Overview+vDraftVersion) aperti in periodi di tempo impostati. I salvataggi automatici si trovano in una cartella <b>.autosave</b> nel percorso del pacchetto SBS.

|  |  |
| --- | --- |
| <b>Backup automatico ogni # minuti</b>  *Impostazione predefinita: 5* | Periodo di tempo tra ogni salvataggio automatico. |
| <b>Mantieni fino a # versioni</b>  *Impostazione predefinita: 6* | Numero massimo di salvataggi automatici da mantenere in un determinato momento. |

Quando viene raggiunta la quantità massima di versioni, i backup più recenti elimineranno quelli meno recenti.\
Si noti inoltre che i salvataggi automatici devono essere aperti *dopo averli spostati* nel percorso del pacchetto SBS originale. *non* devono essere aperti nella posizione corrente.

### Pubblicazione e invio di file SBSAR

|  |  |
| --- | --- |
| <b>Salva sempre il file .sbs durante la pubblicazione in .sbsar o l&#39;invio a un&#39;altra applicazione</b>  *Impostazione predefinita: True* | Controlla il salvataggio automatico del pacchetto SBS durante la [pubblicazione](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) o l&#39;invio a un&#39;altra applicazione[&#128279;](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html). |

### Cooker

|  |  |
| --- | --- |
| <b>Limite dimensione cottura</b>  *Impostazione predefinita: 8192 pixel* | Definisce la risoluzione pixel massima consentita per tutti i [nodi](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/nodes-reference-129368078.html) in qualsiasi [grafico](../../compositing-graphs/substance-compositing-graphs.md). Poiché gli output dei grafici sono sempre immagini quadrate con risoluzioni di potenze di 2, il valore qui impostato definisce sia la larghezza massima che il height in pixel. |

### Motore

|  |  |
| --- | --- |
| <b>Limite cache GPU</b>  *Impostazione predefinita: 2048 MB* | Questa impostazione consente di definire la quantità di memoria da riservare alla memorizzazione nella cache delle fasi di rendering. In genere, la Substance Engine memorizza nella cache l&#39;output di ogni nodo in un grafico a Substance. |

>[!NOTE]
>
> Si consiglia di esaminare i suggerimenti per ridurre l&#39;ingombro di memoria di un grafico nella sezione [Linee guida per l&#39;ottimizzazione delle prestazioni](../../best-practices/performance-optimization/performance-optimization-guidelines.md) della documentazione.

## Progetti

Consultare la pagina [Impostazioni progetti](../../interface/preferences-window/project-settings/project-settings.md).

## Grafico

### Comune

|  |  |
| --- | --- |
| <b>Il tasto Tab mostra il menu del nodo</b>  *Impostazione predefinita: selezionata* | Se questa opzione è selezionata, il tasto &#39;Tab&#39; aprirà il menu <b>Nodo</b>, replicando la funzionalità del tasto &#39;Space&#39;. |
| <b>Abilita la creazione di nodi mediante il trascinamento di connettori</b>  *Impostazione predefinita: selezionata* | Se selezionata, quando fai clic su un connettore, trascina il cursore e rilascia il collegamento creato nello spazio vuoto del grafico per visualizzare il <b>menu Nodo</b>.   Il menu verrà inoltre *filtrato* in base al tipo di connettore su cui si è fatto clic. Ciò significa che verranno visualizzati solo i nodi compatibili con il connettore selezionato. |
| <b>Visualizzare gli output nella vista 3D all’apertura di un grafico</b>  *Impostazione predefinita: selezionata* | Se questa opzione è selezionata, tutti gli output del grafico vengono applicati automaticamente nella [vista 3D](../../interface/3d-view/3d-view.md) quando il grafico viene aperto.   In questo modo viene eseguito anche il rendering di tutti i nodi che fanno parte di un flusso che conduce a un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |

### Grafici di composizione Substance

|  |  |
| --- | --- |
| <b>Calcolo automatico delle miniature di tutti i nodi all&#39;apertura di un grafico</b>  *Impostazione predefinita: selezionata* | Se selezionata, durante il caricamento del grafico viene eseguito automaticamente il rendering di tutte le miniature dei nodi. |
| <b>Visualizzare l&#39;output nella vista 2D all&#39;apertura di un grafico</b>  *Impostazione predefinita: selezionata* | Se questa opzione è selezionata, il primo output del grafico viene visualizzato automaticamente nella [vista 2D](../../interface/2d-view/2d-view.md) quando il grafico viene aperto. In questo modo viene eseguito anche il rendering di tutti i nodi che fanno parte di un flusso che conduce al nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md). |
| <b>Visualizza automaticamente il nodo di composizione appena creato</b>  *Impostazione predefinita: selezionata* | Se questa opzione è selezionata, la [vista 2D](../../interface/2d-view/2d-view.md) verrà aggiornata automaticamente per visualizzare l&#39;output di un nodo appena creato. |
| <b>Inserire automaticamente il nodo di conversione colore/scala di grigi</b>  *Impostazione predefinita: deselezionata* | Se selezionata, risolvi automaticamente le mancate corrispondenze dei tipi di connessione a colori/scala di grigi *posizionando nodi specifici* per eseguire la conversione appropriata.   Quando un output *Scala di grigio* (connettore grigio) è collegato a un input *Colore* (connettore giallo), tra i due connettori viene automaticamente inserito un nodo [Mappa sfumatura](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md).   Quando un output *Color* (connettore giallo) è collegato a un input *Grayscale* (connettore grigio), tra i due connettori viene automaticamente inserito un nodo [Conversione gradazioni di grigio](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/grayscale-conversion/grayscale-conversion.md). |
| <b>Abilita modifica grafico nel contesto</b>  *Impostazione predefinita: deselezionata* | Per impostazione predefinita, quando si apre un grafico a cui fa riferimento un [nodo di istanza](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) con un clic destro sul nodo e si seleziona <b>Riferimento aperto</b>, tale grafico viene caricato e modificato *in modalità isolamento*.   Se questa opzione è selezionata, è possibile modificare i grafici a cui fanno riferimento le istanze *utilizzando le informazioni passate nell&#39;istanza* dal grafico corrente. A tale scopo, fare clic con il pulsante destro del mouse su un nodo di istanza e selezionare <b>Apri riferimento nel contesto</b> oppure utilizzare la combinazione di tasti Ctrl+E.   Ciò significa che un grafico istanza può essere modificato nel contesto del grafico in cui viene creata l’istanza. Questa funzione è molto utile per visualizzare gli effetti delle modifiche sul grafico su cui si stava lavorando. Vedere l&#39;esempio riportato di seguito.  **Nota:** le schede <b>Anteprima</b> e <b>Predefiniti</b> sono *disabilitate* nelle [proprietà del grafico](../../compositing-graphs/graph-parameters/graph-parameters.md) quando si utilizza la modifica contestuale. |

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Modifica contestuale disabilitata](../../assets/substance3ddesigner_incontext_no.gif "Modifica contestuale disabilitata")

*Apri riferimento*

</td>
<td style="border: 0;" valign="top">

![Modifica contestuale abilitata](../../assets/substance3ddesigner_incontext_yes.gif "Modifica contestuale abilitata")

*Apri riferimento nel contesto*

</td>
</tr>
</table>

## Vista 3D

### Varie

|  |  |
| --- | --- |
| <b>Ambiente nascosto per impostazione predefinita</b>  *Impostazione predefinita: selezionata* | Determina l&#39;impostazione di visibilità predefinita [Ambiente](../../interface/3d-view/3d-view.md). Quando è nascosto, lo sfondo della vista 3D viene sostituito con un *colore in tinta unita*. |
| <b>Ridimensionamento del riquadro di visualizzazione</b>  *Predefinito: Automatico* | Controlla il ridimensionamento della risoluzione di rendering della vista 3D quando il sistema utilizza il ridimensionamento della visualizzazione.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Automatico</i>: la risoluzione di rendering si basa sulla risoluzione di visualizzazione <i>ridimensionata</i></li> <li data-preserve-html="true"><i>Nessuno</i>: la risoluzione di rendering si basa sulla risoluzione di visualizzazione <i>nativa</i></li> </ul> |

### OpenGL

|  |  |
| --- | --- |
| <b>Numero di campioni</b>  *Impostazione predefinita: 64* | Influisce sulle dimensioni della tabella di esempio degli ombreggiatori della vista 3D. Un valore più elevato determinerà un miglioramento della qualità dell&#39;immagine a scapito delle prestazioni.  **Nota:** anche la tabella di esempio degli shader è interessata dalla GPU e dal sistema operativo del sistema. |

## Baker

|  |  |
| --- | --- |
| <b>Raytracing GPU</b>  *Impostazione predefinita: selezionata* | Se selezionata, verrà eseguito il ray tracing sulla GPU per [panifici compatibili](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing).   I seguenti backend Raytracing GPU saranno i predefiniti, a seconda dell’architettura della GPU NVIDIA:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>DXR</i>: Turing e versioni successive</li> <li data-preserve-html="true"><i>Optix</i>: Pascal e Maxwell</li> </ul>  **Nota:** ulteriori informazioni sui prodotti da forno basati su GPU sono disponibili nella sezione [Raytracing GPU](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing) della documentazione [Substance Bakers](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home).  **Suggerimento:** è possibile utilizzare i seguenti *argomenti della riga di comando* quando si avvia l&#39;applicazione per *forzare* l&#39;utilizzo di un back-end di Raytracing GPU diverso: <ul data-preserve-html="true"> <li data-preserve-html="true"><code>—force-optix</code> : forzare l&#39;uso di Optix su Nvidia Turing o GPU più recenti</li> <li data-preserve-html="true"><code>—force-dxr</code> : forzare l&#39;uso di DXR sulle GPU Nvidia Pascal</li> </ul> |

## Libreria

|  |  |
| --- | --- |
| <b>Ricostruisci miniature</b> | L&#39;opzione attiverà una ricalcolo di tutte le miniature della [libreria](../../interface/the-library/the-library.md), che sostituirà automaticamente quelle precedenti. |

## Scelte rapide

Potete assegnare scelte rapide da tastiera personalizzate per creare nodi nei grafici.

È possibile assegnare scelte rapide per i nodi in tutti i tipi di grafici: [Substance grafici](../../compositing-graphs/substance-compositing-graphs.md), [Substance grafici di funzione](../../function-graphs/function-graphs.md) e [FX-Map grafici](../../function-graphs/fxmaps/fxmaps.md).

È possibile assegnare un collegamento a qualsiasi nodo, anche ai nodi di libreria personalizzati. Una stessa scelta rapida può essere assegnata a tipi di grafici diversi. Per impostazione predefinita non sono assegnate scelte rapide; puoi personalizzarle a tuo piacimento.

In caso di conflitto con un altro collegamento nodo o un collegamento programma incorporato, la voce verrà evidenziata e verrà visualizzato un avviso. La scelta rapida non avrà *alcun effetto* finché il conflitto non verrà risolto.

>[!IMPORTANT]
>
> Scelte rapide sostituite dai plug-in Python
> 
> Quando un plug-in Python definisce una scelta rapida da tastiera assegnata a un nodo, il plug-in la sovrascriverà. Questo significa che la chiave attiverà l&#39;azione del plug-in invece di creare un nodo.
> 
> Questo è già il caso delle chiavi H, S e V utilizzate dagli [strumenti di allineamento dei nodi](../../interface/the-graph-view/node-alignment-tools/node-alignment-tools.md).
