---
title: Colore Atlante griglia
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Generatore > Pattern > Colore Atlante griglia
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Colore Atlante griglia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona colore Atlante griglia](grid-atlas-color.resources/grid-atlas-color.png "Colore Atlante griglia")

<b>Ingresso:</b> Generatore > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Su una griglia di dimensioni XY regolabili sono disponibili fino a 16 immagini a colori.<br>L&#39;immagine dell&#39;atlas di output può essere campionata da uno [splatter di forma v2](../shape-splatter-v2/shape-splatter-v2.md) o da un nodo [splatter di colore](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md).

Vedere anche [scala di grigi Atlanti griglia](../grid-atlas-grayscale/grid-atlas-grayscale.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|                         |                            |
|:------------------------|:---------------------------|
| <b>Input 1</b> *Colore* | #1. di input dell’immagine a colori |
| <b>Input 2</b> *Colore* | #2. di input dell’immagine a colori |
| <b>Input 3</b> *Colore* | #3. di input dell’immagine a colori |
| <b>Input 4</b> *Colore* | #4. di input dell’immagine a colori |
| <b>Input 5</b> *Colore* | #5. di input dell’immagine a colori |
| <b>Input 6</b> *Colore* | #6. di input dell’immagine a colori |
| <b>Input 7</b> *Colore* | #7. di input dell’immagine a colori |
| <b>Input 8</b> *Colore* | #8. di input dell’immagine a colori |
| <b>Input 9</b> *Colore* | #9. di input dell’immagine a colori |
| <b>Input 10</b> *Colore* | #10. di input dell’immagine a colori |
| <b>Input 11</b> *Colore* | #11. di input dell’immagine a colori |
| <b>Input 12</b> *Colore* | #12. di input dell’immagine a colori |
| <b>Input 13</b> *Colore* | #13. di input dell’immagine a colori |
| <b>Input 14</b> *Colore* | #14. di input dell’immagine a colori |
| <b>Input 2</b> *Colore* | #15. di input dell’immagine a colori |
| <b>Input 2</b> *Colore* | #16. di input dell’immagine a colori |

<a name="outputs"></a>

## Output

|               |                              |
|:--------------|:-----------------------------|
| <b>Output</b> | Atlante griglia del colore di output. |

<a name="parameters"></a>

## Parametri

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Dimensione griglia X</b> *Numero intero* | Dimensione della griglia sull&#39;asse X.<br>Cioè il numero di immagini compresse sull&#39;asse X. |
| <b>Dimensione griglia Y</b> *Numero intero* | Dimensione della griglia sull&#39;asse Y.<br>Cioè il numero di immagini compresse sull&#39;asse Y. |
| <b>Modalità dimensioni output</b> *Numero intero* | Metodo di definizione delle dimensioni dell&#39;immagine di output in base al parametro di base &#39;Dimensioni output&#39; del nodo:<br><br>- <b>Manuale:</b> Utilizzare le dimensioni così come sono.<br>- <b>Rapporto automatico:</b> Regolare le proporzioni dell&#39;immagine in base alle dimensioni della griglia per ridurre al minimo le dimensioni dell&#39;immagine. Si verificherà una deformazione per le griglie non quadrate utilizzando 3 righe o colonne, ad esempio (3, 2), (4, 3) |

## Esempi

<img src="./grid-atlas-color.resources/grid-atlas-color-graph.png" alt="Nodo di colore di Atlante griglia nel contesto di un grafico" style="width: 50%"><br>
<i>Nodo di colore Atlante griglia nel contesto di un grafico</i>