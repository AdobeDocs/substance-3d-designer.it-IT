---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/graph-parameters.html"
breadcrumb-title: ''
description: Scoprite come creare e gestire i parametri dei grafici in Substance 3D Designer per controllare le proprietà e i comportamenti dei materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Graph parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Parametri del grafico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 1%

---


# Parametri del grafico

Questa pagina descrive i parametri standard per il <b>grafico Substance</b>.

Un grafico ha diversi parametri che potete modificare. Puoi trovarli facendo clic su *spazio vuoto* nel grafico o selezionando *elemento grafico* nel pannello <b>Esplora risorse</b>. I parametri verranno quindi visualizzati nella vista Parametri.

<a name="base-parameters"></a>

## Parametri base

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Questa sezione include parametri che hanno un impatto su *tutti i nodi in essa contenuti*.

In effetti, ogni nodo di questo grafico con parametri di base impostati sul [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) &#39;Relativo al padre&#39; otterrà i propri valori dai parametri di base *del grafico*.

A loro volta, i valori dei parametri di base del grafico dipenderanno dal contesto in cui il grafico viene utilizzato.

</td>
<td style="border: 0;" valign="top">

![Parametri di base](graph-parameters.resources/graph-parameters-01.png "Parametri di base"){width="512px" zoomable="yes"}

</td>
</tr>
</table>

Ad esempio, quando il grafico viene utilizzato in un altro grafico come nodo di istanza, per impostazione predefinita i relativi parametri di base utilizzano il metodo di ereditarietà &#39;Relativo all&#39;input&#39;. Ciò significa che otterranno i loro valori dal nodo connesso al suo input primario. (a meno che non siano stati [sostituiti](#input-parameters))

Nella maggior parte dei casi, l’ereditarietà svolge un ruolo significativo nella definizione di questi valori e nel modo in cui questi cambiano in tutto il grafico. Si consiglia pertanto di acquisire una buona conoscenza dell&#39;[ereditarietà nei grafici Substance](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) prima di utilizzare questi parametri.

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Dimensioni output</b> | Questo parametro consente di scegliere la *risoluzione base* delle immagini nel grafico.  Utilizzare la <div><img data-preserve-html="true" height="22" src="graph-parameters.resources/graph-parameters-02.jpg"/></div> pulsante di blocco per far corrispondere i valori di altezza e larghezza e mantenere l&#39;immagine quadrata durante la regolazione delle dimensioni.<br><br>*Impostazione predefinita: (0,0) - Rispetto alla principale* [Ulteriori informazioni](../../compositing-graphs/output-size/output-size.md) |
| <b>Formato di output</b> | Consente di scegliere *la profondità di bit di base* nel grafico, tra le seguenti opzioni:<ul data-preserve-html="true"><li data-preserve-html="true">8 bit</li><li data-preserve-html="true">16 bit</li><li data-preserve-html="true">HDR Low Precision 16F (virgola mobile a 16 bit)</li><li data-preserve-html="true">HDR High Precision 32F (virgola mobile a 32 bit)</li></ul>*Impostazione predefinita: 8 bit per canale - Rispetto all&#39;elemento padre* |
| <b>Dimensione pixel</b> | Definisce le dimensioni in pixel. Si consiglia di lasciare entrambi i valori **Larghezza** e **Height** impostati su **1**.*Impostazione predefinita: (1,1) - Rispetto all&#39;elemento padre* |
| <b>Modalità Porzione</b> | Definisce la *modalità di affiancamento* di base nel grafico dalle seguenti opzioni:<ul data-preserve-html="true"> <li data-preserve-html="true">Nessun affiancamento</li> <li data-preserve-html="true">Affiancamento orizzontale</li> <li data-preserve-html="true">Affiancamento verticale</li> <li data-preserve-html="true">Porzioni H+V (orizzontale e verticale)</li> </ul>*Impostazione predefinita: Porzione H e V - Relativa all&#39;elemento padre* |
| <b>Numero casuale</b> | Definisce il *valore di inizializzazione casuale* di base per il grafico.  Utilizzare la <div><img data-preserve-html="true" height="22" src="graph-parameters.resources/graph-parameters-03.jpg"/></div> per assegnare un nuovo valore casuale al valore di inizializzazione casuale.<br><br>*Impostazione predefinita: 0 - Rispetto all&#39;elemento padre* |

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<a name="attributes"></a>

## Attributi

La sezione <b>Attributi</b> contiene *metadati* per il grafico, che fornisce informazioni per *identificare*, *classificare* e *applicare* il grafico come progettato dall&#39;autore.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Attributi del grafico](graph-parameters.resources/graph-parameters-04.png "Attributi del grafico"){zoomable="yes"}

</td>
</tr>
</table>

