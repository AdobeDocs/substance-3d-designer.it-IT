---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: Utilizzate il nodo Semplice processore vertici tracciati per elaborare i vertici dei tracciati con opzioni di trasformazione semplificate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processore vertici tracciati semplice
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Processore vertici tracciati semplice

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica una trasformazione alla posizione dei vertici dei <b>tracciati</b> di input.

1. Modificare la funzione del parametro <b>Per vertex function</b>;
1. Utilizzare un nodo <b>Get Float2</b> per la variabile *vertex.pos*;
1. Eseguire alcune operazioni su questo valore (ad esempio, moltiplicarlo per ridimensionare i tracciati);
1. Imposta il risultato del calcolo come output.

</td>
</tr>
</table>

È possibile utilizzare immagini di input e campionarle dalla funzione. È necessario prima collegare un input per poterlo campionare dalla funzione. Attenzione, il primo input è *Immagine 1*!\
Puoi anche accedere alle variabili *vertex.corner* (bool) e *path.id* (float).

>[!TIP]
>
> Per gli utenti esperti, la [Specifica formato tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) spiega come i dati dei tracciati vengono codificati in immagini a colori e fornisce suggerimenti per la modifica diretta di questi dati.

>[!NOTE]
>
> Vedere anche [Processore vertici tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | Un elenco di percorsi dei segmenti codificati. Collegare questo input al risultato di una [maschera ai percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) o a un altro nodo di elaborazione dei percorsi. |
| <b>Input n. </b> <i>Colore/Scala di grigi</i> | Input per immagini da campionare nella funzione parametro <b>Per vertex function</b>. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Tracciati</b> <i>Colore</i> | I Tracciati Trasforma. Potete utilizzare [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) per avere un&#39;idea di ciò che rappresenta il risultato, utilizzare un altro nodo di elaborazione tracciati o inserirlo in un [Tracciati da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Conteggio input immagine</b> <i>Numero intero</i> | Numero di connettori di input <b>Input n. </b> visibili per connettere le immagini da campionare nella funzione parametro <b>Per vertex function</b>.<br>Una volta impostati tutti i campioni desiderati, è possibile nascondere i segnaposti inutilizzati riducendo il valore di questo parametro a 0.<br>Se sono necessari altri input, utilizzare in alternativa [il processore vertici percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). |
| <b>Per vertex function</b> <i>Virgola mobile 2</i> | Funzione applicata a ciascun vertice. Deve restituire la nuova posizione del vertice.<br>Consulta la sezione <b>Descrizione</b> di questa pagina per indicazioni. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 2](paths-vertex-processor-simple.resources/PathsVertexProcessor-Demo2.gif "Esempio di nodo 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
