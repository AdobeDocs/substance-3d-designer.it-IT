---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/best-practices/graph-creation-etiquette.html"
breadcrumb-title: ''
description: Scopri le best practice e le convenzioni per la creazione di grafici Substance per garantire flussi di lavoro puliti, gestibili ed efficienti.
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Graph Creation Etiquette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Convenzioni per la creazione di grafici
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1163'
ht-degree: 0%

---


# Convenzioni per la creazione di grafici

La creazione di grafici complessi e di grandi dimensioni può creare rapidamente confusione e rendere difficile la navigazione. Per risolvere questi problemi, è possibile utilizzare diversi strumenti e utilizzare alcune buone abitudini, per evitare problemi in un secondo momento. Questa pagina fornisce un elenco conclusivo delle tecniche che consigliamo di utilizzare per ottenere grafici puliti, efficienti e funzionali che siano facilmente condivisi e compresi.

## Generale

### Organizzazione grafico

#### Elementi grafico

Gli elementi del grafico sono oggetti di supporto che possono essere posizionati accanto e intorno ai nodi nella [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md). Dei tre, il Fotogramma offre i vantaggi più rapidi e maggiori, mentre il Segnaposto Commenti e Navigazione è più adatto a scenari specifici.

#### Fotogrammi

La prima cosa che porta a grafici più puliti e facili da leggere è la posizione dei Fotogrammi attorno ai gruppi centrali del tuo grafico. Senza Fotogrammi, un grande grafico è quasi illeggibile, e anche i grafici piccoli diventano molto più facili da capire una volta disegnati i fotogrammi. Un grande vantaggio dei Fotogrammi è che i loro nomi <b> vengono sempre visualizzati con la stessa scala</b>, anche se si esegue uno zoom indietro molto lontano.

![Fotogrammi nei grafici a Substance](graph-creation-etiquette.resources/graph-creation-etiquette-01.gif "Fotogrammi nei grafici a Substance")

I fotogrammi facilitano la comprensione di ciò che accade in un grafico. Possono aiutarti, in qualità di autore, a tornare al tuo lavoro mesi dopo o di un altro utente, ad esempio un collega, a trovare la loro strada in un Grafico a cui non sono abituati.

Per posizionare i Fotogrammi, utilizzate i seguenti criteri:

* Identificare **blocchi di funzionalità** (ad esempio, 8 nodi che insieme creano un effetto dirt) e raggrupparli utilizzando Fotogrammi.
* Prova sempre a **usare colori diversi** per i tuoi Fotogrammi: i Fotogrammi con lo stesso colore blu predefinito non si distinguono molto l&#39;uno dall&#39;altro.
* Utilizzare **nomi chiari e descrittivi** che non siano eccessivamente lunghi (vedere la sezione seguente per ulteriori suggerimenti)
* Non mettere **troppo o troppo poco** in un Fotogramma, perché questo non aiuta la leggibilità. La quantità esatta differisce ovviamente tra i grafici e la funzionalità.
* Se necessario, **aggiungi testo nella descrizione** per comprendere cosa succede in un fotogramma.

#### Commenti e Segnaposti

Commenti e segnaposti sono secondari solo ai Fotogrammi e non sono un must assoluto per grafici ben scritti. Possono essere utilizzati nei seguenti scenari:

* I commenti sono utili per aggiungere testo aggiuntivo oltre a quanto consentito dalla descrizione di una cornice. Potete aggiungere piccoli bit di testo per nodo, principalmente per piccole informazioni dettagliate. I commenti non vengono ridimensionati correttamente e non leggono da un livello di zoom a distanza.
* I perni di navigazione consentono di scorrere aree specifiche del grafico utilizzando la scelta rapida F2. Questo può essere utile per i grafici molto grandi in cui spesso è necessario saltare tra due aree che sono molto distanti tra loro.

### Posizionamento di input e output

Gli ingressi e le uscite devono essere posizionati alle estremità dei grafici: tutti gli output a destra, tutti gli input a sinistra, ciascuno allineato verticalmente. In questo modo è più facile trovarli e identificarli.

![Posizionamento di input e output](graph-creation-etiquette.resources/graph-creation-etiquette-02.gif "Posizionamento di input e output")

L&#39;esempio precedente è un caso estremo: i fotogrammi non sono sempre necessari o possibili, ma dovrebbe essere chiaro che l&#39;allineamento verticale di In e Output è molto più chiaro rispetto al posizionamento casuale e casuale.

### Reindirizzamento collegamento

Nei grafici di grandi dimensioni e molto lunghi, a volte i collegamenti vengono creati su un&#39;estensione molto ampia. Questo porta a confondere i fili di collegamento che attraversano il grafico senza molto controllo. La scelta rapida &quot;Alt + Maiusc trascina&quot; consente di riorganizzare questi collegamenti, reindirizzandoli su un percorso diverso suddividendo un collegamento e aggiungendo una maniglia aggiuntiva al centro. Si raccomanda di utilizzare questa opzione in scenari in cui abbia senso.

