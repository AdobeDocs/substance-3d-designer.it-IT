---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: Scopri come gestire contenuti e filtri personalizzati nella Libreria di Substance 3D Designer per l'accesso alle risorse organizzate.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gestione di contenuti e filtri personalizzati
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# Gestione di contenuti e filtri personalizzati

In questa pagina viene illustrato il metodo per creare categorie e filtri per la gestione di contenuti personalizzati nella libreria. Include anche suggerimenti per i flussi di lavoro basati su progetti.

## Panoramica

Dopo aver [aggiunto contenuto personalizzato alla libreria](../../../interface/preferences-window/project-settings/project-settings.md), è necessario renderlo *individuabile*.

La libreria utilizza un numero di *coordinate* per l&#39;identificazione del contenuto, per filtrarlo e visualizzare nelle ricerche. Questi dati includono:

* Nome
* Estensione
* URL (ad esempio *nome file*)
* Attributi

Puoi organizzare la tua <b>libreria</b> in categorie contenenti filtri specifici e personalizzarla in base alle esigenze del tuo progetto.\
Le categorie e i filtri personalizzati possono essere *specifici del progetto* e possono essere salvati in [file di progetto](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbsprj). Questi file possono quindi essere assemblati in [file di configurazione](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbscfg) e distribuiti a un team in modo che gli artisti possano utilizzare le* stesse categorie <b>Libreria</b> per qualsiasi progetto specifico.*

Ciò significa che con uno o più file di Project è possibile impostare le cartelle in cui inserire i contenuti da aggiungere alla <b>Libreria</b>, nonché le categorie e i filtri che consentono di ordinare e organizzare tali contenuti.

![Contenuto personalizzato nella libreria](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-01.png "Contenuto personalizzato nella libreria")

## Attributi del grafico

I grafici contenuti nei file [SBS](../../../getting-started/overview/overview.md) e [SBSAR](../../../getting-started/overview/overview.md) possono essere *filtrati e cercati* nella libreria utilizzando il set di dati nella sezione [Attributi](../../../compositing-graphs/graph-parameters/graph-parameters.md) delle proprietà del grafico. Alcuni di questi attributi possono essere impostati anche su altri [tipi di risorse](../../../resources/resources.md).

## Filtri e cartelle personalizzati

I filtri sono semplici parametri di ricerca booleani (True/False) che determinano la visualizzazione di una risorsa all&#39;interno della libreria quando è selezionato <b>Filtro</b>. Le risorse possono essere tutto ciò che è contenuto in un pacchetto. Tenete presente quanto segue:

* Un <b>filtro</b> corrisponderà a tutte le risorse, in *tutti i percorsi controllati*.
* Un <b>filtro</b> può contenere più condizioni, *tutte devono restituire True* (condizione AND) affinché la risorsa venga visualizzata sotto tale filtro.
* Una [risorsa](../../../resources/resources.md) può essere visualizzata in più filtri. Non è *esclusiva* per alcun filtro.
* Una [risorsa](../../../resources/resources.md) da un percorso controllato è *ancora disponibile* nella <b>libreria</b> anche se è *non* in alcun <b>filtro</b>, utilizzando la funzione <b>Ricerca</b>.

### Come creare filtri e cartelle

Le categorie (ad esempio, le cartelle) e i filtri vengono creati e modificati utilizzando i pulsanti riportati di seguito.

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-02.png) Aggiungi cartella:</b> Crea una cartella espandibile nella visualizzazione Libreria. *non puoi* creare sottocartelle.

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-03.png) Aggiungi filtro:</b> Aggiunge un nuovo filtro nella cartella selezionata. *Impossibile* aggiungere filtri alle cartelle predefinite esistenti.

<b>![](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-04.png) Modifica elemento:</b> Modifica la cartella o il filtro attualmente selezionato. L&#39;utente *non può* modificare le proprietà dei filtri e delle cartelle predefiniti.

Per *rimuovere* una cartella o un filtro, *fare clic con il pulsante destro del mouse* su di esso e selezionare l&#39;opzione <b>Rimuovi</b> dal menu di scelta rapida.

### Modifica di filtri e cartelle

