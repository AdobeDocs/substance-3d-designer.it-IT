---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Accedere Ottieni nodi nei grafici delle funzioni di Substance 3D Designer per recuperare valori e dati delle variabili.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variabili
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# Variabili

Le variabili consentono di <b>archiviare valori</b> per recuperarli in seguito (<b>Get</b>) e/o modificarli (<b>Set</b>).

![Substance grafico funzioni - Ottieni grafico a virgola mobile](get-nodes.resources/assign-getfloat.gif "Substance grafico funzioni - Ottieni grafico a virgola mobile"){zoomable="yes"}

In pratica, un nodo Get acquisisce una variabile dinamica e la restituisce dall&#39;output di Get Nodes per utilizzarla in una funzione. Questi nodi Get formano il collegamento tra i parametri di input definiti in [parametri del grafico](../../../../compositing-graphs/graph-parameters/graph-parameters.md) e [funzioni dei parametri](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

Ogni volta che si utilizza un nodo Get, è necessario selezionare un valore disponibile dal menu a discesa. I nodi Get <b>acquisiranno un valore del tipo corrispondente</b>. Ciò significa che vedrai solo opzioni valide nel menu di un nodo Get, non potrai mai selezionare un&#39;opzione non valida. Se una variabile non è disponibile, significa che il tipo non corrisponde

Alcune variabili di sistema <b></b>: variabili speciali predefinite che non è possibile dichiarare. Queste variabili sono molto importanti e per i nodi sottostanti è elencato quali variabili di sistema sono disponibili.

Quando un parametro è [esposto](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), consiste nell&#39;applicare una funzione di parametro su di esso che include solo un nodo Get del tipo corretto.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Scarica

</td>
<td style="border: 0;" valign="top">

### Set

</td>
<td style="border: 0;" valign="top">

### È definita

</td>
</tr>
</table>

## Scarica

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Ottieni float2 - Icona](get-nodes.resources/fn_variables_getfloat2.png "Ottieni float2 - Icona"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Questi nodi consentono di recuperare il valore di una variabile esistente *nell&#39;ambito corrente*.

Il nome della variabile da recuperare è impostato nel Dock proprietà.

</td>
</tr>
</table>

Nodi &#39;Get&#39; alcune limitazioni di cui è necessario tenere conto:

* <b>Sono stati digitati</b>, quindi è necessario assicurarsi che la variabile contenga un valore dello stesso tipo del nodo. Mancata corrispondenza dei tipi segnalata in Console.
* <b>Non verificano l&#39;esistenza della variabile</b> nell&#39;ambito corrente. Le variabili non trovate vengono segnalate in Console.
* Nelle funzioni complesse che utilizzano nodi di flusso di controllo come Sequence, prestare attenzione all&#39;<b>ordine in cui si impostano e si ottengono le variabili</b>. Quando Designer rileva un caso di &quot;Get before Set&quot; (Scarica prima di impostare), questo viene segnalato in Console.

>[!NOTE]
>
> Variabili incorporate
> 
> Diversi nodi &quot;Get&quot; offriranno variabili incorporate per accedere ai valori esistenti in base al contesto corrente, ad esempio: la posizione corrente dei pixel in un processore Pixel, la modalità di suddivisione in porzioni corrente di un nodo...
> 
> Tutte le variabili incorporate sono elencate in [questa pagina dedicata](../../../../function-graphs/variables/system-variables/system-variables.md).

### Ottieni nodi

+++Galleggianti
![Ottieni float - Icona](get-nodes.resources/fn_variables_getfloat.png "Ottieni float - Icona"){width="200px"}



Ottieni virgola mobile

![Ottieni float2 - Icona](get-nodes.resources/fn_variables_getfloat2.png "Ottieni float2 - Icona"){width="200px"}



Ottieni Float2

![Ottieni float3 - Icona](get-nodes.resources/fn_variables_getfloat3.png "Ottieni float3 - Icona"){width="200px"}



Ottieni Float3

![Ottieni float4 - Icona](get-nodes.resources/fn_variables_getfloat4.png "Ottieni float4 - Icona"){width="200px"}



Ottieni Float4

+++

+++Interi
![Ottieni numero intero - Icona](get-nodes.resources/fn_variables_getint.png "Ottieni numero intero - Icona"){width="200px"}



Ottieni numero intero

![Ottieni numero intero2 - Icona](get-nodes.resources/fn_variables_getint2.png "Ottieni numero intero2 - Icona"){width="200px"}



Ottieni Integer2

![Ottieni numero intero3 - Icona](get-nodes.resources/fn_variables_getint3.png "Ottieni numero intero3 - Icona"){width="200px"}



Ottieni Integer3

![Ottieni numero intero4 - Icona](get-nodes.resources/fn_variables_getint4.png "Ottieni numero intero4 - Icona"){width="200px"}



Ottieni Integer4

+++

+++Altri
![Ottieni booleano - Icona](get-nodes.resources/fn_variables_getboolean.png "Ottieni booleano - Icona"){width="200px"}



Ottieni booleano

![Ottieni stringa - Icona](get-nodes.resources/fn_variables_getstring.png "Ottieni stringa - Icona"){width="200px"}



Ottieni stringa

+++

## Set

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Imposta: icona nodo](get-nodes.resources/fn_variables_set.png "Imposta: icona nodo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Testo

</td>
</tr>
</table>

## È definita

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![È definito: icona nodo](get-nodes.resources/fn_variables_isdefined.png "È definito: icona nodo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Testo

</td>
</tr>
</table>
