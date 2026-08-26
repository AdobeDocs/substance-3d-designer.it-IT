---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/preferences-window/project-settings.html"
breadcrumb-title: ''
description: Configura le impostazioni del progetto nelle preferenze di Substance 3D Designer per personalizzare il comportamento predefinito del progetto.
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Project settings
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Impostazioni progetto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '2687'
ht-degree: 1%

---


# Impostazioni progetto

Questa pagina presenta le <b>impostazioni dei progetti</b> in [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) e le impostazioni contenute in.

Substance 3D Designer consente di creare preferenze *per progetto* e di condividerle tra le workstation. Queste preferenze sono disponibili nella scheda <b>Progetti</b> della finestra [Preferenze](../../../interface/preferences-window/preferences-window.md).

Questo è molto utile se desideri configurare un ambiente di lavoro comune per un team che lavora sullo stesso progetto, utilizzando lo *stesso* file di progetto su *tutti* i sistemi.

>[!NOTE]
>
> Per ulteriori informazioni sulla configurazione e l&#39;integrazione di Substance 3D Designer in una **pipeline di produzione**, *consigliamo vivamente* facendo riferimento alla sezione [Configurazione della pipeline e del progetto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) della documentazione.

![Impostazioni progetto](../../../assets/2019-3-0-prefs-proj-01.png "Impostazioni progetto"){zoomable="yes"}

## Configurazione

### File di configurazione

Ciò consente di impostare il percorso del <b>file di configurazione</b> per Substance 3D Designer. Un file di configurazione utilizza l&#39;estensione <b>\*.sbscfg</b> e contiene un elenco di file di progetto con un&#39;impostazione di visualizzazione della compatibilità impostata.

*Impostazione predefinita: default\_configuration.sbscfg*

>[!NOTE]
>
> È possibile utilizzare l&#39;opzione della riga di comando **—config-file** per avviare Designer con un file di configurazione specifico.\
> Per ulteriori informazioni sui file di configurazione, è possibile fare riferimento alla pagina [Elenco di configurazione - SBSCFG](../../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) della documentazione.

### File di progetto

Un file di progetto contiene diverse impostazioni che definiscono gli aspetti principali dell’ambiente di lavoro in Designer, suddivise in schede. Queste impostazioni sono elencate nel capitolo Progetto di questa pagina. I file di progetto utilizzano l&#39;estensione <b>\*.sbsprj</b>.

Puoi importare più file di progetto da utilizzare per il tuo ambiente di lavoro in Designer. Quando sono presenti più file di progetto, le impostazioni che sono elenchi (ad esempio, percorsi controllati dalla libreria, alias e così via) sono *combinati* e le impostazioni che sono valori di set univoci sono definite dall&#39;*ultimo file di progetto dell&#39;elenco*.

*Impostazione predefinita: default\_project.sbsprj (sola lettura), user\_project.sbsprj*

>[!NOTE]
>
> Per ulteriori informazioni sull&#39;utilizzo dei file di progetto in una pipeline di produzione, è possibile fare riferimento alla pagina [File di configurazione del progetto - SBSPRJ](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) della documentazione.

### Visualizzazione della compatibilità

Alcuni nodi creati con una versione recente di Designer non sono compatibili con versioni precedenti della Substance Engine.

<b>La modalità di compatibilità</b> evidenzierà i nodi *non* compatibili con la Substance Engine selezionata, con un contorno giallo.

*Impostazione predefinita: Substance Engine v7*

### Vista 3D

