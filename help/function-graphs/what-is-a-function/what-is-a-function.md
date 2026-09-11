---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Scopri quali funzioni sono disponibili in Substance 3D Designer e come utilizzarle per creare reti di nodi riutilizzabili.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'Che cos''è una funzione '
user-guide-description: ''
user-guide-title: ''
source-git-commit: baf36ab85717512cc9e52d67d00293eabb5ebcf6
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Che cos&#39;è una funzione?

Funzioni in Substance 3D Designer consente all&#39;utente di generare risultati utilizzando la logica che altrimenti si troverebbe in un linguaggio di programmazione.

Ma invece di usare le linee di codici, le funzioni in Designer mantengono lo stesso approccio nodale. A prima vista, un grafico a funzioni sembra molto simile a un grafico regolare.

![](what-is-a-function.resources/image2015-12-17-18-19-37.png)

È possibile incontrare funzioni in 2 casi principali:

* per controllare il risultato di un parametro
* se modificate un elaboratore pixel

## Controllare il risultato di un parametro

In Substance 3D Designer, qualsiasi parametro può essere controllato da una funzione.

![](what-is-a-function.resources/image2015-12-17-21-3-46.png)

Potete quindi immaginare regole e dipendenze tra le parti del grafico, per ottenere risultati unici.

Ad esempio, potete decidere che l’opacità di un nodo di blend sia pari alla metà dell’intensità di un nodo di alterazione:

![](what-is-a-function.resources/warpblend.gif)

In effetti, è possibile che l&#39;utente abbia già creato funzioni senza esserne a conoscenza:

se è stato esposto un parametro, è stata creata automaticamente una funzione e una variabile: la funzione contiene un nodo float get che rileva il valore della variabile appena creata:

![](what-is-a-function.resources/expose.gif)
