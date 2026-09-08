---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/substance-compositing-graphs-and-mdl-materials.html"
breadcrumb-title: ''
description: Scoprite come lavorare insieme su grafici di composizione Substance e materiali MDL in Substance 3D Designer per la creazione di materiali.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Substance graphs and MDL materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance grafici e materiali MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 1%

---


# Substance grafici e materiali MDL

In queste pagine sono descritte le sinergie tra i [grafici Substance](../../compositing-graphs/substance-compositing-graphs.md) e i grafici MDL e viene descritto come collegare le texture dagli [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) del grafico Substance agli input del grafico MDL.

## Panoramica

Gli output dei grafici Substance possono essere *passati ai parametri esposti* dei materiali MDL in due modi, descritti in questa pagina.

Se il materiale MDL attualmente applicato nella vista 3D ha parametri esposti il cui tipo è *[variabile](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)* - questo tipo può essere impostato utilizzando l&#39;opzione <b>Modificatore tipo</b> nelle proprietà del [parametro esposto](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), questi possono essere connessi a *texture*:

* un parametro <b>Color</b> può essere collegato alle texture RGBA
* un parametro <b>Float</b> per le texture in scala di grigio

In questi casi, il valore uniforme grezzo è sostituito da un campionatore di texture che fornisce un valore variabile. Questi campionatori hanno un attributo <b>usage</b> definito nel parametro esposto e questo utilizzo consente a Designer di connettere le texture generate dai grafici Substance al parametro appropriato nel materiale MDL, per *utilizzi corrispondenti*.

## Substance grafici nella vista 3D

Quando si utilizza l&#39;opzione <b>Visualizza output in visualizzazione 3D</b> per un grafico a Substance o si trascina un grafico a Substance dal pannello <b>Esplora risorse</b> alla <b>visualizzazione 3D</b>, gli output sono collegati ai parametri esposti di *utilizzi corrispondenti* nel materiale MDL attualmente visualizzato nella visualizzazione 3D.

Le singole texture di un grafico a Substance possono essere collegate a uno qualsiasi dei parametri di materiale MDL che supportano il campionamento delle texture, indipendentemente dall’identificatore, premendo RMB sul nodo del grafico a Substance e trascinando nella vista 3D. Viene visualizzato un elenco degli usi del campionatore disponibili ed è possibile selezionare l’uso di destinazione per la texture selezionata.

![Input grafici MDL esposti](../../assets/mdl-graph-inputs-samplers.png "Input grafici MDL esposti")

*Le texture generate da un grafico a Substance sono collegate ai parametri esposti di un grafico MDL nella vista 3D*

## Substance grafici nei grafici MDL

È possibile inserire le istanze dei grafici delle Substance direttamente nei grafici MDL trascinandole dal pannello <b>Esplora risorse</b> nel grafico MDL. Nei grafici MDL è possibile utilizzare grafici a Substance di <b>file Substance 3D</b> (SBS) e <b>file di risorse Substance 3D</b> (SBSAR).

+++Substance grafico da file Substance 3D (SBS)
![Substance il grafico dal file SBS nel grafico MDL](../../assets/mdl-sbs-instance-hl.png "Substance il grafico dal file SBS nel grafico MDL")



*[Substance istanza grafico](../../compositing-graphs/substance-compositing-graphs.md) da [file Substance 3D](../../getting-started/overview/overview.md) (SBS) nel grafico MDL*

+++

+++Substance grafico da risorsa Substance 3D (SBSAR)
![Substance il grafico dal file SBSAR nel grafico MDL](../../assets/mdl-sbsar-instance-hl.png "Substance il grafico dal file SBSAR nel grafico MDL")



*[Substance istanza del grafico](../../compositing-graphs/substance-compositing-graphs.md) da [risorsa Substance 3D](../../getting-started/overview/overview.md) (SBSAR) nel grafico MDL*

+++

Quando viene creata, l&#39;istanza di un grafico a Substance viene visualizzata come un *nodo* con le caratteristiche seguenti:

* Connettore *di output digitato* per ogni output del grafico. I dati di output vengono digitati come segue:
  * Bitmap RGBA: colore (variabile)
  * Bitmap in scala di grigio: fluttuante (variabile)
  * Valori: corrisponde al tipo di valore (variabile)
* Un *input* di tipo coordinate UV per specificare le coordinate UV da utilizzare per mappare le texture generate dal grafico a Substance. Se non è collegata, il valore predefinito è una classica sfumatura lineare 0-1 in X e Y nello spazio UV
* Il nodo è *etichettato* dopo l&#39;etichetta del grafico a Substance, o l&#39;identificatore se non è definita alcuna etichetta, e il suo primo output bitmap come miniatura

Le proprietà del nodo consentono di modificare *tutte le proprietà dinamiche* del grafico della Substance:

* Dimensioni output
* Seed casuale
* Parametri di input
* ...

Le proprietà del nodo consentono inoltre di impostare i parametri specifici per il modo in cui le texture vengono *mappate* nel materiale MDL:

* Affiancamento
* Usa Dimensioni fisiche
* Formato normale
* Spazio tangente

L&#39;output del nodo dell&#39;istanza del grafico a Substance può essere collegato a qualsiasi input del nodo di tipo corrispondente nel grafico MDL.

Si noti che la modifica di qualsiasi parametro nella sezione <b>Parametri di base SBS</b> comporta la rielaborazione di uno o più output del grafico a Substance, che utilizza il <b>motore a Substance</b> e comporta un *sovraccarico delle prestazioni* oltre ai calcoli del grafico MDL. Si prevede un impatto sulle prestazioni durante la *modifica di un grafico a Substance* che viene installato in un grafico MDL applicato nella vista 3D.

>[!WARNING]
>
> Quando si utilizza un grafico a Substance in un grafico MDL, l’esportazione del grafico MDL comporta la suddivisione degli output del grafico a Substance in bitmap che verranno esportate come texture incluse nel file MDL esportato. Ciò significa che la natura parametrica del grafico della Substance è *persa* nel file MDL esportato.