|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modulo di rendering predefinito</b> | Questa impostazione consente di selezionare il [modulo di rendering 3D](../../../interface/3d-view/3d-renderers/3d-renderers.md) che deve essere utilizzato per impostazione predefinita quando si avvia una *nuova* [visualizzazione 3D](../../../interface/3d-view/3d-view.md).<br><br>*Impostazione predefinita: impostazione predefinita (modulo di rendering predefinito)* |
| <b>Shader predefinito</b> | Questa impostazione consente di selezionare lo shader da utilizzare per impostazione predefinita all&#39;avvio di una *nuova* [vista 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Impostazione predefinita: open_pbr.glslfx* |
| <b>Mappa ambiente predefinita</b> | Questa impostazione consente di selezionare la texture da applicare per impostazione predefinita all&#39;ambiente quando si avvia una *nuova* [vista 3D &#x200B;](../../../interface/3d-view/3d-view.md)<br><br>*Impostazione predefinita: panorama\_map.hdr* |
| <b>File di stato predefinito</b> | Il [file dello stato della scena **della** vista 3D](../../../interface/3d-view/3d-view.md) include diverse impostazioni per la vista 3D, quali la posizione della fotocamera, l&#39;esposizione dell&#39;ambiente e la trama. Viene utilizzato per memorizzare lo stato della vista 3D in modo da poter caricare rapidamente una scena personalizzata in base alle proprie esigenze. I file di stato della scena utilizzano l&#39;estensione **\*.sbsscn**.Questa impostazione consente di selezionare il file di stato della scena della vista 3D da utilizzare quando si avvia una nuova vista 3D.  **Avviso:** alcuni aggiornamenti software possono modificare il modo in cui gli stati della scena vengono salvati/caricati. Se la scena non è *ripristinata correttamente*, si consiglia di impostare manualmente lo stato desiderato della scena e di *riesportare* il file di stato della scena utilizzato come predefinito. <br><br>*Impostazione predefinita: vuota (in questo caso, viene utilizzato uno stato di scena predefinito)* |
| <b>Stato illuminazione predefinito</b> | Questa impostazione consente di selezionare quale delle luci disponibili predefinite attivare all&#39;avvio di una nuova [vista 3D](../../../interface/3d-view/3d-view.md), *se non è impostato alcun file* nel campo **file di stato predefinito**<br><br>*Impostazione predefinita: solo luce ambiente* |

### Alias

Gli alias vengono utilizzati per *abbreviare* i percorsi di sistema e consentire ai team di *condividere* le risorse in modo più efficiente. Gli alias vengono utilizzati *in tutto il software* e in *file SBS*.

Queste impostazioni consentono di *aggiungere* e *modificare* alias. Quando viene applicato un alias, *sostituisce* il percorso mappato utilizzando la seguente sintassi: <b>://</b>.

Esempio: se una risorsa *myResource* nella cartella *myFolder* si trova nel percorso *C:/Users/user/Documents*, la mappatura di questo percorso a *myalias* determinerà l&#39;utilizzo del percorso *myalias://myFolder/myResource* nell&#39;applicazione *e* nel pacchetto SBS a cui appartiene la risorsa.

*Predefinito: sbs; sd-3dview-shapes; sd-3dview-maps; sd-3dview-shaders (progetto predefinito)*

>[!WARNING]
>
> Gli alias sono *globali per l&#39;applicazione*. Ciò significa che verranno applicati a *tutti i percorsi* utilizzati nell&#39;applicazione, nonché a tutti i percorsi nei *file delle impostazioni del progetto SBSPRJ caricati*. È importante tenere presente questa limitazione quando si imposta l&#39;ambiente del progetto.\
> Si consiglia inoltre di *non nidificare* alias, ad esempio eseguendo l&#39;alias di un percorso incluso anche in un altro alias.

### Baker

