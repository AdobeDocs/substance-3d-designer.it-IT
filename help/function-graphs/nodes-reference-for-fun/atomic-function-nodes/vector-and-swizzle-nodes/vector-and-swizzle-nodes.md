---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Usa i nodi vettoriali e di scorrimento nei grafici delle funzioni di Substance 3D Designer per manipolare i dati e i componenti vettoriali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Vettore
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# Nodi vettore e Swizzle

I nodi vettoriali e di swizzle consentono rispettivamente di costruire e decostruire nodi vettoriali da e in componenti separati.Sono simili a [Unione RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md) e [Divisione RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), ma poi per i grafici di funzione. Si tratta inoltre di un metodo principale per la conversione tra tipi di dati vettoriali, poiché [il cast](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)non è un&#39;opzione in molti casi.

## Nodi vettoriali

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

I nodi vettoriali consentono di combinare elementi vettoriali con un numero inferiore di componenti, in vettori con più componenti. Esistono alcune regole o limitazioni specifiche per i nodi vettoriali:

* I nodi vettoriali hanno **solo due input**, anche se il vettore risultante ha più di 2 componenti.
* Gli input vettoriali sono **non limitati a un tipo**: possono accettare qualsiasi componente minore come input.
* L&#39;ordine dell&#39;output dei risultati è determinato dall&#39;**ordine degli input**.

Ciò significa che è preferibile utilizzare i seguenti metodi:

* Costruisci un vettore 4 in due modi: o collega due vettori a 2 componenti o collega un vettore a 1 componente e un vettore a 3 componenti.
* Se desiderate costruire un vettore componente 3 o 4 da singoli numeri interi o virgola mobile, dovete prima eseguire almeno una combinazione di vettore 2 prima di poterli combinare in un vettore componente 3.

Pensate bene all&#39;ordine delle connessioni. L’ordine di connessione degli ingressi è illustrato di seguito.

![](../../../../assets/vector-int1.png){width="200px"}

Esempio a sinistra Collega prima un valore Integer(1) e quindi un valore Integer 3. Il risultato è il seguente

| Output | X | Y | Z | L |
| --- | --- | --- | --- | --- |
| Input 1 | 0 |  |  |  |
| Input 2 |  | 1 | 2 | 4 |

![](../../../../assets/vector-int2.png){width="200px"}

Esempio a sinistra: scambia gli input dal primo esempio, prima Intero 3, quindi Intero(1).

| Output | X | Y | Z | L |
| --- | --- | --- | --- | --- |
| Input 1 | 1 | 2 | 4 |  |
| Input 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **Intero vettoriale2** | **Intero vettoriale3** | **Numero intero vettoriale4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-vectofloat4.png"/></div> |
| **Mobile vettoriale2** | **Mobile vettoriale3** | **Mobile vettoriale4** |

</td>
</tr>
</table>

## Nodi di Swizzle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Swizzle Nodes decostruisce o separa i componenti dai vettoriali multi-componente, consentendo di utilizzare i componenti X, Y, Z e W singolarmente e di scambiarli. Si applicano le seguenti regole e limitazioni:

* I nodi swizzle hanno **un solo output**.
* I nodi swizzle **accettano qualsiasi input** del tipo corretto (Int o Virgola mobile).

### Dividi componenti

Il caso d&#39;uso più comune di Swizzle è quello di usarlo per dividere i componenti, come la frenatura di un Integer4 in 4 singoli Integer. A causa delle limitazioni, saranno necessari quattro nodi di Swizzle integer separati.

È inoltre possibile eseguire qualsiasi altro tipo di divisione per un valore Integer4, ad esempio due valori Integer2 o un valore Integer e un valore Integer3, tenendo sempre presente che ogni risultato richiede un proprio nodo.

### Scambia/Scambia componenti

Come suggerisce il nome, Swizzle può essere utilizzato per modificare l&#39;ordine dei valori o anche sovrascrivere i valori. È possibile modificare l&#39;ordine da X,Y,Z,W a W,Y,X,Z e modificare i valori da X,Y,Z,W a X,X,X,W, ad esempio.

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../assets/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **Swizzle integer** | **Ornato** **Intero2** | **Ornato** **Intero3** | **Ornato** **Intero4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="../../../../assets/fn-vector-swizzlefloat4.png"/></div> |
| **Ornato** **Virgola mobile** | **Swizzle** **Virgola mobile 2** | **Ornato** **Virgola mobile 3** | **Ornato** **Virgola mobile 4** |

</td>
</tr>
</table>