+++Elenco di attributi

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Identificatore** | Questo è il nome del grafico e deve essere *univoco*. Non è possibile avere due o più grafici con lo stesso <b>identificatore</b> nello stesso pacchetto. Viene utilizzato come *nome* del grafico nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md).<br><br>*Nota:* L&#39;identificatore *non può essere una stringa vuota*. Le stringhe vuote vengono sostituite automaticamente da `_` o `Substance_graph`. Per questo valore è possibile utilizzare *solo* i caratteri seguenti: *`A-Z, 1-9, @$%[{]}_-`.* I caratteri non autorizzati vengono sostituiti automaticamente da `_`.<br><br>*Impostazione predefinita: Nuovo\_grafico oppure impostata dall&#39;utente durante la creazione del grafico* |
| **Etichetta** | L&#39;<b>etichetta</b> viene utilizzata al posto dell&#39;<b>identificatore</b> per visualizzare il *nome* del grafico per una migliore leggibilità negli scenari *rivolti all&#39;utente*, ad esempio la voce [Libreria](../../interface/the-library/the-library.md) o l&#39;etichetta [nodo istanza](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).  Un&#39;etichetta può essere *non univoca* e contenere caratteri speciali.<br><br>*Suggerimento:* Se si rinomina un grafico, ad esempio in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), è possibile modificare anche l&#39;etichetta.<br><br>*Impostazione predefinita: vuota* |
| **Tipo** | <b>Type</b> viene utilizzato per definire lo scopo previsto di un [grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md). È destinato principalmente alla funzionalità di interoperabilità &quot;Invia&quot; di [&#128279;](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md). |
| **Modello di materiale** | L&#39;impostazione del modello di materiale del grafico garantisce l&#39;utilizzo dello shader appropriato nella vista 3D, se è disponibile uno shader *corrispondente al modello*.<br>Ad esempio la visualizzazione di un grafico con la modalità materiale `OpenPBR v1.1` nella vista 3D selezionerà lo shader `OpenPBR Surface` in per il materiale di destinazione.<br><br>Se non viene trovato uno shader corrispondente o il modello del grafico è impostato su `Undefined`, lo shader utilizzato per il materiale di destinazione nella vista 3D è *invariato*. |
| **Dimensioni fisiche** | Questo valore specifica la dimensione della texture nel *mondo fisico*, in X (lunghezza), Y (larghezza) e Z (height). È quindi intrinsecamente correlato al materiale che viene prodotto nel grafico. La dimensioni fisiche può essere utilizzata, ad esempio, per visualizzare la texture con le proporzioni corrette nella <b>vista 2D</b> e nella <b>vista 3D</b>.<br><br>*Suggerimento:* La dimensioni fisiche di un grafico a Substance può essere recuperata come valore Float3 nei grafici a funzione Substance applicati a qualsiasi nodo del grafico, utilizzando la variabile $phyalsize [incorporata](../../function-graphs/variables/system-variables/system-variables.md).<br><br>*Nota:* Il valore **Z** non è attualmente *considerato* nella **3D Visualizza**. Il valore **Scala Height** per il materiale deve pertanto essere impostato utilizzando un nodo **Output** impostato sull&#39;utilizzo **scala altezza** o direttamente nelle **Proprietà materiali**.<br><br>*Impostazione predefinita: (0,0,0)* |
| **Icona** | Quest&#39;area consente di definire un&#39;*icona* che verrà utilizzata dalla <b>libreria</b> per visualizzare la voce di questo grafico, sia come <b>SBS</b> che come <b>SBSAR</b>. L&#39;icona viene utilizzata anche in altre situazioni, ad esempio <b>Shelf</b> di [Substance 3D Painter](https://www.adobe.com/it/products/substance3d-painter.html). L&#39;area offre le seguenti opzioni:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Sfoglia</b>: consente di sfogliare i file di sistema per individuare l&#39;<i>immagine esistente</i> da utilizzare come icona</li> <li data-preserve-html="true"><b>Genera</b>: genera un&#39;icona utilizzando un <i>predefinito incorporato</i> del nodo <b>PBR render</b></li> <li data-preserve-html="true"><b>Incolla</b>: consente di incollare i dati immagine attualmente presenti negli <i>Appunti</i> come icona</li> <li data-preserve-html="true"><b>Rimuovi</b>: questa opzione <i>rimuove</i> l&#39;icona esistente e lascia lo slot per icone <i>vuoto</i></li> </ul>*Nota:* l&#39;opzione **Genera** utilizza la **Dimensioni fisiche** per determinare la **Scala Height** della **PBR render** per il relativo effetto di spostamento. Se nel grafico esiste un nodo **Output** impostato sull&#39;utilizzo **dimensione fisica**, verrà utilizzato questo output. Se tale output non esiste, viene utilizzato *invece* il valore degli **Attributi** del grafico. Se il valore dell&#39;attributo è (0,0,0), viene utilizzato il *valore predefinito* di 0,1.<br><br>*Nota:* Quando *nessuna icona* è definita, viene utilizzato il *primo output immagine* per il grafico.<br><br>*Impostazione predefinita: vuoto* |
| **Pacchetto** | Il nome file *assoluto* per il **pacchetto** a cui appartiene questo grafico.Il pulsante **Cartella** consente di aprire una nuova *finestra del file browser* di sistema in questa posizione.*Impostazione predefinita: Nome file pacchetto / Vuoto se il pacchetto non è mai stato salvato* |
| **Esposto in SBSAR** | Questo controlla se il grafico e i suoi output possono essere *visualizzati* nel file **SBSAR** pubblicato dal **pacchetto** del grafico.Ciò è utile se alcuni grafici nel pacchetto vengono utilizzati solo come *grafici secondari* per il grafico principale del pacchetto e *non devono essere visualizzati* nel **SBSAR**.*Impostazione predefinita: Sì* |
| **Mostra nella libreria** | Controlla se il grafico deve essere *visibile* nella **libreria**, se il pacchetto è archiviato in una posizione *osservata* dalla **libreria**.*Impostazione predefinita: impostata nella scheda Libreria delle impostazioni del progetto* |
| **Descrizione** | Questo è il *testo di descrizione* del grafico.È visibile nella *descrizione comandi* per la voce del grafico nella **libreria**, in qualsiasi nodo **istanza** per questo grafico e nel software con **integrazione Substance** esistente.*Impostazione predefinita: vuota* |
| **Categoria** | È possibile impostare una *categoria* per questo elemento grafico nella **libreria**.*Impostazione predefinita: vuoto* |
| **Autore** | È possibile utilizzare questo campo per inserire il *nome* dell&#39;autore.*Impostazione predefinita: vuoto* |
| **URL autore** | Questo campo consente di immettere un *URL*, ad esempio il sito Web dell&#39;autore.*Impostazione predefinita: vuoto* |
| **Tag** | Potete usare questo campo per aggiungere i vostri *tag*, per migliorare la *ricercabilità* e la *individuabilità* del grafico.*Impostazione predefinita: vuoto* |
| **Gruppo** | Consente di attivare il raggruppamento di voci nel menu Nodo. Le risorse, ad esempio grafici o bitmap, che condividono un valore &#39;Gruppo&#39; comune vengono raggruppate in una sezione che prende il nome dal gruppo. *Impostazione predefinita: vuota* |
| **Dati utente** | È possibile utilizzare questo campo per aggiungere ulteriori dati. Ciò è utile per le integrazioni personalizzate in software di terze parti. Substance 3D Painter e Sampler utilizzano questi dati utente per impostare determinati comportamenti specifici.*Impostazione predefinita: vuoto* |
| **Dati modello** | Quando come modello viene utilizzato un grafico a Substance, questo attributo imposta la categoria e il sottotitolo del modello [. &#x200B;](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)Sono separate da: &lt;category>;&lt;subtitle> <br><br>*Default: Empty* |

+++
<a name="input-parameters"></a>

## Parametri di input

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Tutti i parametri specifici del grafico, inclusi [parametri esposti](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), sono [gestiti](../../compositing-graphs/manage-parameters/manage-parameters.md), modificati e visualizzati in anteprima qui.

È inoltre possibile creare [predefiniti di parametro](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md) per alcuni o tutti i parametri.

</td>
<td style="border: 0;" valign="top">

![Parametri di input](graph-parameters.resources/graph-parameters-05.png "Parametri di input"){zoomable="yes"}

</td>
</tr>
</table>

+++Sostituzione dei parametri di base
Quando si utilizza un grafico in un altro grafico come [nodo di istanza](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), è possibile controllare il valore predefinito per qualsiasi parametro di base su quel nuovo nodo di istanza.

Apri il menu hamburger nella parte superiore della sezione &quot;Parametri di input&quot; e vai al sottomenu &quot;Ignora parametri di base&quot; per selezionare un parametro di base per il quale desideri impostare un valore predefinito arbitrario.

L’editor del parametro selezionato apparirà sopra l’elenco dei parametri di input del grafico. È quindi possibile regolarne il valore e il [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) in base alle esigenze.

+++

>[!IMPORTANT]
>
> Le schede <b>Anteprima</b> e <b>Predefiniti</b> sono disabilitate quando si utilizza la [modifica in contesto](../../interface/preferences-window/preferences-window.md).

<a name="inputs"></a>

## Input

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In questa parte sono elencati tutti i nodi [Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) del grafico.

Puoi riordinarli utilizzando il trascinamento sulla maniglia all’estrema sinistra di ogni elemento.

</td>
<td style="border: 0;" valign="top">

![Input](graph-parameters.resources/graph-parameters-06.png "Input"){zoomable="yes"}

</td>
</tr>
</table>

<a name="outputs"></a>

## Output

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In questa parte, tutti i nodi [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) del grafico.

Puoi riordinarli utilizzando il trascinamento sulla maniglia all’estrema sinistra di ogni elemento.

</td>
<td style="border: 0;" valign="top">

![Output](graph-parameters.resources/graph-parameters-07.png "Output"){zoomable="yes"}

</td>
</tr>
</table>