|                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Nome risorsa predefinito</b> | Questa impostazione consente di impostare un **modello di denominazione** predefinito che verrà utilizzato per i file di immagine di output. Gli alias disponibili nella [finestra di cottura](../../../bakers/bakers.md) possono essere utilizzati anche qui (ad esempio *$(mesh)*, *$(bakername)*, *$(udim)*, *$(custom)*)<br><br>*Impostazione predefinita: $(mesh)\_$(bakername)* |
| <b>Predefinito predefinito</b> | Quando apri la [finestra di cottura](../../../bakers/bakers.md), puoi configurarla **già** con specifici forni e impostazioni utilizzando questa opzione per puntare a un file di predefiniti *JSON*. Questo file può essere esportato dalla finestra di cottura una volta impostato in base alle tue esigenze <br><br>*Impostazione predefinita: nessuna* |
| <b>Modalità filtro nomi</b> | Oggetto scena che deve essere utilizzato come nome per abbinare gli oggetti di scena low poli e high poli:<ul data-preserve-html="true"> <li data-preserve-html="true">Nome geometria: utilizzate il nome dell&#39;oggetto geometria mesh</li> <li data-preserve-html="true">Nome principale (versione precedente): utilizzate il nome dell&#39;elemento principale dell&#39;oggetto della geometria della trama (come in Designer 14.1 e versioni precedenti)</li> </ul>*Predefinito: nome geometria* |
| <b>Macro nome risorsa</b> | Invece dell&#39;alias *$(bakername)*, puoi utilizzare stringhe di caratteri personalizzate per [ogni fornaio](https://experienceleague.adobe.com/it/docs/substance-3d/bakers/bakers-settings/bakers-settings).  Quando l&#39;alias ***$(custom)*** viene utilizzato nel nome dell&#39;immagine di output per qualsiasi baker, verrà sostituito dalla stringa di caratteri corrispondente a tale baker nell&#39;elenco. Se una cella dell&#39;elenco corrispondente a un fornaio viene lasciata vuota, l&#39;alias *$(personalizzato)* *non* verrà sostituito per questo fornaio.Esempio: il valore &#39;c-mesh&#39; assegnato al fornaio &#39;Curvature Map From Mesh&#39; rinominerà automaticamente *t\_mymesh\_&#x200B;**$(personalizzato)*** in *t\_mymesh\_&#x200B;**c-mesh*** per l&#39;output del fornaio Curvature From Mesh *only *<br><br>*Impostazione predefinita: None* |
| <b>Filtro nome mesh secondarie</b> | Quando si utilizza l&#39;opzione **Corrispondenza per nome** nei [forni](../../../bakers/bakers.md), le parti delle versioni a bassa e alta definizione di una trama sono *corrispondenti* se il nome di tali parti prima dei **suffissi** definiti è *identico*. Questa impostazione consente di impostare suffissi personalizzati in base al flusso di lavoro specifico. Le parti corrispondenti delle trame possono far sì che i raggi ignorino la geometria indesiderata nelle operazioni di cottura.Esempio: l&#39;oggetto *body-torso&#x200B;**\_low*** nella trama *body.fbx* corrisponderebbe all&#39;oggetto *body-torso&#x200B;**\_high &#x200B;*** nel *body\_high.fbx,* *se questi oggetti esistono* in queste trame *.**Impostazione predefinita: \_low (Low Poly Mesh) / \_high (High Poly Mesh)*Analogamente,**&#x200B;backfaces&#x200B;**possono essere *ignorati in modo selettivo* per le parti di una trama il cui nome include il &#x200B;** suffisso&#x200B;**definito, per [specifici forni](https://experienceleague.adobe.com/it/docs/substance-3d/bakers/bakers-settings/bakers-settings) che includono l&#39;opzione &#x200B;** Ignora backface**<br><br>* Impostazione predefinita: \_ignorebf *<br><br>* Nota:* I suffissi Ignora backface e Poly mesh bassa/alta possono essere *combinati in qualsiasi ordine* (ad esempio *busto del corpo\_basso\_ignorebf*) |

### Gestione del colore

Consultare la pagina [Gestione colore](../../../color-management/color-management.md).

>[!WARNING]
>
> Le modifiche a queste impostazioni saranno effettive dopo il riavvio di Designer.

