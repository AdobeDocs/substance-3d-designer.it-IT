---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Utilizzate il nodo di Elaboratore pixel per elaborare i singoli pixel utilizzando espressioni personalizzate per una manipolazione avanzata della texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elaboratore pixel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Elaboratore pixel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Elaboratore pixel](pixel-processor.resources/comp_pixelprocessor_1.png "Nodo atomico: Elaboratore pixel"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Genera un&#39;immagine in cui il valore di ogni pixel è il risultato del [grafico della funzione Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) specificato.

L’Elaboratore pixel consente di eseguire una funzione personalizzata per ogni pixel restituito come output, su un input opzionale.

È di gran lunga il nodo più versatile, in quanto consente di eseguire qualsiasi operazione matematica e di restituire risultati all&#39;interno del grafico.

</td>
</tr>
</table>

Analogamente a [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md), richiede la configurazione della funzionalità interna per eseguire qualsiasi operazione. L’Elaboratore pixel che differisce da FX-Map è il fatto che non è focalizzato sul posizionamento di pattern, con funzioni multiple che controllano la forma e il posizionamento di un pattern. Viene invece eseguita in parallelo una singola funzione per ogni pixel, in cui ciascun pixel non è a conoscenza dei risultati del calcolo dei pixel vicini.

L&#39;Elaboratore pixel è simile al [Processore di valori](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), che viene eseguito solo su valori singoli e può fornire una buona ottimizzazione rispetto all&#39;Elaboratore pixel.

Per tutti gli utenti abituati a creare le funzioni [shader](../../../../glossary/glossary.md) in editor basati su nodi, l&#39;Elaboratore pixel deve offrire un ambiente familiare.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Nella sezione [Grafici di Substance di esempio](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) di questa documentazione è disponibile un file di progetto annotato che illustra gli usi semplici del nodo di Elaboratore pixel.
> 
> Il nodo [Processore di valori](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) è un buon punto di partenza per conoscere i [grafici delle funzioni Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Tenete inoltre presente che l&#39;utilizzo di questo tipo di grafico e l&#39;esecuzione di operazioni matematiche sono obbligatori per ottenere qualsiasi risultato da questo nodo.
> 
> Ti consigliamo inoltre di familiarizzare con il concetto di [UV](../../../../glossary/glossary.md), [campionamento della texture](../../../../glossary/glossary.md) e vettori.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Metodo colore</b> *Booleano* | Alterna tra un’immagine in scala di grigio e un’immagine a colori in output. |
| <b>Funzione per pixel</b> *Float/Float4* | [Grafico a funzioni Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) valutato per pixel nell&#39;immagine di output.   Utilizzare il nodo [Get Virgola mobile2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) impostato sulla variabile <b>$pos</b> per accedere alla posizione [normalizzata](../../../../glossary/glossary.md) del pixel corrente. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Immagine di input n. </b> *Scala di grigi/Colore* | Utilizzare un nodo [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) o [Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) per accedere ai valori nell&#39;input dell&#39;indice specificato. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
