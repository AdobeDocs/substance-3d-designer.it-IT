---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: Utilizzate il nodo Processore vertici tracciati per trasformare e manipolare i vertici dei tracciati con opzioni avanzate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processore vertici tracciati
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Processore vertici tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](paths-vertex-processor.resources/paths-vertex-processor-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica una trasformazione alla posizione dei vertici dei <b>tracciati</b> di input.

Il nodo deve essere utilizzato nel modo seguente:

1. Modificare la funzione <b>Per vertex function </b> parametro;
1. Utilizzare i nodi <b>Get Virgola mobile2</b> per acquisire le variabili *vertex.pos*, *prev.pos* e/o *next.pos*
1. Eseguire alcune operazioni su tali valori (ad esempio, moltiplicarli per ridimensionare i tracciati);
1. Imposta il risultato del calcolo come output.

</td>
</tr>
</table>

Prima di eseguire una query su *prev.pos* o *next.pos*, assicuratevi di impostare i valori <b>vertici precedenti a cui si è effettuato l&#39;accesso</b> e <b>vertici successivi a cui si è effettuato l&#39;accesso</b>\
È inoltre possibile aggiungere immagini di input e campionarle dalla funzione. È necessario prima collegare un input per poterlo campionare dalla funzione. Attenzione, il primo input è *Immagine 1*!\
Puoi anche accedere alle variabili *prev[2].pos* (Virgola mobile 2), *next[2].pos* (Virgola mobile 2), *vertex.corner* (bool) e *path.id* (float).

>[!TIP]
>
> Per gli utenti esperti, la [Specifica formato tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) spiega come i dati dei tracciati vengono codificati in immagini a colori e fornisce suggerimenti per la modifica diretta di questi dati.

>[!NOTE]
>
> Vedere anche [Processore vertici tracciati semplice](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collega questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione *percorso*. |
| <b>Input n. </b> <i>Colore/Scala di grigi</i> | Input per immagini da campionare nella funzione parametro <b>Per vertex function</b>. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | I tracciati trasformati. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Vertici precedenti utilizzati</b> <i>Numero intero</i> | L&#39;utilizzo di questo parametro consente di ottenere la posizione del vertice precedente lungo il percorso (*prev.pos*) e il vertice precedente (*prev[2].pos*) utilizzando i nodi <b>Get</b> nella funzione del parametro <b>Per vertex function</b>. |
| <b>Vertici successivi utilizzati</b> <i>Numero intero</i> | L&#39;utilizzo di questo parametro consente di ottenere la posizione del vertice seguente lungo il percorso (*next.pos*) e il vertice successivo (*next[2].pos*) utilizzando i nodi <b>Get</b> nella funzione del parametro <b>Per vertex function</b>. |
| <b>Conteggio input immagine</b> <i>Numero intero</i> | Numero di connettori di input <b>Input n. </b> visibili per connettere le immagini da campionare nella funzione parametro <b>Per vertex function</b>.<br>Una volta impostati tutti i campioni desiderati, è possibile nascondere i segnaposti inutilizzati riducendo nuovamente il valore di questo parametro su 0. |
| <b>Per vertex function</b> <i>Float2</i> | Funzione applicata a ciascun vertice. Deve restituire la nuova posizione del vertice.<br>Consulta la sezione <b>Descrizione</b> di questa pagina per indicazioni. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 2](paths-vertex-processor.resources/PathsVertexProcessor-Demo2.gif "Esempio di nodo 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
