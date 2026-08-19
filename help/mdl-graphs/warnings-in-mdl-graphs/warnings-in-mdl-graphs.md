---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/warnings-in-mdl-graphs.html"
breadcrumb-title: ''
description: Comprendere e risolvere gli avvisi nei grafici MDL per garantire una corretta definizione e rendering del materiale.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Warnings in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avvisi nei grafici MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Avvisi nei grafici MDL

In questa pagina vengono elencati i messaggi di avvertenza ed errore che possono essere attivati dai grafici MDL in [Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) e vengono fornite le procedure di risoluzione dei problemi più comuni per ciascuno di essi.

Gli avvisi vengono visualizzati nella descrizione comandi dell&#39;icona di avviso per la risorsa grafico nel pannello [Esplora risorse](https://helpx.adobe.com/it/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html) e nell&#39;angolo inferiore sinistro della [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) se il grafico è caricato.

>[!NOTE]
>
> Le illustrazioni in questa sezione sono state registrate in <b>Substance grafici modello</b>, che erano *ritirati* nella versione <b>13.0.0</b> di Substance 3D Designer. Tuttavia, si applicano anche ai grafici MDL.

## ![(errore)](../../assets/error.svg) Nessun nodo di output definito

Nessun nodo di output definito per il grafico.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Selezionare qualsiasi nodo nel grafico che genera un valore il cui tipo corrisponda al tipo previsto per questa funzione, se presente, quindi fare clic su RMB e selezionare l&#39;opzione <b>Imposta come radice</b> nel menu di scelta rapida oppure fare doppio clic su LMB sul nodo.\
Il nodo di output di un grafico modello Substance è colorato in *arancione*.