<b>Le cartelle</b> e i <b>filtri</b> sono identificati dai seguenti dati:

* <b>Nome</b> visualizzato nella visualizzazione struttura della libreria.
* [File di configurazione del progetto (SBSPRJ)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) in cui è archiviato l&#39;elemento.

>[!WARNING]
>
> È *molto* importante configurarli correttamente, per assicurarti di modificare il *progetto corretto*.

![Edizione filtro personalizzata](managing-custom-content-and-filters.resources/managing-custom-content-and-filters-05.png "Edizione filtro personalizzata")

Per poter utilizzare i filtri di **Filtri**, in genere è necessario configurare *condizioni*. Queste condizioni sono configurate utilizzando i seguenti criteri:

* **Tipo di risorsa**: imposta un [tipo di risorsa](../../../resources/resources.md) specifico, ad esempio [Grafici](../../../compositing-graphs/substance-compositing-graphs.md)
* **Attributo** a cui applicare la condizione - vedere l&#39;elenco precedente
* **Logica della condizione**: consente al filtro di includere risultati con corrispondenze positive, negative, parziali e intere
* **Parola chiave Condition:** la stringa in base alla quale vengono testati i criteri **Attribute** e **Condition logic**. Se non viene specificato alcun valore, vengono incluse tutte le risorse che soddisfano questi due criteri

È possibile *aggiungere o rimuovere* condizioni utilizzando i pulsanti &#39;**+**&#39; e &#39;**x**&#39; all&#39;estrema destra della parola chiave Condition.

>[!NOTE]
>
> Un filtro senza condizioni configurate provocherà la visualizzazione di *tutti* i contenuti della **libreria**.

## Procedure ottimali

### Linee guida consigliate

* La regola generale per la libreria predefinita è <b>Folder</b> elencata nell&#39;attributo <b>Category</b>, mentre il nome <b>Filter</b> è determinato dall&#39;attributo <b>Tag</b>
* Non creare nodi personalizzati che si mescolano con la libreria predefinita, a meno che non lo desideri *esplicitamente*. I nodi *verranno* visualizzati nei filtri predefiniti se corrispondono, quindi sarà necessario utilizzare un *diverso sistema di assegnazione/denominazione* per evitare che ciò si verifichi
* Utilizza gli identificatori *univoci*, *per progetto*. Possono essere inserite ovunque desiderate (ad esempio <b>Descrizione</b>, <b>Categoria</b> o <b>Dati utente</b>), a condizione di essere *coerenti* tra tutti i progetti. Ciò semplifica notevolmente la ricerca e il filtraggio del contenuto *per progetto*
* Utilizzare l&#39;attributo <b>Author</b> per tenere traccia della persona inizialmente responsabile del contenuto, senza dover scorrere i record del controllo della versione
* Un modo efficace di creare <b>icone</b> consiste nell&#39;utilizzare l&#39;opzione <b>Genera</b> dell&#39;attributo grafico [Icona](../../../compositing-graphs/graph-parameters/graph-parameters.md) oppure creare un grafico [modello](../../../interface/preferences-window/project-settings/project-settings.md) per la generazione. In questo modo puoi garantire coerenza e risparmiare il lavoro sulla creazione. Tutte le icone di libreria predefinite sono state create in Designer in questo modo.

### Gestione di contenuti di ambito variabile

* È possibile aggiungere risorse a *categorie esistenti* se questo è più logico. La gestione e la manutenzione dei filtri risulterà meno complessa e sarà possibile utilizzare uno stile di icona speciale per *distinguerli*.
* È possibile definire le cartelle e i filtri in un *file globale* (a livello di studio) [file di configurazione del progetto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) e quindi aggiungervi contenuto semplicemente aggiungendo percorsi controllati da *file consecutivi* [file di progetto](../../../interface/preferences-window/project-settings/project-settings.md)
* È possibile definire cartelle e filtri specifici per *ogni progetto* per mantenerli separati
* È possibile combinare, abbinare e utilizzare i metodi di tutti e tre gli elementi precedenti: utilizzare i filtri esistenti, definire nuovi filtri globali e creare metodi univoci per progetto
