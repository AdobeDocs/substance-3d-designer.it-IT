---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Informazioni sui nodi a funzione atomica, le unità di nodi più piccole nei grafici a funzione Substance per la creazione di funzioni personalizzate.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nodi di funzione atomica
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 16%

---


# Nodi di funzione atomica

Analogamente a [nodi atomici nei grafici a Substance](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), i nodi atomici nei grafici a funzione Substance sono le unità di nodo più piccole in quel tipo di grafico.

Possono essere ordinati in diverse categorie in base al loro scopo:

| Categoria | Nodo | Tipo/i di input | Tipo di output | Descrizione |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Costante](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | A virgola mobile | - | A virgola mobile | Definisce un valore mobile costante, ad esempio 0,1 |
|                                                                                                                                        | Float2 | - | Float2 | Definisce un vettore costante di 2 valori mobili, ad esempio (0,1, 0,2) |
|                                                                                                                                        | Float3 | - | Float3 | Definisce un vettore costante di 3 valori mobili, ad esempio (0,1, 0,2, 0,3) |
|                                                                                                                                        | Float4 | - | Float4 | Definisce un vettore costante di 4 valori mobili, ad esempio (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Intero | - | Intero | Definisce un valore intero costante, ad esempio 1 |
|                                                                                                                                        | Integer2 | - | Integer2 | Definisce un vettore costante di 2 valori interi, ad esempio (1, 2) |
|                                                                                                                                        | Integer3 | - | Integer3 | Definisce un vettore costante di 3 valori interi, ad esempio (1, 2, 3) |
|                                                                                                                                        | Integer4 | - | Integer4 | Definisce un vettore costante di 4 valori interi, ad esempio (1, 2, 3 ,4) |
|                                                                                                                                        | Booleano | - | Booleano | Definisce un valore booleano costante, ad esempio True o False. |
|                                                                                                                                        | Stringa | - | Stringa | Definisce un valore String costante, ad esempio &quot;Substance&quot;. |
| [Vettoriale](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vettore Float2 | VIRGOLA MOBILE1 | VIRGOLA MOBILE 2 | Crea 2 valori mobili in un vettore con 2 coordinate |
|                                                                                                                                        | Vettore Float3 | Virgola mobile1/Virgola mobile2 | VIRGOLA MOBILE 3 | Crea 2 valori mobili in un vettore con 3 coordinate |
|                                                                                                                                        | Vettore Float4 | Virgola mobile 1/2/3 | VIRGOLA MOBILE 4 | Crea 2 valori mobili in un vettore con 4 coordinate |
|                                                                                                                                        | Swizzle Float1 | Vettore Float | VIRGOLA MOBILE1 | Estrae una coordinata mobile da un vettore |
|                                                                                                                                        | Swizzle Float2 | Vettore Float | Float2 | Estrae 2 coordinate mobili da un vettore |
|                                                                                                                                        | Swizzle Float3 | Vettore Float | Float3 | Estrae 3 coordinate mobili da un vettore |
|                                                                                                                                        | Swizzle Float4 | Vettore Float | Float4 | Estrae 4 coordinate mobili da un vettore |
|                                                                                                                                        | Vettore Integer2 | Integer2 | Vettore Integer2 | Crea 2 valori interi in un vettore con 2 coordinate |
|                                                                                                                                        | Vettore Integer3 | Integer3 | Integer3 | Crea 2 valori interi in un vettore con 3 coordinate |
|                                                                                                                                        | Vettore Integer4 | Integer4 | Integer4 | Crea 2 valori interi in un vettore con 4 coordinate |
|                                                                                                                                        | Swizzle Integer1 | Intero vettoriale | Intero1 | Estrae una coordinata intera da un vettore |
|                                                                                                                                        | Swizzle Integer2 | Intero vettoriale | Integer2 | Estrae 2 coordinate intere da un vettore |
|                                                                                                                                        | Swizzle Integer3 | Intero vettoriale | Integer3 | Estrae 3 coordinate intere da un vettore |
|                                                                                                                                        | Swizzle Integer4 | Intero vettoriale | Integer4 | Estrae 4 coordinate intere da un vettore |
| [Variabili](../../../function-graphs/variables/variables.md) | Set | qualsiasi | tipo di input | Imposta una variabile |
|                                                                                                                                        | Ottieni numero intero1 | - | Intero1 | Ottieni una funzione o un grafico Input con valore intero |
|                                                                                                                                        | Ottieni Integer2 | - | Integer2 | Ottieni input valore Integer2 per funzione o grafico |
|                                                                                                                                        | Ottieni Integer3 | - | Integer3 | Ottieni input valore Integer3 di una funzione o di un grafico |
|                                                                                                                                        | Ottieni Integer4 | - | Integer4 | Ottieni input valore Integer4 di una funzione o di un grafico |
|                                                                                                                                        | Ottieni Virgola mobile 1 | - | VIRGOLA MOBILE1 | Ottieni input valore mobile per funzione o grafico |
|                                                                                                                                        | Ottieni Float2 | - | Float2 | Ottieni input valore Virgola mobile 2 funzione o grafico |
|                                                                                                                                        | Ottieni Float3 | - | Float3 | Ottieni input valore Virgola mobile 3 funzione o grafico |
|                                                                                                                                        | Ottieni Float4 | - | Float4 | Ottieni input valore Virgola mobile 4 funzione o grafico |
|                                                                                                                                        | Ottieni booleano | - | Booleano | Ottenere un input di valore booleano di funzione o grafico |
| Campionatori | Grigio campione | Vettore Float2 | Float4 | Restituisce il valore in scala di grigi di un&#39;immagine di input alle coordinate UV specificate (float2) |
|                                                                                                                                        | Colore campione | Vettore Float2 | Float4 | Restituisce il valore del colore di un&#39;immagine di input alle coordinate UV specificate (float2) |
| Cast | Virgola | Intero1 | VIRGOLA MOBILE1 | Converte un numero intero in virgola mobile |
|                                                                                                                                        | A Float2 | Integer2 | Float2 | Converte un valore Integer2 in una Virgola mobile 2 |
|                                                                                                                                        | A Float3 | Integer3 | Float3 | Converte un valore Integer3 in una Virgola mobile 3 |
|                                                                                                                                        | A Float4 | Integer4 | Float4 | Converte un numero intero4 in una Virgola mobile 4 |
|                                                                                                                                        | A intero | VIRGOLA MOBILE1 | Intero1 | Converte una Virgola mobile in un numero intero |
|                                                                                                                                        | A Integer2 | Float2 | Integer2 | Converte una Virgola mobile 2 in un numero intero2 |
|                                                                                                                                        | A Integer3 | Float3 | Integer3 | Converte una Virgola mobile 3 in un numero intero3 |
|                                                                                                                                        | A Integer4 | Float4 | Integer4 | Converte una Virgola mobile 4 in un numero intero4 |
| [Operatore](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Aggiungi | Vettore Float/Numero intero | Tipo di a e b | Aggiunge 2 valori dello stesso tipo: a + b |
|                                                                                                                                        | Sottrazione | Vettore Float/Numero intero | Tipo di a e b | Sottrae 2 valori dello stesso tipo: a - b |
|                                                                                                                                        | Moltiplicazione | Vettore Float/Numero intero | Tipo di a e b | Moltiplica 2 valori dello stesso tipo: a \* b |
|                                                                                                                                        | Moltiplicazione scalare | Vettore Float | Tipo di | Moltiplica un valore per un valore mobile: un \* scalare |
|                                                                                                                                        | Divisione | Virgola mobile1/Integer1 | Tipo di a e b | Divide 2 valori dello stesso tipo: a / b |
|                                                                                                                                        | Negazione | Virgola mobile1/Integer1 | Tipo di | Restituisce il valore di negazione: -a |
|                                                                                                                                        | Modulo | Virgola mobile1/Integer1 | Tipo di | Restituisce il valore modulo: mod(a, divisore) |
|                                                                                                                                        | Prodotto scalare | Vettore Float | Tipo di a e b | Restituisce il prodotto dot di 2 valori dello stesso tipo: dot(a, b) |
| [Logico](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | E | Booleano | Booleano | Restituisce vero se le due voci booleane sono vere. Restituisce false se una delle voci è false. |
|                                                                                                                                        | Oppure | Booleano | Booleano | Restituisce vero se 1 delle voci booleane è vero. Restituisce falso se entrambi sono falsi. |
|                                                                                                                                        | Non | Booleano | Booleano | Restituisce il valore booleano di negazione della voce: !a |
| [Confronto](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Uguale | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a = b |
|                                                                                                                                        | Non uguale | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a != b |
|                                                                                                                                        | Maggiore | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a > b |
|                                                                                                                                        | Maggiore o uguale | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a >= b |
|                                                                                                                                        | Minore | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a &lt; b |
|                                                                                                                                        | Minore o uguale | Virgola mobile1/Integer1 | Booleano | Restituisce vero se a &lt;= b |
| Funzione | Assoluto | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore assoluto di a: abs(a) |
|                                                                                                                                        | Floor | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore più alto inferiore o uguale a: floor(a) |
|                                                                                                                                        | Ceil | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore più piccolo superiore o uguale a: ceil(a) |
|                                                                                                                                        | Coseno | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore coseno di a: cos(a) |
|                                                                                                                                        | Seno | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore sinusoidale di a: sin(a) |
|                                                                                                                                        | Tangente | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore tangente di a: tan(a) |
|                                                                                                                                        | Tangente arco 2 | Vettore Float2 | VIRGOLA MOBILE1 | Restituisce il valore arc tan 2 di una voce vettoriale2: arctan2(xa, ya) |
|                                                                                                                                        | Cartesiano | VIRGOLA MOBILE1 | Float2 | Converte 2 coordinate polari in coordinate cartesiane: carth(rho, theta) |
|                                                                                                                                        | Radice quadrata | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore della radice quadrata di un |
|                                                                                                                                        | Logaritmico | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore logaritmico di un valore: log(a) |
|                                                                                                                                        | Esponenziale | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce il valore esponenziale di a: exp(a) |
|                                                                                                                                        | Poa 2 | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce la potenza di 2 valore di un |
|                                                                                                                                        | Interpolazione lineare | Virgola mobile1/Integer1 | VIRGOLA MOBILE1 | Restituisce l’interpolazione lineare tra 2 valori, a seconda di un valore mobile : (1-x)a + x \* b |
|                                                                                                                                        | Minimo | Virgola mobile1/Integer1 | Tipo di a e b | Restituisce il valore minimo compreso tra a e b |
|                                                                                                                                        | Massimo | Virgola mobile1/Integer1 | Tipo di a e b | Restituisce il valore massimo compreso tra a e b |
| Casuale |                       | VIRGOLA MOBILE1 | VIRGOLA MOBILE1 | Genera un valore mobile compreso tra 0 e a |
| [Controllo](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Sequenza | qualsiasi | Tipo di input | Consente di scegliere quale valore calcolare per primo tra 2 valori. |
|                                                                                                                                        | If...Else | Booleano/a e b | Tipo di a e b | Restituisce vero se la condizione in Se è vera. Restituisce falso se è falso. |
