---
helpx_url: ""
breadcrumb-title: ''
description: Accedete ai nodi delle costanti in Substance 3D Designer per definire i valori delle costanti nei grafici delle Substance.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Costante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Costante

I nodi costanti consentono di creare un valore statico da utilizzare all&#39;interno dei grafici delle Substance.

Questi nodi sono disponibili nella sezione **Valori > Costanti** della libreria.\
Includono tutti un semplice nodo [Processore di valori](../../atomic-nodes/value-processor/value-processor.md) che genera il valore.

+++ Nodi costanti nella libreria

![constants-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="Nodo Virgola mobile costante" /></p>

## Interi

Gli interi costanti generano numeri interi e hanno un passo di 1.

[Possono essere convertiti in Virgola mobile,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) operazione consigliata quando si eseguono operazioni più complesse di aggiunte, sottrazioni e confronti semplici.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo intero](../../../../assets/fn-constant-integer.png "Icona tipo intero")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Numero intero</b>

Un numero intero ha un singolo componente. È utile come indice per effettuare selezioni quali:

* selezionando un&#39;opzione presentata all&#39;utente come menu a discesa (vedere &#39;Elenco a discesa&#39; in [questa pagina](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* selezione dell&#39;input di un nodo [Multi switch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).<b></b>

>[!IMPORTANT]
>
> <b>I numeri interi negativi</b> nelle funzioni dei parametri *non sono supportati*. Per una soluzione alternativa, vedere [questa pagina](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) nella sezione &#39;Problemi tecnici&#39;.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Integer2](../../../../assets/fn-constant-integer2.png "Icona tipo Integer2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero2</b>

Un nodo Integer2 genera un vettore intero statico a 2 componenti con componenti (X, Y).

Uno dei casi d&#39;uso più comuni di Integer2 è l&#39;impostazione delle dimensioni della griglia X e Y, come nel nodo [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Integer3](../../../../assets/fn-constant-integer3.png "Icona tipo Integer3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero3</b>

Un nodo Integer3 genera un vettore intero statico a 3 componenti con componenti (X, Y, Z).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Integer4](../../../../assets/fn-constant-integer4.png "Icona tipo Integer4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero4</b>

Un nodo Integer4 genera un vettore intero statico a 4 componenti con componenti (X, Y, Z, W).

</td>
</tr>
</table>

## Galleggianti

I valori delle Virgole mobili costanti generano numeri frazionari, ossia supportano i valori dopo il segno decimale e possono essere regolati in passaggi più piccoli di 1. (Predefinito: 0,01)

[Le Virgole mobili possono essere convertite in numeri interi](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), ma verranno arrotondate per eccesso o per difetto al numero intero più vicino, con conseguente perdita di dati e precisione.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile](../../../../assets/fn-constant-float.png "Icona tipo Virgola mobile")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Mobile</b>

Una Virgola mobile ha un singolo componente ed è molto comunemente usata per ogni singolo valore che richiede precisione.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 2](../../../../assets/fn-constant-float2.png "Icona tipo Virgola mobile 2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Un nodo Virgola mobile2 genera un vettore a 2 componenti con componenti (X, Y).

Virgola mobile2 è comunemente utilizzato per [coordinate di campionamento](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), [trasformazioni di offset](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) e manipolazione vettoriale 2D generale.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 3](../../../../assets/fn-constant-float3.png "Icona tipo Virgola mobile 3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Un nodo Virgola mobile3 genera un vettore a 3 componenti (X, Y, Z).

Virgola mobile3 viene utilizzato principalmente quando si lavora con oggetti 3D e [coordinate di scala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), ad esempio nei [nodi SDF 3D](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), e come metodo più semplice per memorizzare i colori RGB, ad esempio senza Alpha.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 4](../../../../assets/fn-constant-float4.png "Icona tipo Virgola mobile 4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Una Virgola mobile 4 genera un vettore a 4 componenti (X, Y, Z, W).

Virgola mobile 4 è il modo preferito per memorizzare e impostare le informazioni sui colori in cui i valori XYZW sono mappati su RGBA, ad esempio nel [nodo di Colore uniforme](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md).

</td>
</tr>
</table>

## Non numerico

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo booleano](../../../../assets/fn-constant-boolean.png "Icona tipo booleano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Un valore booleano è il tipo di dati più semplice disponibile, con due soli stati: <code>true</code> o <code>false</code>.

Questo tipo è abbastanza comune quando si utilizzano i parametri di attivazione/disattivazione e le condizioni [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md).<br>I booleani sono un modo semplice ed efficiente per controllare il flusso di una funzione o di un grafico, ad esempio utilizzando un [nodo switch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md).

</td>
</tr>
</table>
