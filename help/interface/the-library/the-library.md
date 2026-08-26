---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/the-library.html"
breadcrumb-title: ''
description: Utilizza la libreria in Substance 3D Designer per accedere e gestire i predefiniti dei nodi, i materiali e il contenuto personalizzato.
helpx_creative_field: ""
helpx_description: Designer > Interface > Library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Libreria
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---


# La libreria

Questa pagina presenta il pannello **Libreria** di Substance 3D Designer, il suo layout e gli strumenti disponibili per la ricerca e il filtraggio dei contenuti.

![Libreria](../../assets/library-main.png "Libreria")

## Panoramica

Il pannello <b>Libreria</b> è un *gestore delle risorse* a vista divisa, in cui puoi trovare e raccogliere tutte le *risorse* con cui devi lavorare nel grafico.

Controlla le *cartelle* sul disco rigido o in rete aggiunte all&#39;elenco dei [percorsi controllati dalla libreria](https://docs.substance3d.com/display/SDDOC/Project+Settings#ProjectSettings-proj-libraryLibrary) nelle [impostazioni del progetto](../../interface/preferences-window/project-settings/project-settings.md). Eventuali modifiche apportate a tali cartelle (aggiunta, rimozione e aggiornamento del contenuto) vengono *riportate* nella <b>libreria</b>.

>[!WARNING]
>
> **Informazioni sui contenuti personalizzati**
> 
> Le risorse personalizzate verranno aggiunte alla **libreria**, ma potrebbero non essere visibili a causa delle regole di filtro impostate per le categorie esistenti. Ti consigliamo di creare i tuoi filtri organizzati in cartelle, per garantire che i tuoi contenuti possano essere trovati in modo affidabile mentre lavori ai tuoi progetti.\
> Per ulteriori informazioni, vedere la sezione [Gestione di contenuti e filtri personalizzati](./managing-custom-content/managing-custom-content-and-filters.md) della documentazione.

La **libreria** può monitorare tutte le risorse supportate [risorse](../../resources/resources.md):

