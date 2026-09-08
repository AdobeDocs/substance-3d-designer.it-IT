---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Scoprite i metodi di fusione disponibili in Substance 3D Designer per combinare le texture con diversi effetti di composizione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metodi fusione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# Metodi fusione

Il nodo [Fusione](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) offre i seguenti metodi di fusione:

## Copia

Il metodo di fusione *Copia* posizionerà il primo piano sopra lo sfondo.

![Metodo fusione: Copia](../../../../../assets/image2015-8-20-9-38-0.png "Metodo fusione: Copia"){zoomable="yes"}

Per le immagini a colori, il canale alfa viene considerato per impostazione predefinita nell’opacità.

Questo può essere modificato utilizzando il parametro &quot;Fusione Alpha&quot;.

![Metodo di fusione: Copia (2)](../../../../../assets/image2015-8-20-14-15-29.png "Metodo di fusione: Copia (2)"){zoomable="yes"}

## Aggiungi (Scherma lineare)

Il metodo di fusione *Aggiungi* aggiungerà il valore di input in primo piano a ciascun pixel corrispondente sullo sfondo.

![Metodo fusione: Aggiungi (Scherma lineare)](../../../../../assets/image2015-8-20-9-38-19.png "Metodo fusione: Aggiungi (Scherma lineare)"){zoomable="yes"}

## Sottrai

Il metodo di fusione *Substract* sottrarrà il valore dell’input in primo piano da ogni pixel corrispondente sullo sfondo.

Se il risultato della substrazione è inferiore a 0, il valore viene limitato a 0, ottenendo il nero puro.

![Metodo fusione: Substract](../../../../../assets/image2015-8-20-9-38-35.png "Metodo fusione: Substract"){zoomable="yes"}

## Moltiplica

Il metodo di fusione *Moltiplica* moltiplicherà il valore di input dello sfondo per ogni pixel corrispondente in primo piano.

Poiché il valore di ciascun pixel è compreso tra 0 e 1, il risultato è sempre uguale o inferiore (più scuro) rispetto all’originale.

![Metodo fusione: Moltiplica](../../../../../assets/image2015-8-20-9-38-53.png "Metodo fusione: Moltiplica"){zoomable="yes"}

## Aggiungi sub

Il metodo di fusione *Aggiungi sub* funziona come segue:

* I pixel in primo piano con un valore superiore a 0,5 vengono aggiunti ai rispettivi pixel di sfondo.
* I pixel in primo piano con un valore inferiore a 0,5 vengono sottratti dai rispettivi pixel di sfondo.

![Metodo di fusione: Aggiungi metodo di fusione secondario](../../../../../assets/image2015-8-20-9-39-11.png "Metodo di fusione: Aggiungi metodo secondario"){zoomable="yes"}

## Max (Schiarisci)

Il metodo di fusione *Max* selezionerà il valore più alto tra lo sfondo e il primo piano.

![Metodo fusione: Max (Schiarisci)](../../../../../assets/image2015-8-20-9-40-12.png "Metodo fusione: Max (Schiarisci)"){zoomable="yes"}

## Min (Scurisci)

Il metodo di fusione *Min* selezionerà il valore più basso tra lo sfondo e il primo piano.

![Metodo di fusione: Min (scurisci)](../../../../../assets/image2015-8-20-9-40-31.png "Metodo di fusione: Min (scurisci)"){zoomable="yes"}

## Cambia

Il metodo di fusione *Switch* è simile al metodo di copia, con una differenza *cruciale*:

* &#39;Opacità&#39; impostata su 0: il flusso di nodi connessi all&#39;input &#39;In primo piano&#39; *non verrà calcolato*.
* &#39;Opacità&#39; impostata su 1: il flusso di nodi connessi all&#39;input &#39;Background&#39; *non verrà calcolato*.

Pertanto, questa modalità può essere utilizzata per migliorare le prestazioni del grafico.

I nodi [Switch](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) e [Switch scala di grigi](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md) sono configurati per utilizzare i nodi di fusione in queste configurazioni specifiche.

![Metodo fusione: Cambia](../../../../../assets/image2015-8-20-9-38-0.png "Metodo fusione: Cambia"){zoomable="yes"}

## Dividi

Il metodo di fusione *Dividi* dividerà il valore dei pixel di input dello sfondo per ogni pixel corrispondente in primo piano.

![Metodo fusione: Dividi](../../../../../assets/image2015-8-20-9-41-32.png "Metodo fusione: Dividi"){zoomable="yes"}

## Sovrapposizione

Il metodo di fusione *Sovrapposizione* combina i metodi di fusione Moltiplica e Scherma:

* 
  * Se il valore del pixel del livello inferiore è inferiore a 0,5, viene applicata una fusione di tipo *Moltiplica*
  * Se il valore del pixel del livello inferiore è superiore a 0,5, viene applicata una fusione di tipo *Schermo*

![Metodo fusione: Sovrapposizione](../../../../../assets/image2015-8-20-9-41-50.png "Metodo fusione: Sovrapposizione"){zoomable="yes"}

## Scolora

Con il metodo di fusione Schermo i valori dei pixel nei due input vengono invertiti, moltiplicati e quindi invertiti di nuovo.

Il risultato è l’effetto opposto a quello della moltiplicazione ed è sempre uguale o superiore (più chiaro) rispetto all’originale.

![Metodo fusione: Schermo](../../../../../assets/image2015-8-20-9-42-11.png "Metodo fusione: Schermo"){zoomable="yes"}

## Luce soffusa

Il metodo di fusione Luce soffusa crea un risultato leggermente più chiaro o più scuro a seconda della luminosità del colore di primo piano.

La fusione di colori con luminosità superiore al 50% schiarirà i pixel di sfondo e i colori con luminosità inferiore al 50% scurirà i pixel di sfondo.

![Metodo di fusione: luce soffusa](../../../../../assets/image2015-8-20-9-42-32.png "Metodo di fusione: luce soffusa"){zoomable="yes"}
