---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: Scopri le linee guida per l'ottimizzazione delle prestazioni per Substance 3D Designer, per migliorare le prestazioni grafiche e ridurre i tempi di elaborazione.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Linee guida per l'ottimizzazione delle prestazioni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---


# Linee guida per l&#39;ottimizzazione delle prestazioni

## Grafici Substance

Maggiore è la complessità dei [grafici Substance](../../compositing-graphs/substance-compositing-graphs.md), maggiore è la potenza di elaborazione necessaria per il rendering. Dovresti cercare di <b>trovare un equilibrio tra complessità e velocità di rendering</b>.\
Questo è *particolarmente* importante se li utilizzi in applicazioni grafiche in tempo reale, ad esempio i giochi.

In generale, i nodi che espongono parametri personalizzati, che possono essere modificati in fase di esecuzione, devono essere posizionati il più vicino possibile alla fine del grafico</b>.<b>

Ciò avviene perché l&#39;output di ogni nodo viene memorizzato nella cache dove possibile. Di conseguenza, più in alto è il grafico del nodo modificabile, più output dovranno essere elaborati ogni volta che uno di questi parametri esposti viene modificato. Se il nodo esposto è vicino alla fine del grafico, sarà necessario ricalcolare solo i pochi nodi tra di esso e i nodi di output.

Ad esempio, se modifichi un colore uniforme all’inizio del grafico, verranno ricalcolati tutti i nodi seguenti. Se modificate un nodo HSL posizionato direttamente prima dell&#39;output, solo questo nodo verrà ricalcolato, migliorando notevolmente le prestazioni del grafico.

Si prega di prendere nota delle seguenti linee guida:

### IMPOSTAZIONI GENERALI RELATIVE ALLE PRESTAZIONI

+++Il motore GPU è molto più veloce del motore CPU
A meno che non si disponga di una scheda grafica non supportata (integrata), utilizzare il motore di substance della GPU (cambiare con Hotkey F9).

+++