* Grafici da [Pacchetti Substance](../../getting-started/overview/overview.md) (SBS) e [Archivi Substance](../../getting-started/overview/overview.md) (SBSAR)
* [Immagini bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* [Immagini vettoriali](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [Grafici a funzioni](../../function-graphs/function-graphs.md)
* [File AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)
* [Font](../../resources/font-resource/font-resource.md)
* [Scene 3D](../../resources/3d-scene-resource/3d-scene-resource.md)

Il pannello è suddiviso in due parti principali:

* La sezione **Categorie** a sinistra
* La sezione **Contenuto** a destra

## Categorie

Situata a sinistra del pannello <b>Libreria </b>, la sezione <b>Categoria</b> contiene tutte le risorse *categorie* (ad esempio le cartelle) e *filtri*, come visualizzazione struttura.\
È possibile fare clic su qualsiasi elemento in questa visualizzazione struttura per visualizzarne il contenuto, insieme a quello di *tutti gli elementi figlio*.

### Le categorie

Le categorie e i filtri predefiniti contengono tutte le risorse fornite con Designer. Non possono essere modificati o rimossi.\
Le categorie predefinite includono:

* Preferiti: raccoglie tutte le risorse contrassegnate come &quot;Preferite&quot;
* [Elementi del grafico](../../interface/the-graph-view/graph-items/graph-items.md): elenca gli oggetti speciali per organizzare i grafici
* [Nodi atomici](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md): elenca i nodi atomici per [grafici a Substance](../../compositing-graphs/substance-compositing-graphs.md)
* [FX-Map nodi](../../function-graphs/fxmaps/fxmaps.md): include nodi specifici per i grafici calcolati dai nodi [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)
* [Nodi di funzione](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md): elenca i nodi atomici per [grafici di funzione](../../function-graphs/function-graphs.md)
* [Generatori di texture](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/texture-generators.md): contiene nodi che rappresentano [grafici Substance](../../compositing-graphs/substance-compositing-graphs.md) che generano contenuto in modo autonomo
* [Filtri](../../compositing-graphs/nodes-reference-for-com/node-library/filters/filters.md): contiene nodi che rappresentano [Substance grafici](../../compositing-graphs/substance-compositing-graphs.md) che modificano un input
* [Strumenti spline e percorsi](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-paths-tools.md): catalogo dei nodi [spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) e [percorsi](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md)
* [Funzioni SDF](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions): include nodi per la creazione di Funzioni SDF 3D, da utilizzare con i nodi [Shape splatter v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) e [3D viewer](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)
* [Funzioni](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md): include nodi che rappresentano [grafici di funzione](../../function-graphs/the-function-graph/the-function-graph.md)
* [Vista 3D](../3d-view/3d-view.md): offre contenuti relativi alle mappe utilizzate per l&#39;illuminazione basata su immagini in una scena 3D, ad esempio nella [vista 3D](../../interface/3d-view/3d-view.md), come mappe di ambiente e nodi per la creazione di mappe di ambiente
* Materiali PBR: materiali predefiniti che possono essere utilizzati come segnaposto per testare altri nodi, &quot;ricette&quot; o una configurazione di uno spazio di lavoro personalizzata. Per informazioni sulla creazione di materiali, consigliamo di dare un&#39;occhiata ai nostri [campioni di materiale](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) dedicati.
* [Valori](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md): nodi per la generazione di valori semplici nei grafici delle Substance.

## Contenuto

Il contenuto della <b>libreria</b> viene visualizzato come *miniature etichettate*. Queste miniature avranno un aspetto diverso a seconda dei seguenti fattori:

* [La Substance di grafici](../../compositing-graphs/substance-compositing-graphs.md) nei file [SBS](../../getting-started/overview/overview.md) e [SBSAR](../../getting-started/overview/overview.md) è rappresentata dal *primo output* o dall&#39;*icona personalizzata*, se impostata dall&#39;autore del grafico
* [Bitmap](../../resources/bitmap-resource/bitmap-resource.md) e [grafica vettoriale (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) sono rappresentate da un *rendering in miniatura* della bitmap stessa
* [Scene 3D](../../resources/3d-scene-resource/3d-scene-resource.md), [Grafici di funzione](../../function-graphs/the-function-graph/the-function-graph.md), [Font](../../resources/font-resource/font-resource.md) e [File AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) sono rappresentati da *icone generiche* per ogni tipo

>[!WARNING]
>
> **In caso di problemi con le miniature**
> 
> Il passaggio consigliato per la risoluzione dei problemi relativi alle miniature della libreria (immagine errata, rendering bloccato sull’icona di aggiornamento, ecc.) deve attivare manualmente un *aggiornamento delle miniature*.\
> A tale scopo, utilizzare il pulsante **Ricostruisci miniature** nella sezione [Libreria](../../interface/preferences-window/preferences-window.md) della [finestra Preferenze](../../interface/preferences-window/preferences-window.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Utilizzo di una risorsa dalla libreria

Per utilizzare una risorsa della libreria, *trascinala* nella posizione desiderata.\
È possibile selezionare *più* elementi nella sezione <b>Contenuto</b> tenendo premuto il tasto <b>Ctrl</b> mentre si fa clic sugli elementi. In questo caso, l&#39;operazione di trascinamento posizionerà i nodi nel grafico per l&#39;*intera selezione*.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Eliminazione di un nodo dalla libreria](../../assets/library-create-node.gif "Eliminazione di un nodo dalla libreria")

</td>
</tr>
</table>

### Ricerca di una risorsa per nome

La barra <b>Ricerca</b>, situata in alto a sinistra della sezione <b>Contenuti</b>, consente di cercare *qualsiasi risorsa per nome*. Durante la ricerca di contenuto in questo modo, la selezione corrente nella sezione <b>Categorie</b> viene ignorata e viene eseguita la ricerca dell&#39;*intero contenuto* nella <b>Libreria</b>.\
È possibile filtrare i risultati della ricerca in base al *tipo di grafico*, utilizzando l&#39;icona ![](../../assets/library-icon-search-filter.png) <b>Filtra per...</b> accanto alla barra <b>Ricerca</b>.

>[!NOTE]
>
> La barra di ricerca terrà conto del nome della risorsa che stai cercando, ma anche dei *tag* che la risorsa può contenere o della *categoria* a cui appartiene.\
> Se ad esempio si digita &#39;*Normale*&#39; verranno elencate tutte le risorse che possono essere utilizzate per generare o modificare una mappa normale. Questo è un buon modo per scoprire nuovi nodi, e quindi nuove possibilità!

![Ricerca di risorse nella libreria](../../assets/library-search-2.png "Ricerca di risorse nella libreria")

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Visualizzazione delle risorse della libreria

Utilizzando il pulsante a discesa ![](../../assets/library-icon-view-mode.png) <b>Modalità visualizzazione</b>, è possibile selezionare le dimensioni di visualizzazione per gli elementi di contenuto.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Modalità visualizzazione risorse libreria](../../assets/library-display-modes.png "Modalità visualizzazione risorse libreria")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Il pulsante ![](../../assets/library-icon-toggle-label.png) **Attiva/disattiva etichette** consente di visualizzare o nascondere le etichette dei nodi.

</td>
<td style="border: 0;" valign="top">

![Alterna etichetta](../../assets/library-toggle-label.png "Alterna etichetta")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Quando si posiziona il cursore su un elemento di contenuto, dopo un breve periodo verrà visualizzata una descrizione *dell&#39;elemento*, se l&#39;autore ne ha fornito una.\
*Fare clic con il pulsante destro del mouse* sull&#39;elemento per visualizzare ulteriori informazioni, incluso il percorso del file di origine per l&#39;elemento.

</td>
<td style="border: 0;" valign="top">

![Descrizione comando informazioni risorsa](../../assets/library-item-tooltip.png "Descrizione comando informazioni risorsa")

</td>
</tr>
</table>

>[!NOTE]
>
> Per [nodi di istanza](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), ovvero nodi non atomici, questo percorso è un *collegamento ipertestuale* che visualizzerà il file nell&#39;elenco dei file del sistema.\
> I nodi atomici utilizzano un percorso con alias speciale (ad esempio, `graphatomic://`, `structure://`, ...) che non è possibile selezionare perché punta a una libreria interna.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Preferiti

È possibile aggiungere qualsiasi elemento nella sezione <b>Contenuto</b> all&#39;elenco <b>Preferiti</b> utilizzando il pulsante ![](../../assets/library-icon-favoritepng.png) <b>Aggiungi a Preferiti</b>. Il pulsante consente inoltre di *rimuovere* contenuto dall&#39;elenco, se è già stato aggiunto.\
Quando il contenuto viene aggiunto a questo elenco, è disponibile nella categoria <b>Preferiti</b> della <b>Libreria</b> e verrà visualizzato nella *parte superiore* dell&#39;elenco di menu <b>Nodo</b> durante la ricerca di un nodo nel grafico, a condizione che i termini di ricerca corrispondano.

</td>
<td style="border: 0;" valign="top">

![Preferiti nella libreria](../../assets/library-favourites.png "Preferiti nella libreria")

</td>
</tr>
</table>
