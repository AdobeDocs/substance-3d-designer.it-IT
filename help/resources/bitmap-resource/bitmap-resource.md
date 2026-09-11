---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Scoprite come importare, creare e utilizzare le risorse bitmap in Substance 3D Designer per la creazione di materiale basato su texture.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risorsa bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# Risorsa bitmap

Una risorsa bitmap è una risorsa in un pacchetto di Substance. È diverso dal nodo bitmap [ atomico. Il nodo bitmap atomica](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) è una rappresentazione specifica della bitmap all&#39;interno di[un grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md).

Le bitmap sono tra le risorse non grafiche più comuni di Substance 3D Designer, di solito il loro utilizzo rientra in una delle seguenti categorie:

* Una mappa con baking, [eseguita i baking internamente da Designer](../../bakers/bakers.md) o esternamente da un&#39;altra applicazione.
* Una texture di supporto, come un motivo, una mappa di grunge o una decalcomania.
* Una semplice maschera in scala di grigio per la fusione, creata internamente utilizzando [il nodo bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) o con un&#39;app esterna.

## Archiviazione bitmap

Le bitmap sono in genere le risorse più grandi gestite da Designer. Ecco perché è utile comprendere come Designer gestisce questi file con i suoi due tipi di file principali.

### Nei file Substance 3D (SBS)

La modalità di archiviazione delle bitmap nell&#39;SBS dipende dal fatto che [le colleghi o le importi, accertarsi innanzitutto di avere familiarità con il concetto.](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) Le bitmap importate possono essere modificate utilizzando gli [strumenti di pittura bitmap](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

A differenza delle risorse SVG (Grafiche vettoriali), le immagini bitmap vengono sempre memorizzate esternamente, anche se create come nuova risorsa o importate. I nuovi pacchetti di Substance vengono mantenuti in memoria fino a quando il file .SBS non viene salvato su disco. Una volta salvate su disco, le bitmap vengono archiviate in una cartella */resources* accanto al file SBS.

### In risorse Substance 3D (SBSAR)

In [file SBSAR](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md), le bitmap sono incorporate, il che significa che hanno un grande impatto sulla dimensione finale del file SBSAR. Ulteriori informazioni sull&#39;impatto sulle dimensioni dei file sono disponibili in questa pagina. Quando vengono pubblicati i file SBSAR, vengono incorporate solo le bitmap utilizzate per calcolare l&#39;output di un grafico. Tutte le bitmap inutilizzate vengono ottimizzate ed escluse dal pacchetto SBSAR finale, senza alcun effetto sulla dimensione del file.

## Tipo di file, metodo colore e risoluzione

Substance 3D Designer è in grado di modificare e riorganizzare facilmente i dati dalle bitmap, ma è preferibile tenere presente quanto segue:

* Imposta le risoluzioni su 2, ovvero segui le dimensioni standard della texture in tempo reale come <b>256, 512, 1024 ,2048,</b> ecc. Designer ridimensionerà le texture al di fuori di questo intervallo alla risoluzione corrispondente più vicina. Si noti che non devono essere in proporzioni quadrate.
* Sono supportati molti tipi di file, ma scegline uno che sia il più adatto alle tue esigenze. <b>La compressione senza perdita di dati o anche i tipi di file non compressi</b> come PNG o TGA offrono una qualità migliore rispetto a JPG o DDS.
* Assicuratevi di <b>impostare correttamente il metodo colore</b>, a seconda che siano necessari colori, scala di grigi o un canale alfa.

## Attributi bitmap

Le risorse bitmap in un pacchetto hanno una serie di attributi che è possibile personalizzare. La maggior parte degli attributi non ha uno scopo principale e sono utilizzati per i filtri libreria, anche se una minoranza influenza le dimensioni del file.

| Nome attributo | Scopo |
| --- | --- |
| Identificatore | Utilizzato per fare riferimento alla risorsa bitmap in un pacchetto, deve essere univoco. |
| Percorso del file | Percorso su disco della bitmap a cui fa riferimento la risorsa. |
| Descrizione | Descrizione visualizzata nelle descrizioni comandi [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) e [Libreria](../../interface/the-library/the-library.md) per questa risorsa. |
| Categoria | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Etichetta | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Autore | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| URL dell&#39;autore | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Tag | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Dati utente | Dati aggiuntivi opzionali, non utilizzati sulle bitmap. |
| Mostra nella libreria | Determina se la bitmap deve essere nascosta in [visualizzazione Libreria.](../../interface/the-library/the-library.md) |
| Formato bitmap | Raw o Jpeg, ha un grande effetto sulla dimensione del file SBSAR. Per ulteriori informazioni, consulta le [linee guida per la riduzione del file](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md). |
| Qualità di compressione bitmap | Ha effetto solo con la compressione Jpeg e determina il bilanciamento tra qualità e dimensione dei file. |

## Riduzione della dimensione dei file

Per consigli su come ridurre al minimo le dimensioni dei file delle bitmap incorporate nelle [risorse Substance 3D pubblicate (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md), consultate la pagina [Linee guida per la riduzione dei file](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) nella sezione [Procedure ottimali](../../best-practices/best-practices.md).
