---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Scoprite come funziona FXMaps in Substance 3D Designer per applicare grafici di funzioni alle texture per effetti procedurali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Come funziona
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# Come funziona

Per padroneggiare questa potente funzione è fondamentale capire come funziona un grafico FX-Map.

Un grafico FX-Map può contenere uno o più dei tre tipi di nodo FX-Map: Quadrante, Itera e Switch. Di questi nodi, quello che probabilmente utilizzerete più spesso è il Quadrante, con il nodo di iterazione un secondo vicino.

Il nodo Set di parametri è il primo motore di FX-Maps. Crea l’area centrale su cui si basano le mappe FX del grafico a quattro alberi, ma non viene visualizzata come un’unica area. Visivamente, il grafico a quattro alberi è mostrato sotto forma di una catena di Markov.

Durante il rendering di FX-Map, il grafico semplificato FX-Map viene &quot;srotolato&quot; in modo da assomigliare al grafico ad albero. Il motore &quot;cammina&quot; l&#39;intero quad-albero, lavorando dall&#39;alto verso il basso, quindi da sinistra a destra.

I nodi FX-Map non copiano e incollano le immagini in modo cieco. Quando viene eseguito il rendering di ogni immagine, vengono eseguite tutte le funzioni dinamiche di cui dispone. Le funzioni influiscono su ogni immagine sottoposta a rendering dal nodo. Potete quindi applicare a ogni singola immagine una rotazione casuale, un fattore di scala o una serie di altre regolazioni.