### Generale

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modelli di Substance</b> | Quando crei un nuovo grafico, ti viene chiesto di iniziare a lavorare su un **modello** che può avere diverse impostazioni e contenuti *preconfigurati*, come output (ad esempio *PBR (metallizzato/rugosità)*).Questa impostazione ti consente di puntare Designer verso directory in cui puoi archiviare i tuoi file SBS da utilizzare come modelli. I modelli personalizzati verranno quindi *aggiunti all&#39;elenco* durante la creazione di un nuovo grafico <br><br>*Predefinito: Nessuno *<br><br>*Nota:* Si consiglia di utilizzare i modelli correnti come riferimento per la configurazione e la formattazione dei file SBS dei modelli.  I modelli si trovano nella cartella **risorse > modelli** nella directory di installazione di Substance 3D Designer. |
| <b>Scene 3D</b> | Per impostazione predefinita, Designer utilizza lo **spazio tangente MikkT** nella vista 3D. MikkT è ampiamente utilizzato ed è l&#39;impostazione predefinita in programmi quali Unity, Unreal Engine 4, Blender e xNormal.È possibile utilizzare **il proprio spazio tangente** per la vista 3D, che viene fornito a Designer sotto forma di un *file DLL* input in questa impostazione. L&#39;etichetta viene rilevata automaticamente dal file DLL ed è possibile modificare la descrizione del plug-in <br><br>*Predefinito: mikktspace.dll* Ricalcola sempre i fotogrammi tangenti <br><br>*Predefinito: Non selezionato* Angolo di arrotondamento normale e tangente <br><br>*Predefinito: 180.0°* |
| <b>Varie</b> | Le mappe normali possono essere generate o elaborate utilizzando il formato <b>DirectX</b> o <b>OpenGL</b>. Questa impostazione consente di impostare il valore di questo formato in diversi punti, ad esempio [proprietà materiali](../../../interface/3d-view/material-properties/material-properties.md) nella [vista 3D](../../../interface/3d-view/3d-view.md) e i parametri del nodo filtro [Normale](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md).<br><br>*Impostazione predefinita:*<br><br> Per quanto riguarda il nodo filtro [Normale](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), è possibile impostare il valore predefinito per il parametro <b>Contenuto canale Alpha</b>. Puoi scegliere di forzare l&#39;alfa a 1 in tutti i casi o riempirlo con informazioni dal suo input.<br><br>*Impostazione predefinita: forza l&#39;Alpha a 1* |
| <b>Formati immagine</b> | Ciò consente di specificare le impostazioni di formato predefinite per *immagini esportate*<br><br>*Predefinito: Wavelet predefinito (BMP) / basato su pixel, deselezionato, non selezionato (EXR) / Non selezionato, non selezionato, 75 (JPG) / Velocità massima, non selezionato (PNG) / Predefinito (TGA) / LZW (TIF) / Non selezionato, 75 (WEBP)* |
| <b>Percorsi dipendenze</b> | <p>I pacchetti SBS generalmente hanno <b>dipendenze</b>, ovvero dipendono da <i>risorse esterne</i> come altri pacchetti SBS, bitmap o file vettoriali.<br>Queste dipendenze, elencate in [Gestione dipendenze](../../../interface/dependency-manager/dependency-manager.md), sono archiviate e <i>referenziate nel pacchetto SBS</i> con un <b>percorso</b> che punta a queste risorse.</p><p>Per le dipendenze che includono lo <i>stesso percorso</i> del pacchetto SBS (ovvero che si trovano nelle stesse posizioni o sottocartelle da quella posizione), il percorso di riferimento viene scritto <b>rispetto a</b> il percorso del pacchetto SBS.</p><p>Esempio: per un pacchetto SBS <code>myproject/mypackage.sbs</code>, un&#39;immagine <code>myproject/myfolder/myimage.png</code> verrà fatto riferimento a <code>myfolder/myimage.png</code> percorso in <code>pacchetto.sbs</code>).</p><p>Per le dipendenze che <i>non</i> includono lo stesso percorso del pacchetto SBS (ovvero si trovano in una posizione completamente diversa dal pacchetto SBS), è possibile scegliere la modalità di scrittura del percorso.</p><p>Se è impostato su <b>percorsi relativi</b>, alla risorsa verrà fatto riferimento nello stesso modo descritto in precedenza.</p><p>Esempio: per un pacchetto SBS <code>myparentfolder/myproject/mypackage.sbs</code>, un&#39;immagine <code>myparentfolder/myotherfolder/myimage.png</code> verrà fatto riferimento a <code>../myotherfolder/myimage.png</code> percorso in <code>pacchetto.sbs</code>.</p><p>Se è impostato su <b>percorsi assoluti</b>, alla risorsa verrà fatto riferimento dal percorso di sistema completo.</p><p>Esempio: per un pacchetto SBS <code>myparentfolder/myproject/mypackage.sbs</code>, un&#39;immagine <code>myparentfolder/myotherfolder/myimage.png</code> verrà fatto riferimento allo stesso percorso completo in <code>mypackage.sbs</code></p><p><i>Impostazione predefinita: ...percorsi relativi.</i></p><p><i>Nota:</i> in tutti i casi, lo spostamento delle risorse comporterà <i>interruzioni delle dipendenze</i>, che produrranno <b>nodi di istanza fantasma</b> nei grafici.  Per <i>consolidare</i> tutte le dipendenze in una singola cartella di progetto insieme al pacchetto SBS, puoi utilizzare le funzionalità <b>Esporta con dipendenze...</b> nel pannello [Esplora risorse](../../the-explorer-window/the-explorer-window.md). In questo modo viene creata una cartella di progetto <i>autonoma</i> che può essere spostata liberamente. |

