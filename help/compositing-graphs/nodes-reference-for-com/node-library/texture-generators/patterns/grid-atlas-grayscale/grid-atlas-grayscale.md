---
title: Scala di grigi Atlante griglia
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Generatore > Pattern > Atlante griglia scala di grigi
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Scala di grigi Atlante griglia

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona scala di grigio Atlante griglia](grid-atlas-grayscale.resources/grid-atlas-grayscale-01.png "Scala di grigio Atlante griglia")

<b>Ingresso:</b> Generatore > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Confezione di fino a 16 immagini in scala di grigio su una griglia di dimensioni XY regolabili.<br>L&#39;immagine dell&#39;atlas di output può essere campionata da uno splatter [Shape v2](../shape-splatter-v2/shape-splatter-v2.md) o da un nodo [Shape splatter mapper greyscale](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

Vedere anche [colore Atlante griglia](../grid-atlas-color/grid-atlas-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|                             |                                |
|:----------------------------|:-------------------------------|
| <b>Input 1</b> *Scala di grigi* | #1. di input dell’immagine in scala di grigio |
| <b>Input 2</b> *Scala di grigi* | #2. di input dell’immagine in scala di grigio |
| <b>Input 3</b> *Scala di grigi* | #3. di input dell’immagine in scala di grigio |
| <b>Input 4</b> *Scala di grigi* | #4. di input dell’immagine in scala di grigio |
| <b>Input 5</b> *Scala di grigi* | #5. di input dell’immagine in scala di grigio |
| <b>Input 6</b> *Scala di grigi* | #6. di input dell’immagine in scala di grigio |
| <b>Input 7</b> *Scala di grigi* | #7. di input dell’immagine in scala di grigio |
| <b>Input 8</b> *Scala di grigi* | #8. di input dell’immagine in scala di grigio |
| <b>Input 9</b> *Scala di grigi* | #9. di input dell’immagine in scala di grigio |
| <b>Input 10</b> *Scala di grigi* | #10. di input dell’immagine in scala di grigio |
| <b>Input 11</b> *Scala di grigi* | #11. di input dell’immagine in scala di grigio |
| <b>Input 12</b> *Scala di grigi* | #12. di input dell’immagine in scala di grigio |
| <b>Input 13</b> *Scala di grigi* | #13. di input dell’immagine in scala di grigio |
| <b>Input 14</b> *Scala di grigi* | #14. di input dell’immagine in scala di grigio |
| <b>Input 15</b> *Scala di grigi* | #15. di input dell’immagine in scala di grigio |
| <b>Input 16</b> *Scala di grigi* | #16. di input dell’immagine in scala di grigio |

<a name="outputs"></a>

## Output

|               |                                  |
|:--------------|:---------------------------------|
| <b>Output</b> | Atlante griglia della scala di grigi di output. |

<a name="parameters"></a>

## Parametri

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Dimensione griglia X</b> *Numero intero* | Dimensione della griglia sull&#39;asse X.<br>Cioè il numero di immagini compresse sull&#39;asse X. |
| <b>Dimensione griglia Y</b> *Numero intero* | Dimensione della griglia sull&#39;asse Y.<br>Cioè il numero di immagini compresse sull&#39;asse Y. |
| <b>Modalità dimensioni output</b> *Numero intero* | Metodo di definizione delle dimensioni dell&#39;immagine di output in base al parametro di base &#39;Dimensioni output&#39; del nodo:<br><br>- <b>Manuale:</b> Utilizzare le dimensioni così come sono.<br>- <b>Rapporto automatico:</b> Regolare le proporzioni dell&#39;immagine in base alle dimensioni della griglia per ridurre al minimo le dimensioni dell&#39;immagine. Si verificherà una deformazione per le griglie non quadrate utilizzando 3 righe o colonne, ad esempio (3, 2), (4, 3) |

## Esempi

<img src="./grid-atlas-grayscale.resources/grid-atlas-grayscale-02.png" alt="Atlante griglia di nodo in scala di grigi nel contesto di un grafico" style="width: 50%"><br>
<i>Nodo Atlante griglia in scala di grigi nel contesto di un grafico</i>
