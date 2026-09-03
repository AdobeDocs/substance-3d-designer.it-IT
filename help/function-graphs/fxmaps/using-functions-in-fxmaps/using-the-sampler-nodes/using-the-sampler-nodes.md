---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: Scoprite come utilizzare i nodi campionatori in FXMaps per campionare le texture e creare variazioni procedurali dei materiali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilizzo dei nodi di Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Utilizzo dei nodi di Sampler

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-01.jpg)

Il nodo del campionatore può essere utilizzato per campionare i valori dei pixel in un input di immagine collegato al nodo della mappa fx. I valori campionati possono quindi essere utilizzati per guidare qualsiasi parametro utilizzando le funzioni.

## Esempio semplice

In questo esempio è stata creata una catena di nodi quadranti per generare una griglia di serie. Viene creata una funzione nel parametro Opacità/Luminanza dell’ultimo quadrante.

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-02.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-03.jpg){width="300px"}

Il nodo Sample accetta un input float2 come coordinate di campionamento (x, y). In questo esempio abbiamo utilizzato la variabile $pos: per ogni pattern, il valore dei pixel viene campionato nella posizione del pattern nel primo input dell’immagine collegato al nodo FxMap.

Il nodo Grigio campione restituisce un valore float1 compreso nell&#39;intervallo 0, 1.

Il nodo Sample Color restituisce un valore float4 (rgba) compreso nell&#39;intervallo 0, 1.

## Esempio avanzato

Qui confrontiamo il valore campionato con una costante (0,3). Se il valore campionato è maggiore di 0,3 la funzione restituisce 1, altrimenti restituisce 0.

![](using-the-sampler-nodes.resources/using-the-sampler-nodes-04.jpg){width="300px"}![](using-the-sampler-nodes.resources/using-the-sampler-nodes-05.jpg){width="300px"}

## Scarica esempio

[![Icona file SBS](using-the-sampler-nodes.resources/using-the-sampler-nodes-06.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