![Reindirizzamento collegamento](graph-creation-etiquette.resources/graph-creation-etiquette-03.gif "Reindirizzamento collegamento")

### Etichetta, identificatore e utilizzo

Qualsiasi grafico progettato per la condivisione o la pubblicazione deve essere accuratamente inserito nei metadati aggiuntivi per migliorare la facilità d’uso. I punti seguenti sono importanti:

Le etichette consigliate predefinite non sono mai sufficienti, prendetevi il tempo e l&#39;impegno necessari per aggiungere etichette personalizzate ai parametri esposti e agli input e output.

![Identificatore ed etichetta](graph-creation-etiquette.resources/graph-creation-etiquette-04.png "Identificatore ed etichetta")

Cercare di non avere identificatore e Label differiscono troppo: nel caso in cui l&#39;identificatore venga utilizzato altrove (in più funzioni) può essere molto difficile trovare quale proprietà dell&#39;interfaccia utente è correlata a quale variabile.

![Chiarezza dell&#39;identificatore](graph-creation-etiquette.resources/graph-creation-etiquette-05.png "Chiarezza dell&#39;identificatore")

Cercate di far corrispondere le Etichette ai termini utilizzati in Cornici (Etichette cornice) e nei commenti. Semplifica la ricerca della sezione del grafico collegata al parametro esposto

![Etichette fotogramma e parametro corrispondenti](graph-creation-etiquette.resources/graph-creation-etiquette-06.png "Etichette fotogramma e parametro corrispondenti")

### Impostazioni parametri

Quando si espongono i parametri, è importante non solo l&#39;etichetta e l&#39;Identificatore, ma tenere presente quanto segue:

* Scegli il tipo di editor corretto. Un cursore potrebbe non avere sempre senso: un elemento Interfaccia Angolo o Dropdown sono anche possibilità.
* Impostate i valori Min e Max appropriati e decidete se è opportuno applicare il bloccaggio.
* Scegliete un valore predefinito sensato: i valori predefiniti che non servono più a nulla, e i risultati delle analisi dei bordi devono essere evitati.
* Considerate la possibilità di modificare l&#39;intervallo tramite una [Funzione](../../function-graphs/function-graphs.md)se necessario: un cursore compreso tra 0,125 e 0,357 non ha alcun senso, potete facilmente rimappare con un&#39;interpolazione lineare e fare in modo che l&#39;elemento dell&#39;interfaccia utilizzi un intervallo da 0 a 1.

## Grafici Substance

### Gestione del colore e della scala di grigi

Quando si utilizzano i dati a colori e in scala di grigi, è necessaria una grande cautela e non si possono combinare facilmente entrambi i tipi di dati al volo. È opportuno tenere presenti i seguenti punti:

* I grafici non devono mai contenere collegamenti punteggiati rossi (di errore).
* Non dovrebbero verificarsi inutili conversioni tra colore e scala di grigi e viceversa. In alcuni casi, il &quot;nodo di conversione automatico colore/scala di grigi&quot; nelle preferenze del grafico può portare a catene lunghe e inutili di nodi di conversione ancorati.
* I dati vengono conservati in scala di grigi il più a lungo possibile e convertiti solo quando assolutamente necessario. Ciò riduce la complessità e consente di risparmiare sulle prestazioni.
* Gli input e gli output devono essere creati o impostati tenendo presente il tipo corretto: ad esempio, non ha senso avere un input &quot;maschera&quot; impostato sul colore se verrà convertito in scala di grigi per l&#39;uso come maschera binaria.

![Conversioni in scala di colore e di grigio](graph-creation-etiquette.resources/graph-creation-etiquette-07.png "Conversioni in scala di colore e di grigio")

### Controllo della risoluzione

Il controllo della risoluzione di un [grafico della Substance](../../compositing-graphs/substance-compositing-graphs.md) può creare confusione, pertanto è necessario prestare attenzione a eseguire correttamente questa operazione. Gli errori possono compromettere gravemente le prestazioni o produrre risultati inutilizzabili di scarsa qualità.

[Per comprendere appieno questo argomento, assicurati di conoscere le dimensioni di output assolute e relative.](../../compositing-graphs/output-size/output-size.md)

* Un grafico dovrebbe essere impostato sulla risoluzione &quot;Relativa alla principale&quot; in quasi tutti i casi, a meno che non ci sia un&#39;eccezione molto specifica dove non è richiesto (molto raro).
* I nodi in genere non dovrebbero avere impostazioni di esclusione per le dimensioni di output. Nella maggior parte dei casi, la risoluzione è controllata al meglio tramite le proprietà Padre o Grafico.
* Per le bitmap, è necessario impostare con particolare attenzione il fatto che le dimensioni di output assolute predefinite non si estendano a tutto il grafico, ma che vengano sostituite da Relative a Parent. Si tratta di una delle poche eccezioni alla regola di cui sopra.