![&#39;Nessun nodo di output definito&#39; soluzione](../../assets/warnings-model-output.gif "&#39;Nessun nodo di output definito&#39; soluzione")

### ![(errore)](../../assets/error.svg) Almeno un valore di input è stato rifiutato

Il valore fornito per un parametro non determina un calcolo valido del nodo.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Regolate il valore in modo che abbia senso per il parametro di destinazione.

![&#39;Almeno un valore di input è stato rifiutato&#39; soluzione](../../assets/warnings-model-rejected-value.gif "&#39;Almeno un valore di input è stato rifiutato&#39; soluzione")

### ![(errore)](../../assets/error.svg) Nessun valore di input

Non è stato fornito un valore di input previsto da un nodo per eseguire il calcolo.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Alcuni parametri dei nodi non possono tornare a un valore predefinito quando non vengono forniti dati al connettore di input. Questo è spesso il caso degli input di Scena.

Collegare gli input del nodo al connettore di output di un altro nodo di tipo corrispondente.

![&#39;Nessun valore di input&#39; soluzione](../../assets/warnings-model-no-input-value.gif "&#39;Nessun valore di input&#39; soluzione")

### Nodo ![(errore)](../../assets/error.svg) non calcolato

Le informazioni fornite al nodo sono incomplete o non valide, pertanto il nodo non è stato in grado di eseguire i calcoli.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Andare a monte nel grafico e verificare la presenza di avvisi attivati da problemi che impediscono ai nodi di fornire un output valido.

![&#39;Nodo non calcolato&#39; soluzione](../../assets/warnings-model-no-input-value.gif "&#39;Nodo non calcolato&#39; soluzione")

### ![(errore)](../../assets/error.svg) I dati a cui si fa riferimento contengono alcuni avvisi

La risorsa a cui fa riferimento un nodo presenta uno o più avvisi. Di seguito sono riportati alcuni nodi che fanno riferimento a una risorsa:

* Un nodo di istanza del grafico fa riferimento a un grafico
* Un nodo di risorse Scena fa riferimento a una risorsa scena 3D bitmap

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Nel pannello Esplora risorse individuare la risorsa a cui si fa riferimento e risolvere tutti gli avvisi generati dalla risorsa:

* Per i grafici, fai riferimento ad altri elementi in questa pagina
* Per qualsiasi altro tipo di risorsa, vedere la pagina Avvisi da dipendenze

![&#39;I dati a cui si fa riferimento contengono alcuni avvisi&#39; soluzione](../../assets/warnings-model-referenced-data.gif "&#39;I dati a cui si fa riferimento contengono alcuni avvisi&#39; soluzione")

### ![(errore)](../../assets/error.svg) Risorsa di riferimento non trovata

Impossibile trovare la risorsa a cui fa riferimento un nodo nel percorso salvato nel file Substance 3D (SBS). Di seguito sono riportati alcuni nodi che fanno riferimento a una risorsa:

* Un nodo di istanza del grafico fa riferimento a un grafico
* Un nodo di risorse Scena fa riferimento a una risorsa scena 3D bitmap

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Per i nodi delle istanze del grafico

Verificare che il grafico di origine esista nel pacchetto che si trova nel percorso salvato nel relativo attributo <b>Package</b>.\
In caso contrario, eliminare il nodo dell&#39;istanza e sostituirlo con un nodo dell&#39;istanza che fa riferimento a un pacchetto valido. In alternativa, puoi ricreare il pacchetto e il grafico a cui fa riferimento il nodo dell&#39;istanza, quindi ricaricare il pacchetto host facendo clic su *RMB* nel pannello [Esplora risorse](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) e selezionando l&#39;opzione <b>Ricarica</b> nel menu di scelta rapida.

Per i nodi delle risorse Scena

Trovare le risorse a cui si fa riferimento nel pannello [Esplora risorse](https://substance3d.adobe.com/documentation/display/DRAFTDESIGNER/.The+Explorer+window+vDraftVersion) e verificarne la presenza nel percorso salvato nell&#39;attributo <b>Percorso file</b>.\
In caso contrario, fare clic su *RMB* sull&#39;elemento della risorsa in Esplora risorse e selezionare <b>Riposiziona...Opzione </b> nel menu di scelta rapida per impostare un nuovo file di destinazione valido per la risorsa.

![&#39;Risorsa di riferimento non trovata&#39; soluzione](../../assets/warnings-model-referenced-resource.gif "&#39;Risorsa di riferimento non trovata&#39; soluzione")

### L&#39;intervallo soft ![(error)](../../assets/error.svg) non contiene il valore

Il valore di default di un parametro esposto non è incluso nell&#39;intervallo soft definito per tale parametro.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Regolate il valore predefinito o l’intervallo morbido in modo che il primo sia incluso nel secondo.

>[!NOTE]
>
> Questo avviso non può essere attivato tramite l&#39;interfaccia utente, poiché *regola automaticamente* l&#39;intervallo soft per includere il valore predefinito. Solo la modifica dei dati nel file Substance 3D (SBS) *direttamente* può attivare questo avviso.

![&#39;L&#39;intervallo soft non contiene il valore&#39; soluzione](../../assets/warnings-model-ranges.gif "&#39;L&#39;intervallo soft non contiene il valore&#39; soluzione")

### ![(error)](../../assets/error.svg) Intervallo sfumato non compreso nell&#39;intervallo consentito

L&#39;intervallo libero di e il parametro esposto non sono interamente inclusi nell&#39;intervallo rigido definito per tale parametro.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Regolate l’intervallo morbido o l’intervallo rigido in modo che il primo sia completamente incluso nel secondo.

>[!NOTE]
>
> Questo avviso non può essere attivato tramite l&#39;interfaccia utente, poiché *regola automaticamente* l&#39;intervallo soft in modo che venga incluso completamente nell&#39;intervallo hard. Solo la modifica dei dati nel file Substance 3D (SBS) *direttamente* può attivare questo avviso.

![&#39;L&#39;intervallo soft non è compreso nell&#39;intervallo hard&#39; soluzione](../../assets/warnings-model-ranges.gif "&#39;L&#39;intervallo soft non è compreso nell&#39;intervallo hard&#39; soluzione")

### Il valore ![(error)](../../assets/error.svg) non è compreso nell&#39;intervallo consentito

Il valore di default di un parametro esposto non è incluso nell&#39;intervallo rigido definito per tale parametro.

<b>![(tick)](../../assets/check.svg) Soluzione</b>

Regolate il valore predefinito o l’intervallo rigido in modo che il primo sia incluso nel secondo.

>[!NOTE]
>
> Questo avviso non può essere attivato tramite l&#39;interfaccia utente, poiché *regola automaticamente* il valore predefinito da includere nell&#39;intervallo rigido. Solo la modifica dei dati nel file Substance 3D (SBS) *direttamente* può attivare questo avviso.

![&#39;Il valore non è compreso nell&#39;intervallo&#39; soluzione](../../assets/warnings-model-ranges.gif "&#39;Il valore non è compreso nell&#39;intervallo&#39; soluzione")