+++Il cambio della risoluzione principale del grafico è lento
Ricalcola il grafico, la cache e tutte le miniature. È preferibile utilizzare [la scheda <b>Batch </b>della finestra di dialogo di esportazione](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md) in quanto evita di eseguire un ricalcolo esteso e non necessario (ad esempio durante l&#39;esportazione con risoluzione 8192).

+++

+++In casi estremi, potrebbe essere necessario aumentare la cache della memoria
L&#39;applicazione [limita la quantità di RAM che può essere utilizzata](../../interface/preferences-window/preferences-window.md) per la cache delle immagini, ma è possibile ignorarla e aumentarla con attenzione.

+++

### OTTIMIZZAZIONE DEL GRAFICO

+++Prestare attenzione alle risoluzioni dei nodi e all&#39;ereditarietà in generale.
Valori elevati influiscono negativamente sulle prestazioni, quindi è importante considerare come verrà utilizzato il materiale e se è possibile ridurre le dimensioni dei dati coinvolti.

Ti consigliamo di ottenere ulteriori informazioni sulla risoluzione di [nodi (dimensioni output)](../../compositing-graphs/output-size/output-size.md) e sull&#39;[ereditarietà nei grafici Substance](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

+++

+++Usa scala di grigi quando non è necessario alcun colore
Le operazioni che interessano il colore impiegano quattro volte più tempo delle operazioni in scala di grigi. Inoltre, cercate di ridurre al minimo le conversioni dei caratteri tra colore e scala di grigi.

+++

+++Usa 8 bit quando non è necessario 16 bit
La versione CPU della Substance Engine (SSE2) *non supporta* il colore a 16 bit o la scala di grigi a 8 bit. Il motore GPU supporta tutte e 4 le combinazioni di 8/16 bit e scala di grigi/colore. *Attualmente, solo il motore CPU viene utilizzato nei plug-in Unity e Unreal Engine*.

+++

+++Riduci al minimo le dimensioni dell&#39;output del nodo quando possibile
A volte, il ridimensionamento di alcuni nodi non influisce sul risultato finale, ma influisce sulle prestazioni. Ad esempio, l’utilizzo di un nodo Colore uniforme impostato sulle stesse dimensioni di output del documento è inutile: Colore uniforme deve essere impostato su Assoluto [16px x 16px] e il nodo successivo su Relativo a elemento principale. In genere, questo trucco è indicato per le immagini a bassa frequenza, ad esempio il disturbo di Perlin.

+++

+++Non utilizzare immagini di dimensioni inferiori a 16*16 pixel
Questo rallenta le prestazioni di rendering.

+++

+++Quando utilizzate il nodo Fusione, disattivate la fusione degli Alpha quando non è necessaria


+++

+++Le sfocature e le alterazioni sono i nodi che richiedono più risorse del processore


+++

+++Alcuni generatori di rumore sono influenzati dalla quantità di pattern disegnati
Ad esempio, il nodo [Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) diventerà più lento nell&#39;elaborazione dei nuovi modelli aggiunti.

+++

+++Alcuni rumori sono influenzati da un fattore di scala
Questo fattore disegnerà più schemi. I nodi interessati includono rumori, pattern di Cella e così via. Se avete bisogno di un pattern di disturbo bianco, non utilizzate un disturbo con un valore di scala molto elevato e utilizzate invece i nodi [Disturbo bianco](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md) o [Disturbo bianco rapido](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md).

+++

+++Al contrario, ci sono alcuni generatori di rumore molto veloci
Queste comprendono [White Noise Fast](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md), [Somma frattale Base](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md) e [Anisotropic Noise](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md).

+++

+++Prestare attenzione con le funzioni di campionamento delle immagini in alcuni casi
Le funzioni vengono eseguite sul motore CPU, ad eccezione dei [processori pixel](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md). Se il campionamento delle immagini (modifica delle coordinate $pos) in [Value Processors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) o [FXmaps](../../function-graphs/fxmaps/fxmaps.md) è molto intenso, lo scambio tra VRAM e RAM della CPU potrebbe causare ritardi nelle prestazioni.

+++

### OTTIMIZZAZIONI PER L&#39;UTILIZZO SU DISPOSITIVI MOBILI

+++Si sconsiglia di utilizzare Altera e FX-Maps
Sono molto costose in termini di prestazioni.

+++

+++Evitare i nodi di sfocatura
In questo caso, utilizzare le trasformazioni di downscale.

+++

+++Lavora il più possibile in scala di grigi
Passa al metodo colore alla fine del grafico.

+++

+++Condividere il più possibile i nodi tra gli output


+++

### OTTIMIZZAZIONE DELLE DIMENSIONI PER LE BITMAP INCORPORATE

Per impostazione predefinita, per [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) le [dimensioni di output](../../compositing-graphs/output-size/output-size.md) sono impostate su [&#39;assoluto&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Ciò significa che se la bitmap è connessa attraverso la catena di nodi a un output, forzerà l&#39;output finale a corrispondere alle dimensioni della bitmap incorporata.\
La dimensione dell&#39;output di un nodo inserito dopo la bitmap sarà impostata su [&#39;Rispetto all&#39;input&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Ciò significa che il nodo erediterà anche le dimensioni della bitmap e le trasporterà lungo la catena dei nodi fino agli output. Per risolvere il problema, è necessario impostare il nodo dopo la bitmap in modo che le dimensioni di output siano impostate su [&#39;Rispetto al padre&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md).

Se il grafico è impostato per avere una risoluzione dinamica, potete impostare la dimensione di output sulla bitmap incorporata su Relativa alla pagina principale.\
In questo modo, le dimensioni della bitmap cambieranno in base al grafico principale e non ci si troverà in una situazione in cui il grafico elabora una risoluzione maggiore di quella necessaria.

>[!WARNING]
>
> Se si imposta un nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) su &quot;Rispetto al padre&quot; e si [pubblica](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) il grafico in una risorsa Substance 3D (SBSAR), la bitmap verrà salvata con una risoluzione di **256x256** anziché le dimensioni originali. Si consiglia invece di mantenere il [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) dei nodi Bitmap&#39; [Dimensioni output](../../compositing-graphs/output-size/output-size.md) come &#39;Assoluto&#39; e utilizzare un nodo [Trasformazione 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) impostato su &#39;Relativo al padre&#39; subito dopo il nodo Bitmap.

![Ottimizzazione bitmap incorporate 1](performance-optimization-guidelines.resources/input-1.jpg "Ottimizzazione bitmap incorporate 1")

![Ottimizzazione bitmap incorporate 2](performance-optimization-guidelines.resources/relativetoparent.jpg "Ottimizzazione bitmap incorporate 2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Inoltre, si consiglia di impostare il formato delle risorse Bitmap su Jpeg per ridurre al minimo le dimensioni delle risorse Substance 3D pubblicate (SBSAR).

</td>
<td style="border: 0;" valign="top">

![Ottimizzazione bitmap incorporate 3](performance-optimization-guidelines.resources/format.jpg "Ottimizzazione bitmap incorporate 3")

</td>
</tr>
</table>
