---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: Utilizza il nodo Itera in FXMaps per creare pattern ripetuti e variazioni di procedurali nei materiali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodo di iterazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# Nodo di iterazione

Il nodo iterato consente di moltiplicare le immagini di un nodo quadrante ed è essenzialmente un nodo &quot;ripetitore&quot;. Un nodo quadrante con una profondità di 1 produce normalmente 4 quadranti. Il nodo Itera consente di ripetere l&#39;immagine di output quante volte vuoi, con ogni set di ripetizioni trattate separatamente.

Il nodo Iterate non dispone di altre proprietà oltre al parametro &quot;Come si desidera eseguire le ripetizioni?&quot;. Di conseguenza, per impostazione predefinita, le nuove immagini vengono semplicemente sovrapposte e fuse con quelle prodotte dal nodo Quadrante.

Il nodo Itera ripete l&#39;immagine di input ricevuta. Il numero di ripetizioni è definito dalla relativa proprietà Iterazioni:

Per utilizzare il nodo iterazione, è importante che vengano elaborate anche tutte le funzioni dinamiche associate a ogni immagine ripetuta. Ciò significa che ogni ripetizione può avere un proprio insieme di regolazioni uniche. È possibile utilizzare la proprietà Numero casuale del nodo iterato per modificare il funzionamento di questa proprietà. È inoltre possibile accedere alla variabile di sistema *$number* all&#39;interno delle funzioni dinamiche per determinare quale ripetizione viene attualmente sottoposta a rendering e modificare di conseguenza il risultato della funzione.

Ad esempio, se applicate una rotazione casuale a ogni immagine in un nodo Quadrante, quindi inviate l’output di quel nodo Quadrante all’input attivo di un nodo Iterato, ciascuna delle immagini ripetute avrà anche una propria rotazione casuale.

Tutte le stesse funzionalità dinamiche disponibili sul nodo Quadrante si applicano anche alle immagini ripetute prodotte dal nodo Iterate. È come se il nodo avesse duplicato il nodo Quadrante allo stesso livello, invece di aggiungere un altro livello di profondità.

## Connettore pass-through

Ogni nodo iterato ha due connettori lungo la sua base. Il connettore sinistro è un connettore pass-through. L’immagine ricevuta viene passata direttamente al connettore di output del nodo, dove viene fusa con eventuali immagini ripetute:

L’immagine pass-through viene sempre passata inalterata, indipendentemente dall’Iterazione del parametro.

![](the-iterate-node.resources/the-iterate-node-01.jpg)
