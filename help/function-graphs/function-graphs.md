---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: Scoprite come creare e utilizzare i grafici delle funzioni Substance in Designer per creare funzioni personalizzate e reti di nodi riutilizzabili.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance grafici delle funzioni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Substance grafici delle funzioni

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](../assets/function-1.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[Substance grafici di funzione](https://substance3d.adobe.com/) <b>elabora valori singoli</b> (interi, mobili, vettori) anziché dati immagine (interi set di pixel). Le funzioni sono anche elementi grafici con reti di nodi, ma i [nodi utilizzati](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)e l&#39;interfaccia sono diversi dai [normali grafici a Substance](../compositing-graphs/substance-compositing-graphs.md). Il flusso di lavoro è completamente basato su <b>operazioni matematiche</b> e non mostra miniature di anteprima delle immagini, il che lo rende un <b>modo di lavorare molto più avanzato</b> con Substance 3D Designer.

Le funzioni possono essere utilizzate in molti contesti diversi, principalmente per modificare il comportamento di [un parametro esposto](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), per creare il comportamento di [Elaboratori pixel](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) o [FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) e per utilizzare [valori nei grafici delle Substance](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

## Esempi

Di seguito sono riportati alcuni esempi di utilizzi comuni per Funzioni.

### Funzione semplice

![](../assets/lerpfunction_1.png)

Funzione semplice nel contesto di un parametro esposto. Ottiene un valore float di input chiamato &quot;Intensità&quot; che è determinato per andare da 0 a 1 (un intervallo facile da capire) e rimappa a un intervallo impostato di 0,1 - 0,8. Ciò significa che se l’utente imposta Intensità su 0, verrà utilizzato internamente 0,1, se l’interfaccia utente è impostata su 1, verrà utilizzato 0,8 e qualsiasi valore intermedio verrà interpolato linearmente. Questo tipo di funzione è in genere utilizzato quando si [espongono parametri](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ma si utilizzano funzioni personalizzate.

Questa funzione potrebbe anche essere scritta come *lerp(0.1, 0.8, Intensità)* in uno pseudocodice simile a HLSL o GLSL.

### Funzione avanzata

![](../assets/pixel-function_1.png){width="545px"}

Questa funzione avanzata mostra il funzionamento interno di un [Elaboratore pixel](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) destinato a regolare la tonalità di un input della mappa colore in base all&#39;intensità di un secondo input della maschera in scala di grigio.

Campiona entrambi gli input con la variabile di Alpha &quot;$pos&quot;, quindi rimuove l’input, converte il valore del colore in HSL e modifica il componente Tonalità moltiplicandolo per il valore della scala di grigi campionata. Successivamente riassembla il vettore, converte nuovamente l&#39;HSL in RGB e aggiunge nuovamente l&#39;Alpha per l&#39;output finale.

nello pseudo-codice questa sarebbe una funzione molto più complicata che non si adatta a una singola riga.