### Libreria

Questa sezione consente di <b>gestire il contenuto personalizzato</b> della [libreria](../../../interface/the-library/the-library.md).

Il contenuto di tutte le cartelle elencate nell&#39;elenco <b>Percorsi aggiunti</b> verrà incluso nella libreria. Eventuali modifiche apportate al contenuto vengono applicate alla libreria, dopo un periodo di aggiornamento che può essere impostato nella [&#128279;](../../../interface/preferences-window/preferences-window.md)scheda [scheda](../../../interface/preferences-window/preferences-window.md) della [finestra Preferenze](../../../interface/preferences-window/preferences-window.md) della libreria.

Nelle colonne dell’elenco sono disponibili opzioni che consentono di controllare in modo più dettagliato il modo in cui il contenuto di queste cartelle viene aggiunto alla libreria:

* **Abilitato:** Il contenuto della cartella è visualizzato nella libreria (*Predefinito: Selezionato*)
* **Ricorsivo:** Il contenuto di tutte le cartelle secondarie viene visualizzato anche nella libreria (*Predefinito: Selezionato*)
* **Escludi modello:** I file che *nome* corrisponde all&#39;input Regex (espressione regolare) sono *non* visualizzati nella libreria (ad esempio `wip-*`). Ulteriori informazioni sulla sintassi dell&#39;espressione regolare [qui](https://doc.qt.io/qt-5/qregularexpression.html#wildcardToRegularExpression)
* **Escludi estensione:** I file che *estensione* includono la stringa di testo di input sono *non* visualizzati nella libreria. Più stringhe devono essere separate da `;` punti e virgola. (E.g. `jpg;png;tif;fbx`)

Se i pacchetti SBS vengono aggiunti alla libreria, le **grafiche** e le **risorse** in essa contenute possono essere *visualizzate nella libreria* come voci separate, se il relativo parametro **Visibile nella libreria** è impostato su &#39;Sì&#39;.\
Sono disponibili opzioni per definire se il parametro deve essere impostato su &#39;Sì&#39; *per impostazione predefinita* durante la creazione o l&#39;aggiunta di un nuovo grafico o di una nuova risorsa in un pacchetto.

*Impostazione predefinita: selezionata*

