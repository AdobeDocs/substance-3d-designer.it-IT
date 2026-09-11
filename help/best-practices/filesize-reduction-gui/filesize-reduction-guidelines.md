---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Linee guida per la riduzione delle dimensioni dei file dei grafici Substance al fine di ottimizzare le prestazioni e i requisiti di storage.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Linee guida per la riduzione delle dimensioni dei file
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# Panoramica

In alcuni casi la dimensione totale dei file di [risorse Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) può essere un fattore importante. Questa pagina contiene alcune aree critiche e impostazioni da tenere presenti quando si tenta di ridurre le dimensioni dei file.

La dimensione del file è determinata principalmente da [bitmap incorporate.](../../resources/bitmap-resource/bitmap-resource.md) Si tratta di file collegati, incorporati o in batch e aggiunti al file [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) come risorsa. Nella risorsa Substance 3D vengono pubblicate solo le bitmap utilizzate in un grafico, ovvero connesse a un output direttamente o attraverso la catena di nodi. In un file di Substance 3D, le bitmap non hanno alcun impatto sulle dimensioni del file, poiché tutte le risorse bitmap sono ancora memorizzate all&#39;esterno del file.

>[!IMPORTANT]
>
> Assicuratevi che la proprietà [Dimensione output](../../compositing-graphs/output-size/output-size.md) di tutti i nodi [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) sia impostata sul metodo *Assoluto* [di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). In caso contrario, la [risorsa bitmap](../../resources/bitmap-resource/bitmap-resource.md) a cui si fa riferimento verrà salvata con la risoluzione predefinita 256\*256 nel file di risorse Substance 3D pubblicato, che* influirà sulla qualità* di uno o più output.

## Fattori dimensione file

Ci sono alcuni fattori diversi che influenzano la dimensione totale dei file SBSAR. Sono elencati di seguito con una breve spiegazione.

+++Risoluzione
Ovviamente ha un grande effetto. Scegliete la risoluzione più bassa possibile, tenendo presente che il file Substance potrebbe anche funzionare con risoluzioni maggiori. Potete usare i trucchi di mascheratura della risoluzione standard per far sembrare le bitmap più piccole più grandi.

*Disponibile in: software esterno o importazione/riesportazione di bitmap in Designer.*

+++

+++Metodo colore file
Impostato nell’Editor immagini prima dell’esportazione, il metodo colore influisce anche sulle dimensioni dei file quando si utilizza il formato bitmap RAW. Le immagini bitmap solo in scala di grigio sono più piccole delle immagini RGB(A).

*Rilevato in: software esterno o importazione/riesportazione bitmap in Designer durante la configurazione corretta di [nodi di output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).*

+++

+++Formato file
Il formato di file delle immagini fa la differenza, anche se in alcuni casi può essere ignorato. Un programma come Photoshop consente un controllo leggermente maggiore sulla compressione dell&#39;JPG e a volte può offrire una strada di mezzo decente.

*Disponibile in: software esterno o importazione/riesportazione di bitmap in Designer.*

+++

+++Utilizzo nel grafico
La modalità impostata per il nodo Bitmap influisce anche sul modo in cui Designer comprimerà il file; l&#39;utilizzo di un file in scala di grigio come bitmap a colori nel grafico comporta la creazione di file di grandi dimensioni. Assicurati di impostarle correttamente!

*Trovato in:[Proprietà nodo bitmap.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++Formato bitmap nel pacchetto
Nelle proprietà Risorsa è possibile scegliere tra la compressione &quot;Raw&quot; e &quot;Jpeg&quot;. Ciò può avere un effetto considerevole sul risultato finale.

*Trovato in: Proprietà risorsa bitmap tramite la finestra Esplora risorse.*

+++

+++Qualità di compressione bitmap nel pacchetto
Quando si utilizza il formato &quot;Jpeg&quot; Bitmap, il cursore seguente può influire sulla qualità e sulle dimensioni dei file. Questo cursore non si comporta molto prevedibilmente, ma 1 tende a corrispondere alla compressione JPG di qualità più elevata e 0,5 tende a dare le dimensioni più piccole.

*Trovato in: Proprietà risorsa bitmap tramite la finestra Esplora risorse.*

+++

+++Modalità di compressione alla pubblicazione
Quando si esegue la pubblicazione su SBSAR, è possibile scegliere tra &quot;Automatico&quot;, &quot;Migliore&quot; e &quot;Nessuno&quot; per la compressione, questi fattori possono fare una differenza notevole se si utilizza il formato bitmap &quot;Raw&quot;. Questo influisce notevolmente anche sulla velocità di esportazione. Generalmente non si consiglia di utilizzare &quot;nessuno in quanto non offre alcun aumento della qualità.

*Trovato in: impostazioni di pubblicazione finali per un pacchetto SBSAR.*

+++

## Confronto dimensioni file

La tabella seguente mostra l’influenza di tutte le impostazioni l’una sull’altra. La bitmap utilizzata è un&#39;immagine 4096x4096 del disturbo generato, esportata da Photoshop come TGA a 24 bit o JPG con qualità 8. I file TGA sono stati esportati anche in scala di grigi e in modalità RGBA.

Il grafico posiziona semplicemente un singolo nodo bitmap connesso a un singolo output. Il metodo Bitmap viene impostato in base al metodo del file sorgente.

Mentre la tabella a destra non è completamente conclusiva, quando si confrontano i risultati visivi e le dimensioni dei file è possibile imparare quanto segue:

* Bitmap raw + compressione Migliore offre la migliore qualità con file di dimensioni accettabili.
* I file sorgente precompressi possono dare dimensioni ridotte nella maggior parte dei casi, ma a un costo di qualità.
* File più piccoli, ma la qualità peggiore si ottiene con il formato pacchetto JPG con qualità 0.5.
* La scala di grigi non è sempre più piccola in dimensione di file, ma avrà una qualità superiore rispetto al colore con impostazioni simili.

>[!NOTE]
>
> **Formato Jpeg Bitmap**
> 
> È importante notare che le mappe speciali che richiedono un&#39;elevata precisione, ad esempio le mappe Normali, le mappe Vettoriali e altre, probabilmente non devono essere impostate sulla compressione Jpeg, poiché questo comporterà artefatti molto più visibili.

| Immagine sorgente | TGA a colori | Colore JPG | TGA scala di grigi | JPG in scala di grigi |
| --- | --- | --- | --- | --- |
| <b>Modalità di compressione Formato bitmap raw</b>: *Nessuna* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>Formato bitmap raw</b> Modalità di compressione: *Alta* | 9,11 MB | 3,37 MB | 5,06 MB | 4,75 MB |
| <b>Formato Jpeg Bitmap</b> Qualità compressione: *1* | 5,09 MB | 1,94 MB | 6,30 MB | 2,49 MB |
| <b>Formato Jpeg Bitmap</b> Qualità compressione: *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>Formato Jpeg Bitmap</b> Qualità compressione: *0* | 407 KB | 433 KB | 990 KB | 808 KB |
