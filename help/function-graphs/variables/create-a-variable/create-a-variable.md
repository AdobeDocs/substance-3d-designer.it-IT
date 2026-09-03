---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: Scopri come creare variabili personalizzate nei grafici delle funzioni di Substance 3D Designer per valori e parametri riutilizzabili.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creare una variabile
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# Creare una variabile

Esistono diversi modi per creare una variabile in Substance 3D Designer:

* Utilizzo di un parametro di input
* Utilizzare un nodo Set.

## Utilizzo di un parametro di input

Quando create un parametro di input, viene creata e associata una variabile. Potete quindi riutilizzare questa variabile in qualsiasi funzione del grafico.

Pertanto, un singolo parametro esposto può avere un’influenza su più parti del grafico.

## Utilizzo di un nodo Set

Un nodo Set è un nodo disponibile solo nei grafici delle funzioni:

Consente all&#39;utente di creare una variabile personalizzata:

* Il nome viene dichiarato nei parametri.
* Il valore è definito dall&#39;input.

### Come utilizzare il nodo *Set*

L&#39;utilizzo di un nodo Set è un po&#39; particolare:

quando lo dichiarate, è disponibile solo all’interno del grafico, il che per impostazione predefinita non è realmente utile (dopo tutto potete già generare il suo valore con i collegamenti).

Pertanto, è necessario dichiarare questa nuova variabile, al di fuori di questo grafico.

a tale scopo, è necessario utilizzare un nodo di sequenza ed effettuare le seguenti operazioni:

* Collegare il nodo di output effettivo all&#39;input &quot;ultimo&quot; del nodo Sequenza
* Collegare il nodo Set all&#39;input &quot;In&quot; del nodo di sequenza.
* Impostare Sequenza come nodo di output

Dopo aver eseguito questa operazione, la variabile sarà disponibile nell&#39;altro grafico delle funzioni dello stesso nodo.

>[!WARNING]
>
> Quando un nodo viene elaborato dal motore substance, i relativi parametri (e le funzioni che potrebbero controllarli) vengono letti dall&#39;alto verso il basso. Pertanto, un nodo Set può essere accessibile solo dai parametri posizionati sotto di esso nello stack dei parametri del nodo.

>[!NOTE]
>
> Se avete più variabili da creare, ripetete l&#39;operazione di creazione dei nodi *Set* e *Sequence* e impostate l&#39;ultimo nodo di sequenza come nodo di output:
> 
> ![](create-a-variable.resources/create-a-variable-01.png)
