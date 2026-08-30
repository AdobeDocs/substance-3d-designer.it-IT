---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Scopri come utilizzare le espressioni if visibili in Substance 3D Designer per controllare la visibilità dei parametri in base alle condizioni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visibile se le espressioni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# Visibile se le espressioni

L&#39;espressione &#39;Visible if&#39; consente di <b>controllare la visibilità</b> di input, output e parametri nei grafici.

Quando [si espongono i parametri](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), è possibile nascondere o visualizzare i parametri o i connettori dei nodi in base allo stato degli altri parametri. Ad esempio, un cursore che viene visualizzato solo quando un pulsante del parametro booleano è impostato su `true`, perché altrimenti non avrebbe alcun effetto e questo potrebbe confondere gli utenti.

A tale scopo, è possibile immettere un&#39;*espressione logica* nella proprietà <b>Visible if</b> di:

* [parametro di input](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) di un grafico;
* nodo [Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) di un grafico;
* nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) di un grafico.

![Attivazione/disattivazione della visibilità dei parametri di input](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-example.gif "Attivazione/disattivazione della visibilità dei parametri di input"){width="512px"}

Se l&#39;espressione logica restituisce `true`, il parametro, l&#39;input o l&#39;output viene visualizzato in tutti i [nodi di istanza](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) che rappresentano il grafico corrente. In caso contrario, è *nascosto*.

Le condizioni complesse sono possibili, a condizione che l&#39;espressione logica che indica tali condizioni sia valida.

>[!NOTE]
>
> Caveats
> 
> * Questa funzionalità *solo* influisce sulla visualizzazione di un parametro o di un connettore nell&#39;interfaccia utente e non ha *alcun effetto* sui calcoli e sul risultato di un grafico.
> * Durante l&#39;esposizione o l&#39;applicazione di una funzione a qualsiasi parametro utilizzato nelle istruzioni &#39;Visible if&#39;, tali istruzioni verranno *ignorate* e impostate per impostazione predefinita su &#39;true&#39;.

>[!IMPORTANT]
>
> Sebbene questa funzionalità funzioni all&#39;interno dell&#39;ecosistema Substance 3D, alcune integrazioni potrebbero non supportarla. Se non supportata, la condizione di visibilità predefinita è `true`.

## Scrittura delle espressioni &#39;Visible if&#39; in corso

### ACCESSO AI PARAMETRI DI INPUT

Qualsiasi valore Visible If Expression deve utilizzare almeno un input, che può essere eseguito tramite la sintassi seguente:

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> L&#39;**identificatore** deve essere il nome *esatto* della proprietà **Identificatore** di un parametro di input esistente e deve essere digitato *con distinzione tra maiuscole e minuscole*. L&#39;utente *non può* fare riferimento a un parametro tramite la relativa etichetta.\
>  Se non esiste un parametro a cui si fa riferimento o l&#39;espressione logica non è valida, verrà visualizzato un *avviso* nella proprietà **Visible if**.

### OPERATORI DISPONIBILI

I campi &quot;Visible if&quot; accettano i seguenti parametri:

* Input Boolean, Float e Integer.
* Valori `true` e `false` (con distinzione tra maiuscole e minuscole, senza maiuscole)
* `.x`: accesso al sottoparametro
* `&&`<b> </b>: e
* `||`<b> </b>: o
* `!`<b> </b>: non
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=`: confronto
* `()`: parentesi

### DEVE SEMPRE VALUTARE BOOLEANI

Un&#39;espressione If visibile viene utilizzata come condizione per un&#39;istruzione &quot;IF&quot;, ovvero deve sempre restituire `true` o `false`.

* I valori booleani possono essere valutati direttamente come condizione. Un pulsante semplice con un valore booleano non richiede più di questo. Vedere gli esempi seguenti, primo caso;
* I parametri non booleani richiedono in genere un&#39;operazione *di confronto*. Vedere sopra per gli operatori di confronto, di seguito per gli esempi;
* Alcuni valori non booleani possono essere *veritieri* o *falsi*, ovvero `true` di `false`, ad esempio un valore intero `0` restituisce false.

## Esempi

| Condizione (&quot;If&quot;) | Formula | Nota |
| --- | --- | --- |
| True | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_input è un valore booleano |
| False | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_input è un valore booleano |
| Minore di | ` input["my_input"] < 3   input.my_input < 3 ` | my\_input è un valore intero |
| Uguale | ` input["param1"] == 2   input.param1 == 2 ` | param1 è un valore float o integer |
| Minore di | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_input è un valore float o integer con uno o più componenti, ad esempio float2(x, y), integer3(x, y, z) |
| Oppure | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1 e param2 sono valori booleani |
| E | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1 e param2 sono valori float o integer |
