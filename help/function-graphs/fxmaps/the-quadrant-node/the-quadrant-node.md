---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/fxmaps/the-quadrant-node.html"
breadcrumb-title: ''
description: Utilizzate il nodo Quadrante in FXMaps per dividere le texture in quattro sezioni per creare pattern e variazioni affiancate.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Quadrant Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodo quadrante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 2%

---


# Nodo quadrante

Molte FX-Maps sono costituite interamente da catene di nodi quadranti. I nodi quadranti sono i nodi più potenti e flessibili del gruppo FX-Map, quindi vale la pena capire come funziona questo nodo.

La cosa più importante dei nodi quadranti è che sono l&#39;unico nodo in grado di aumentare la profondità o *ottava* del grafico FX-Map. Ogni nodo del quadrante viene aggiunto al grafico del quadrialbero sottostante, mentre nessuno degli altri nodi lo fa.

Il nodo Quadrante dispone di un numero di parametri:

## Colore/Luminosità

Quando il nodo aggiunge un’immagine alla FX-Map, queste impostazioni definiscono il modo in cui i canali vengono fusi con altre immagini nella catena. I parametri *Colore/Luminosità* si applicano a tutte le immagini renderizzate da questo particolare nodo.

### Scostamento ramo

Modifica l&#39;immagine del nodo. Lo scostamento viene applicato a tutte le altre immagini sottoposte a rendering dai nodi successivi nel grafico. L&#39;offset di diramazione applica la traslazione al nodo quadrante corrente e a tutti i nodi sottostanti nella stessa diramazione del grafico.

Questo parametro può essere controllato con una funzione dinamica.

### Motivo

Definisce l’immagine (se presente) da aggiungere alla mappa FX da questo nodo.

I nodi quadranti supportano un lungo elenco di modelli, descritti più avanti in questo argomento.

>[!WARNING]
>
> Impossibile controllare questo parametro con una funzione dinamica in un file sbsar.

### Scostamento pattern

Sposta l&#39;immagine del nodo in base alla quantità specificata, ma non influisce sui nodi successivi. Questo parametro può essere controllato con una funzione dinamica.

### Dimensioni pattern

Definisce le dimensioni dell’immagine (se applicabile) da aggiungere alla FX-Map. Questo parametro può essere controllato con una funzione dinamica.

### Rotazione pattern

Definisce la rotazione dell’immagine (se applicabile) da aggiungere alla FX-Map. Questo parametro può essere controllato con una funzione dinamica.

### Variazione pattern

Alcuni pattern hanno varianti. Questa impostazione consente di scegliere la variante da utilizzare. Questo parametro può essere controllato con una funzione dinamica.

### Metodo fusione

Specifica il processo di fusione da utilizzare quando si mixa l&#39;immagine di questo nodo (se applicabile) nell&#39;immagine FX-Map. Questo parametro può essere controllato con una funzione dinamica.

### Seme casuale

Valore di inizializzazione per il generatore di numeri casuali.

Il generatore usa questo seme come punto di partenza, creando una sequenza di quelli che sembrano essere numeri casuali. Il vantaggio di questo approccio è che, a differenza del mondo reale, potete garantire che venga generata ogni volta la stessa sequenza di numeri casuali, producendo risultati prevedibili, ripetibili, ma dall&#39;aspetto casuale.

Questo parametro può essere controllato con una funzione dinamica.

### Eredita casuale

Se impostato su &quot;Sì&quot;, il valore di inizializzazione del generatore di numeri casuali viene ereditato dal nodo precedente nel grafico (ovvero il nodo sopra questo nell&#39;albero quadruplo). Se questo è il primo nodo, il valore di inizializzazione casuale viene ricavato dal [grafico Substance](../../../compositing-graphs/substance-compositing-graphs.md) che lo contiene.

## Pattern

Ogni nodo Quadrante può aggiungere facoltativamente un’immagine alla FX-Map finale.

Per impostazione predefinita, l’opzione Nessun pattern è selezionata e quindi non viene eseguito il rendering dell’immagine. Il nodo Quadrante si limita a suddividere l’immagine FX-Map, dividendola in quattro per il nodo successivo nella catena.

L&#39;opzione successiva, *Immagine di input*, consiste nell&#39;utilizzare un&#39;immagine fornita al nodo FX-Map. Il nodo FX-Map accetta immagini a colori o in scala di grigi da utilizzare come sfondo o in sostituzione di uno dei pattern incorporati. Si noti che il nodo Quadrante può eseguire il rendering solo di un&#39;immagine di input in scala di grigio in una mappa Fx in scala di grigio e viceversa, può eseguire il rendering solo di un&#39;immagine di input colore in una mappa FX a colori. Se vuoi miscelare il tipo di colore, devi convertire gli input prima nel grafico.

Infine, potete scegliere tra uno dei modelli incorporati: Quadrato, Disco, paraboloide, Campana, Gaussiano, Spina, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Mezzaluna e Capsula.

Nota aggiuntiva: è possibile creare una funzione dinamica in questo parametro, ma funzionerà solo in Substance 3D Designer. Per accedere all&#39;input dell&#39;immagine con una funzione dinamica, è necessario utilizzare valori compresi tra 256 (voce immagine 1) e valori superiori (257 per voce immagine 2, ecc.).

### Tipi di pattern.

I pattern sono tutti in scala di grigi. Alcuni possono essere leggermente modificati utilizzando il parametro *Variazione pattern*.

Molti dei pattern incorporati hanno una forma di riempimento sfumatura radiale o simile. Ciò li rende molto utili per molti tipi di rumori e pattern. Altri motivi, come Mattone, Disco e Quadrato, sono forme semplici e piatte.

Il parametro Variazione serie (Pattern Variation) regola una feature definita della serie.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/the-quadrant-node-01.png){width="80px"}

</td>
<td style="border: 0;" valign="top">

![](the-quadrant-node.resources/the-quadrant-node-02.jpg)

</td>
</tr>
</table>