Se un documento di [Photoshop](https://www.adobe.com/it/products/photoshop.html) (\*.file PSD) incluso nella libreria contiene <b>più livelli</b>, un&#39;opzione consente di visualizzare il contenuto di* ogni livello come voce di immagine separata* nella libreria.

*Impostazione predefinita: selezionata*

>[!NOTE]
>
> Anche se le risorse personalizzate verranno aggiunte alla libreria, potrebbero *non essere visibili* a causa delle regole di filtro impostate per le categorie di libreria esistenti. Ti consigliamo di creare *i tuoi filtri* organizzati in cartelle, per garantire che i tuoi contenuti possano essere trovati in modo affidabile mentre lavori ai tuoi progetti.\
> Per ulteriori informazioni, vedere la sezione [Gestione di contenuti e filtri personalizzati](../../the-library/managing-custom-content/managing-custom-content-and-filters.md) della documentazione.

### Python

Substance 3D Designer caricherà automaticamente tutti i [plug-in](../../../scripting/plugin-basics/plugin-basics.md) che si trovano nelle cartelle aggiunte all&#39;<b>URL</b>.

*Impostazione predefinita: nessuna*

>[!WARNING]
>
> Le modifiche a queste impostazioni saranno effettive dopo il riavvio di Designer.\
> [I pacchetti di plug-in](../../../scripting/plugins-packages/plugins-packages.md) devono ancora essere installati *manualmente* utilizzando [Gestione plug-in](../../../scripting/plugin-manager/plugin-manager.md).

### Scripting

>[!WARNING]
>
> Questa funzione sarà *ritirata* in una versione futura, a favore della più robusta **API Python**. Pertanto, si consiglia di effettuare il cambiamento negli script il prima possibile.\
> Per iniziare, puoi accedere alla pagina [Callback dell&#39;applicazione](../../../scripting/application-callbacks/application-callbacks.md) nella sezione [Scripting](../../../scripting/scripting.md) della nostra documentazione.

Questa sezione consente di impostare e controllare *script* da eseguire quando si verificano *eventi* specifici in Designer. È particolarmente utile se utilizzato insieme all&#39;integrazione [Perforce](https://www.perforce.com/) che può essere configurata nella scheda Controllo versione delle impostazioni del progetto.

|                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Azioni</b> | Designer ha preconfigurato **trigger di callback**, che *eseguiranno lo script* fornito utilizzando l&#39;interprete configurato nell&#39;elenco **Interpreti** descritto di seguito.I callback inclusi sono i seguenti:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>onBeforeFileLoaded</strong> - esegue lo script <em>prima</em> del caricamento di un pacchetto SBS</li><li data-preserve-html="true"><strong>onAfterFileLoaded</strong>: esegue lo script <em>after</em> quando viene caricato un pacchetto SBS</li><li data-preserve-html="true"><strong>onBeforeFileSaved</strong> - esegue lo script <em>prima</em> del salvataggio di un pacchetto SBS</li><li data-preserve-html="true"><strong>onAfterFileSaved</strong> - esegue lo script <em>dopo</em> il salvataggio di un pacchetto SBS</li><li data-preserve-html="true"><strong>getGraphExportOptions</strong>: esegue lo script quando vengono chiamate le opzioni [Output di esportazione](../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)</li></ul>Nei file di installazione è incluso uno script [Python](https://www.python.org/), con le funzioni attivate da ogni callback *già configurato* e pronto per l&#39;uso. Puoi usarlo come punto di partenza e aggiungere funzionalità in base alle tue esigenze. Questo script è **functions.py** e si trova nella cartella **tools > scripting** dei file di installazione <br><br>*Default: None *<br><br>*Nota:* Inizialmente, selezionando uno script per uno qualsiasi dei callback si immetterà lo script in *tutti* i callback. È possibile impostare liberamente script diversi per callback specifici dopo tale punto. |
| **Interpreti** | In questo elenco è possibile fornire *interpreti* specifici che Designer deve utilizzare per eseguire gli script impostati nell&#39;elenco **Azioni** descritto in precedenza. Gli interpreti vengono identificati utilizzando un *alias personalizzato* che è possibile modificare nel campo di testo di ogni voce dell&#39;elenco.Un interprete [Python](https://www.python.org/) 3.6 è incluso nei file di installazione di Designer. Potete trovarlo nella cartella **plugin > pythonsdk** dei file di installazione <br><br>*Predefinito: Nessuno* |

### Controllo versioni

>[!WARNING]
>
> [Perforce](https://www.perforce.com/) è lo strumento *only* attualmente supportato per il controllo delle versioni.

Fare riferimento alla pagina [Controllo versione](../../../interface/preferences-window/version-control/version-control.md).

**Come si utilizza questo elemento?**

È consigliabile impostare tutte le preferenze *specifiche per il progetto* in un file di progetto (\*.sbsprj) in Designer. Queste preferenze includono:

* Plug-in spazio tangente
* Libreria
* Alias
* Impostazioni vista 3D
* Impostazioni di cottura
* [Impostazioni controllo versione](../../../interface/preferences-window/version-control/version-control.md)

Tutti i percorsi sono archiviati *rispetto a* il file di progetto (.sprj). in modo da avere una cartella **libreria** nella stessa posizione del file di progetto in Perforce, con la seguente struttura di sottocartelle:

* mappe/
* mesh/
* sbs/
* sbsar/
* psd/
* 3Dview/
* ...

Sullo stesso livello del file di progetto, potete anche memorizzare un plug-in per lo spazio tangente o uno shader predefinito.

Il file di configurazione (\*.sbscfg) deve essere inserito nell&#39;area di lavoro di Perforce insieme al file di progetto.

>[!NOTE]
>
> Per ulteriori informazioni sulla configurazione e l&#39;integrazione di Substance 3D Designer in una **pipeline di produzione** , *consigliamo vivamente* facendo riferimento alla sezione [Configurazione della pipeline e del progetto](../../../pipeline-and-project-con/pipeline-and-project-configuration.md) della documentazione.
