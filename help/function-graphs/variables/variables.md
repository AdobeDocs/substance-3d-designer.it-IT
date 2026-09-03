---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Scoprite come utilizzare le variabili nei grafici delle funzioni di Substance 3D Designer per memorizzare e riutilizzare i valori in modo efficiente.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variabili
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Variabili

>[!NOTE]
>
> Per informazioni sulla creazione e sull&#39;utilizzo dei nodi delle variabili, fare riferimento alla *[sezione Nodi delle variabili](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*.

## Definizione

Se avete poca conoscenza nella programmazione, potreste avere familiarità con il concetto di variabile.

In caso contrario, si tratta di una definizione semplice:

>[!NOTE]
>
> Una variabile è solo un &quot;contenitore&quot; con un nome specifico che contiene un valore.
> 
> È possibile utilizzare il valore contenuto in una variabile chiamandola con il relativo nome.

## Tipi di variabili

In Substance 3D Designer avete due famiglie di variabili: Numerica e Booleano.

## Variabili numeriche

Le variabili numeriche sono fondamentalmente numeri. Ma facciamo una netta distinzione tra due tipi di numeri:

* Interi : 0 | 1 | -1 | 203568 , ecc.
* Virgole mobili: 0,23 | 1,0 | -0,3546 | ecc.

>[!WARNING]
>
> Designer distingue chiaramente i numeri interi dai numeri a virgola mobile: per impostazione predefinita, non è possibile utilizzarli insieme.
> 
> È possibile utilizzare i nodi *To Integer* o To Virgola mobile per eseguire conversioni di tipi.

### Più valori numerici nella stessa variabile

A seconda delle esigenze, è possibile accumulare fino a 4 valori numerici all&#39;interno della stessa variabile.

Ancora una volta tutti i valori devono essere dello stesso tipo.

A tale scopo, è possibile scegliere tra tutti i seguenti valori numerici:

![](variables.resources/variables-01.png)

## Booleano

Un valore booleano è un valore binario puro, il che significa che il suo valore può essere solo *True* o *False* (puoi anche dire 0 o 1).
