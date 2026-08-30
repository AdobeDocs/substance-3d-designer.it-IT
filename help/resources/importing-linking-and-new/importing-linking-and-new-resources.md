---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Scopri come importare, collegare e creare nuove risorse in Substance 3D Designer per i tuoi progetti di materiali.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Importazione, collegamento e nuove risorse
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---


# Importazione, collegamento e nuove risorse

[Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) supporta 3 modalità di inserimento o creazione di nuove risorse da utilizzare nel grafico. Queste risorse possono essere di diversi tipi, inclusi [bitmap](../../resources/bitmap-resource/bitmap-resource.md), [grafica vettoriale](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [scene 3D](../3d-scene-resource/3d-scene-resource.md) e [font](../../resources/font-resource/font-resource.md). In questa pagina vengono illustrati i diversi metodi e i casi in cui è preferibile utilizzarli singolarmente.

Per accedere a tutti i metodi, fare clic su RMB in un pacchetto in Esplora risorse.

La tabella seguente fornisce una rapida panoramica delle differenze nelle funzionalità tra i metodi.

|                                                                                                                                                                         | Nuovo | Importa | Collega |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Grafici ([Substance grafici](../../compositing-graphs/substance-compositing-graphs.md), [Substance grafici funzione](../../function-graphs/function-graphs.md) | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(errore)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/error.svg"/></div> | <div><img alt="(errore)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/error.svg"/></div> |
| [Bitmap](../../resources/bitmap-resource/bitmap-resource.md),[grafica vettoriale (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/check.svg"/></div> |
| Scene 3D, [font](../../resources/font-resource/font-resource.md) | <div><img alt="(errore)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/error.svg"/></div> | <div><img alt="(errore)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/error.svg"/></div> | <div><img alt="(spuntare)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/check.svg"/></div> |
| Viene creato accanto al file SBS | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(errore)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/error.svg"/></div> |
| Modificabile in Designer | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(errore)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/error.svg"/></div> |
| Le modifiche esterne vengono sincronizzate automaticamente | <div><img alt="(errore)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/error.svg"/></div> | <div><img alt="(errore)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/error.svg"/></div> | <div><img alt="(spuntare)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/check.svg"/></div> |
| Incorporato nella SBSAR pubblicata | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)" data-preserve-html="true" src="importing-linking-and-new-resources.resources/check.svg"/></div> | <div><img alt="(spuntare)&quot; data-preserve-html=&quot;true" src="importing-linking-and-new-resources.resources/check.svg"/></div> |

## Nuove risorse

Per creare una nuova risorsa si intende che una risorsa nel pacchetto verrà creata da zero. Tutte le risorse solo per Designer possono essere create solo in questo modo, ad esempio Substance grafici e Substance grafico delle funzioni.

Un caso speciale si verifica quando si crea una nuova [bitmap](../../resources/bitmap-resource/bitmap-resource.md)o [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md): questi file verranno visualizzati in Esplora risorse e si comporteranno come una risorsa importata, ma senza richiedere un file esterno. Possono essere modificati in Designer. Le nuove immagini bitmap e SVG create in questo modo sono utili se non è necessario ricorrere a un editor esterno, ad esempio per ottenere una forma vettoriale semplice e veloce o una semplice maschera bitmap 2D dipinta.

## Risorse importate

Per importare una risorsa, accanto al file SBS verrà creato un duplicato del file di risorse (nella cartella *Graphname*.resources), [ad eccezione dei file SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). Talvolta viene anche chiamato &#39;incorporamento&#39; di una risorsa.

Una volta inserita nel grafico, una risorsa importata può quindi essere modificata in Designer utilizzando [gli strumenti di pittura bitmap](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) o [gli strumenti di modifica vettoriale](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) nella [vista 2D](../../interface/2d-view/2d-view.md). Le risorse importate non sono più collegate ai file di origine originali: se si modifica, rimuove o aggiorna il file importato originariamente, ciò non ha alcun effetto sulla risorsa in Designer.

Nel caso di [file AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md), la procedura è un po&#39; più complessa; i grafici di Substance e le risorse bitmap vengono creati dal pacchetto AxF. Tutte queste possono comunque essere modificate nei rispettivi editor: vista Grafico o vista 2D.

>[!WARNING]
>
> Per i nuovi pacchetti, le risorse importate e nuove risorse non vengono salvate su disco finché il pacchetto non viene salvato.

## Risorse collegate

Collegare una risorsa significa che Designer farà riferimento al file sorgente nella posizione originale sul disco, ma lo presenterà in Esplora risorse come se fosse parte del pacchetto. Non sarà possibile modificare la risorsa effettiva direttamente all&#39;interno di Designer, ma solo utilizzarla come componente nel grafico o come origine per le mappe di cottura.

Il collegamento è ideale se sapete che è necessario utilizzare un editor esterno per aggiornare la risorsa mentre lavorate contemporaneamente in Designer. Baking maps è un ottimo esempio: potresti avere bitmap di riferimento di Designer da un&#39;applicazione di baking esterna, che ricaricherà e aggiornerà automaticamente il grafico non appena questi file verranno modificati. Allo stesso modo, le scene 3D possono essere collegate solo, in modo che ogni volta che si esporta un nuovo file FBX dall’applicazione 3D, Designer aggiorna automaticamente la trama utilizzata nella vista 3D. Se le vostre mappe di cottura da questa mesh dovrete riavviare manualmente il processo di cottura, idealmente facendo clic su RMB e selezionando &#39;Aggiorna tutte le mappe con baking&#39;.

## Eliminazione delle risorse

Quando si elimina una risorsa da un pacchetto, viene visualizzata la finestra di dialogo <b>Conferma rimozione elemento</b>. Se alcuni elementi in fase di rimozione sono *referenziati da altre risorse*, ad esempio [istanze di grafici](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) e [risorse bitmap](../../resources/bitmap-resource/bitmap-resource.md) utilizzate in [Substance grafici](../../compositing-graphs/substance-compositing-graphs.md), la finestra di dialogo includerà un *avviso ed elenco* di questi elementi.

>[!NOTE]
>
> Si consiglia di prestare attenzione a questi elementi e di intraprendere le azioni necessarie per *prevedere eventuali dipendenze interrotte* che potrebbero derivare dall&#39;eliminazione di elementi da un pacchetto.\
> Queste azioni possono includere *la rimozione di tutti gli usi* di queste risorse prima dell&#39;eliminazione.

![&quot;Risorsa eliminata in uso&quot; avviso](importing-linking-and-new-resources.resources/confirm-item-removal.png "&quot;Risorsa eliminata in uso&quot; avviso"){width="512px"}
