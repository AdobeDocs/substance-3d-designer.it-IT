---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: Utilizza il nodo Mappatura forme per mappare le forme sulle texture con trasformazioni e posizionamento personalizzabili.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura forme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Mappatura forme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Mappatura forme - Icona](../../../../../../assets/shape_mapper.png "Mappatura forme - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Progetta un’immagine di input lungo un cerchio o un poligono.

La proiezione deforma l&#39;immagine in modo da seguire il contorno della forma e adattarla esattamente a un determinato numero di volte senza spazi vuoti.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Input

</td>
<td style="border: 0;" valign="top">

### Output

</td>
<td style="border: 0;" valign="top">

### Parametri

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Input

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi* | Il motivo da posizionare lungo la forma. |

## Output

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | Risultato della proiezione del motivo lungo la forma, come bitmap in scala di grigio. |

## Parametri

|  |  |
| --- | --- |
| <b>Forma</b> Intero | Imposta il tipo di forma lungo cui devono essere posizionati i motivi:<ul data-preserve-html="true"> <li data-preserve-html="true">Cerchio</li> <li data-preserve-html="true">Poligono</li> </ul> |
| <b>Quantità motivo</b> Numero intero | Quantità di motivi posizionati lungo la forma selezionata. |
| <b>Collega segmenti con quantità di pattern</b> Booleano *Disponibile quando &#39;Shape&#39; è impostato su &#39;Polygon&#39;* | Usate <b>Quantità pattern</b> come numero di <b>Segmenti</b>.   In questo modo si evita che i pattern si avvolgano attorno agli angoli, assicurando un aspetto retto e coerente. |
| <b>Segmenti</b> Numero intero *Disponibile quando &#39;Shape&#39; è impostato su &#39;Polygon&#39; e &#39;Link segements with pattern amount&#39; è impostato su &#39;False&#39;* | La quantità di segmenti per il poligono lungo cui vengono posizionati i pattern.   I segmenti sono di *dimensioni uniformi* e tutti i vertici sono *equidistanti dal centro*, in modo che aumentando la quantità di segmenti il poligono converga verso un cerchio. |
| <b>Raggio</b> Mobile | Moltiplicatore per il raggio della forma, in cui 1,0 corrisponde alla metà della lunghezza del lato più corto dell&#39;immagine. |
| <b>Larghezza</b> Mobile | Moltiplicatore per la larghezza dei motivi lungo la forma, dove 1,0 corrisponde alla metà della lunghezza del lato più corto dell&#39;immagine. |
| <b>Rotazione</b> Mobile | Quantità di rotazione applicata alla forma, espressa in numero di giri in senso orario rispetto all&#39;orizzontale a destra. |
| <b>Capovolgere uno su due</b> elementi booleani | Capovolgi verticalmente una forma ogni due forme. |
| <b>Modalità filtro</b> Numero intero | Metodo di filtraggio applicato ai motivi posizionati lungo la forma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Più vicino:</i> applica il valore del pixel più vicino così com&#39;è, creando un aspetto più nitido ma con aliasing.</li> <li data-preserve-html="true"><i>Bilineare:</i> applica un filtro bilineare per interpolare il pixel proiettato con i pixel vicini, per un aspetto più uniforme ma più sfocato.</li> </ul> |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene la forma generata squadrata ed espande la generazione dell&#39;immagine fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
