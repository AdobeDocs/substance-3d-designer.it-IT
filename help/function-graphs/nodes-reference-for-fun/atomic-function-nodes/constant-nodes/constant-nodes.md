---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Accedere ai nodi costanti nei grafici delle funzioni di Substance 3D Designer per definire valori e parametri costanti.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Costante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# Costante

I nodi costanti consentono di creare un valore statico da utilizzare all&#39;interno dei grafici delle funzioni delle Substance. A differenza delle [variabili](../../../../function-graphs/variables/variables.md), non possono essere modificate esternamente.

Inoltre, questa pagina fornisce alcune informazioni aggiuntive per ogni tipo di dati e casi d&#39;uso comuni.

## Interi

Gli interi costanti generano numeri interi e hanno un passo di 1.

[Possono essere convertiti in Virgola mobile,](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) operazione consigliata quando si eseguono operazioni più complesse di aggiunte, sottrazioni e confronti semplici.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo intero](constant-nodes.resources/constant-nodes-01.png "Icona tipo intero")

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

![Icona tipo Integer2](constant-nodes.resources/constant-nodes-02.png "Icona tipo Integer2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero2</b>

Un nodo Integer2 genera un vettore intero statico a 2 componenti con componenti (X, Y).

Integer2 non è comune, ma viene utilizzato ad esempio per impostare l&#39;Affiancamento X e Y 2D in un [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Integer3](constant-nodes.resources/constant-nodes-03.png "Icona tipo Integer3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero3</b>

Un nodo Integer3 genera un vettore intero statico a 3 componenti con componenti (X, Y, Z).

Intero 3 non è comune ed è improbabile che venga rilevato molto.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Integer4](constant-nodes.resources/constant-nodes-04.png "Icona tipo Integer4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Intero4</b>

Un nodo Integer4 genera un vettore intero statico a 4 componenti con componenti (X, Y, Z, W).

Intero 4 non è comune ed è improbabile che venga rilevato molto.<b>\
</b>

</td>
</tr>
</table>

## Galleggianti

Le Virgole mobili costanti generano numeri frazionari, non numeri interi, il che significa che avranno sempre dei valori dopo il segno decimale e possono entrare o diminuire in passaggi più piccoli di 1 (valore predefinito 0,01).

[Le Virgole mobili possono essere convertite in numeri interi](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), ma verranno arrotondate per eccesso o per difetto al numero intero più vicino, con conseguente perdita di dati e precisione.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile](constant-nodes.resources/constant-nodes-05.png "Icona tipo Virgola mobile")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Mobile</b>

Una Virgola mobile, ha un singolo componente, il (1) è omesso dal nome per brevità. La Virgola mobile è molto comune e viene utilizzata per qualsiasi valore che richiede un controllo preciso sotto forma di cursore o angolo. Potete trovarlo in quasi tutti i parametri dei nodi. È inoltre il tipo di dati preferito per un valore in scala di grigi!<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 2](constant-nodes.resources/constant-nodes-06.png "Icona tipo Virgola mobile 2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float2</b>

Un nodo Virgola mobile2 genera un vettore Virgola mobile statico a 2 componenti. I componenti sono denominati X, Y. Virgola mobile2 è molto comune ed è utilizzato per [coordinate di campionamento](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) e per [scostamenti di trasformazione](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 3](constant-nodes.resources/constant-nodes-07.png "Icona tipo Virgola mobile 3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float3</b>

Un nodo Virgola mobile3 genera un vettore Virgola mobile statico a 3 componenti. I componenti sono denominati X,Y,Z. Virgola mobile3 non è comune, viene utilizzato principalmente per rappresentare [coordinate di scala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) e come metodo più semplice per memorizzare il colore senza dati Alpha.<b>\
</b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo Virgola mobile 4](constant-nodes.resources/constant-nodes-08.png "Icona tipo Virgola mobile 4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Float4</b>

Una Virgola mobile 4 genera una Virgola mobile vettoriale statica a 4 componenti.I componenti sono denominati X,Y,Z,W. Virgola mobile4 è molto comune, in quanto rappresenta il modo preferito per memorizzare e impostare [informazioni sui colori, in cui i dati XYZW rappresentano valori RGBA.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## Altri

Esistono due tipi di dati aggiuntivi all&#39;interno dei grafici delle funzioni di Substance: booleani e stringhe. In Designer versione 6 sono state introdotte stringhe accanto al nodo [Testo](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md).

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo booleano](constant-nodes.resources/constant-nodes-09.png "Icona tipo booleano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Un valore Boolean è il tipo di dati più semplice, con due stati distinti: True o False, 1 o 0. È rappresentata dal colore bianco. Non è possibile scambiare valori Boolean e Integer senza [Casting](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) o utilizzando [nodi logici.](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) Un valore booleano è abbastanza comune ed è un modo eccellente per controllare il flusso di una funzione o di un grafico. Un utilizzo tipico potrebbe essere per un [nodo switch.](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Icona tipo stringa](constant-nodes.resources/constant-nodes-10.png "Icona tipo stringa")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Stringa</b>

Un nodo stringa genera una stringa statica, ovvero un testo. Si tratta del tipo più esotico di dati disponibili in Funzioni e generalmente non può essere utilizzato molto insieme ad altri nodi di Funzione. L&#39;obiettivo principale è quello di funzionare come output finale per il [nodo di testo.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

</td>
</tr>
</table>
