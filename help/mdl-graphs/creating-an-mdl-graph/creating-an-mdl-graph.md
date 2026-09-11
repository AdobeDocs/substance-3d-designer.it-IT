---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Scoprite come creare grafici del linguaggio di definizione dei materiali in Substance 3D Designer per la creazione di materiali personalizzati.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creazione di un grafico MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2a6e26cc03e887569a518cadd171ae1b51ae6abd
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# Creazione di un grafico MDL

Questa pagina descrive il processo di creazione di un grafico MDL per creare materiali MDL in Substance 3D Designer.

![Percorsi per la creazione di grafici MDL](creating-an-mdl-graph.resources/mdl-new-graph-hl.png "Percorsi per la creazione di grafici MDL")

*Percorsi per la creazione di un nuovo grafico MDL nell&#39;interfaccia di Designer*

## Metodi per la creazione di un grafico MDL

Potete creare un grafico MDL utilizzando uno dei seguenti metodi:

* Seleziona l&#39;opzione **File > Nuovo > Grafico MDL** nella *barra dei menu principale*
* Fai clic sul pulsante ![](creating-an-mdl-graph.resources/mdl-new-graph-icon.png) **Aggiungi grafico MDL** nella *barra degli strumenti principale*
* Fate clic con il pulsante destro del mouse su un *pacchetto esistente* nel pannello **Esplora risorse** e selezionate l&#39;opzione **Nuovo > Grafico MDL**

Verrà visualizzata la finestra di dialogo **Nuovo grafico MDL**, vedere di seguito.

![Finestra di dialogo Nuovo grafico MDL](creating-an-mdl-graph.resources/mdl-templates.png "Finestra di dialogo Nuovo grafico MDL")

*Finestra di dialogo Nuovo grafico MDL*

## Finestra di dialogo Nuovo grafico MDL

Indipendentemente dal metodo utilizzato per creare un nuovo grafico MDL, verrà sempre visualizzata la finestra di dialogo <b>Nuovo grafico MDL</b> che consente di configurare il nuovo grafico.

### Modelli

La sezione <b> modelli</b> consente di selezionare un modello di grafico, che include nodi preconfigurati per iniziare a utilizzare il grafico più rapidamente. I nodi preconfigurati includono nodi di output, nodi semplici per passare i valori a questi output, ad esempio Colore uniforme e nodi di input a seconda del modello.

Per iniziare da un grafico *vuoto*, selezionate il modello <b>Vuoto</b>.

L&#39;opzione <b>Progetto</b> consente di filtrare l&#39;elenco dei modelli in base al file di progetto. In questo modo è più semplice trovare i modelli personalizzati nelle posizioni aggiunte nella sezione <b>Generali</b> delle impostazioni del progetto per il file di progetto.

>[!WARNING]
>
> Se selezioni il modello errato, *non puoi* passare a un modello diverso dopo aver creato il grafico.\
> Per trasferire il grafico esistente a un altro modello, potete creare un nuovo grafico utilizzando il modello appropriato e copiare e incollare il grafico in quello nuovo. Riconnettere i nodi come appropriato, incluso il nodo [radice](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md).

L&#39;elenco dei modelli può essere visualizzato in modalità diverse utilizzando i *pulsanti* accanto alla casella combinata **Progetto**:

* **![](creating-an-mdl-graph.resources/mdl-template-recent-icon.png)Visualizzazione utilizzata di recente**: consente di filtrare l&#39;elenco per visualizzare gli ultimi modelli utilizzati nell&#39;ordine *dal più recente al meno recente*. L&#39;elemento principale è il più recente.
* **![](creating-an-mdl-graph.resources/mdl-template-graphs-icon.png)grafici di visualizzazione**: i modelli vengono visualizzati solo dalla relativa *etichetta*, nell&#39;ordine dei [file Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) nella directory dei modelli
* **![](creating-an-mdl-graph.resources/mdl-template-packages-icon.png)Visualizza file Substance 3D**: i modelli vengono visualizzati dalla relativa etichetta come *elementi secondari del file Substance 3D a cui appartengono*, nell&#39;ordine dei file nella directory dei modelli
* **![](creating-an-mdl-graph.resources/mdl-template-directory-icon.png)directory di visualizzazione**: i modelli vengono visualizzati dalla relativa etichetta come *figli della directory a cui appartengono*, nell&#39;ordine dei file nella directory dei modelli

### Proprietà

La sezione <b>Proprietà grafico </b> consente di impostare le informazioni di base relative al nuovo grafico. Ognuno di questi può essere modificato in qualsiasi momento, ma è opportuno prestare attenzione in un primo momento e configurarli in modo appropriato per il proprio caso di utilizzo.

* <b>Nome grafico</b>: identificatore del grafico. Deve essere univoco per un determinato pacchetto e non può includere spazi e alcuni caratteri speciali.
* <b>Crea un grafico nel pacchetto</b>: è possibile utilizzare questa casella combinata per creare un *nuovo* pacchetto per il nuovo grafico o aggiungere il nuovo grafico a qualsiasi pacchetto *esistente* già caricato nel pannello Esplora risorse.\
  Nota: se il processo di creazione viene avviato utilizzando il metodo <b>4</b> (vedere sopra), questo parametro è *predefinito* rispetto al pacchetto esistente da cui è stato avviato il processo.
* <b>Dettagli modello</b>: questa sezione contiene un breve testo che illustra le caratteristiche e lo scopo del modello
