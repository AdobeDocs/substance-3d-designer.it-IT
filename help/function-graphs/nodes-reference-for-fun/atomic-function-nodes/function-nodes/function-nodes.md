---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Accedere ai nodi delle funzioni nei grafici delle funzioni di Substance 3D Designer per richiamare ed eseguire grafici delle funzioni personalizzati.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Funzione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Nodi funzione

I nodi di funzione trasformano il valore di input in base alla funzione matematica che rappresentano.

Sebbene i connettori di input non siano in genere tipizzati, non supportano tutti i tipi di valore.

## Elenco nodi

+++Pow
![Icona nodo di flusso](function-nodes.resources/function-nodes-01.jpg "Icona nodo di flusso")



Restituisce il primo input elevato alla potenza del secondo input: <b>X^Y</b>.

+++

+++2Pow
![Icona nodo 2Pow](function-nodes.resources/function-nodes-02.jpg "Icona nodo 2Pow")



Restituisce 2 alla potenza del valore di input: <b>2^X</b>.

+++

+++Radice quadrata
![Icona nodo radice quadrata](function-nodes.resources/function-nodes-03.jpg "Icona nodo radice quadrata")



Restituisce la radice quadrata del valore di input: <b>√X</b>.

+++

+++Esponenziale
![Icona nodo esponenziale](function-nodes.resources/function-nodes-04.jpg "Icona nodo esponenziale")



Restituisce il valore esponenziale del relativo valore di input: <b>e^X</b>

<b>e</b> è approssimativamente uguale a 2.7182818.

+++

+++Logaritmo
![Icona nodo logaritmo](function-nodes.resources/function-nodes-05.jpg "Icona nodo logaritmo")



Restituisce il logaritmo naturale del valore di input: <b>ln(X)</b>.

+++

+++Base logaritmica 2
![Icona nodo Logaritmo Base 2](function-nodes.resources/function-nodes-06.jpg "Icona nodo Logaritmo Base 2")



Restituisce il logaritmo in base 2 del relativo valore di input: <b>log2(X)</b>.

+++

+++Assoluto
![Icona nodo assoluto](function-nodes.resources/function-nodes-07.jpg "Icona nodo assoluto")



Restituisce il valore assoluto del relativo input: <b>abs(X)</b>.

+++

+++Ceil
![Icona nodo Ceil](function-nodes.resources/function-nodes-08.jpg "Icona nodo Ceil")



Arrotonda per eccesso il valore di input. Restituisce il valore intero più piccolo, non minore di X: <b>ceil(X)</b>.

+++

+++Floor
![Icona nodo floor](function-nodes.resources/function-nodes-09.jpg "Icona nodo floor")



Arrotonda per difetto il valore di input. Restituisce il valore intero più grande non maggiore di X: <b>floor(X)</b>.

+++

+++Interpolazione lineare
![Icona nodo di interpolazione lineare](function-nodes.resources/function-nodes-10.jpg "Icona nodo di interpolazione lineare")



Restituisce l&#39;interpolazione lineare tra due valori in funzione di un valore mobile: <b>(1 - X)\*A + X\*B</b>.

+++

+++Minimo
![Icona nodo minimo](function-nodes.resources/function-nodes-11.jpg "Icona nodo minimo")



Restituisce il valore più basso tra i due valori di input: <b>min(A, B)</b>.

+++

+++Massimo
![Icona nodo massimo](function-nodes.resources/function-nodes-12.jpg "Icona nodo massimo")



Restituisce il più alto dei due valori di input: <b>max(A, B)</b>.

+++

+++Coseno
![Icona nodo coseno](function-nodes.resources/function-nodes-13.jpg "Icona nodo coseno")



Restituisce il coseno del relativo valore di input in radianti: <b>cos(X)</b>.

+++

+++Seno
![Icona nodo sinusoidale](function-nodes.resources/function-nodes-14.jpg "Icona nodo sinusoidale")



Restituisce il seno del valore di input in radianti: <b>sin(X)</b>.

+++

+++Tangente
![Icona nodo tangente](function-nodes.resources/function-nodes-15.jpg "Icona nodo tangente")



Restituisce la tangente del valore di input in radianti: <b>tan(X)</b>.

+++

+++Tangente arco 2
![Icona nodo Arco tangente 2](function-nodes.resources/function-nodes-16.jpg "Icona nodo Arco tangente 2")



Restituisce l&#39;angolo tra il vettore 2D di input e l&#39;orizzontale.

È il reciproco della funzione <b>Cartesiana</b>.

Non è necessario cambiare i componenti X e Y del vettore di input come nella normale funzione <b>atan2</b>.

+++

+++Cartesiano
![Icona nodo assoluto](function-nodes.resources/function-nodes-07.jpg "Icona nodo assoluto")



Converte le coordinate polari in coordinate cartesiane.

È il reciproco della funzione <b>Arco tangente 2 </b>: <b>Lunghezza \* Float2(cos(Angolo), sin(Angolo).</b>

Le coordinate polari sono una distanza dall&#39;origine e un angolo in radianti rispetto all&#39;orizzontale.

+++

+++Casuale
![Icona nodo casuale](function-nodes.resources/function-nodes-17.jpg "Icona nodo casuale")



Restituisce un valore casuale compreso tra 0 e il valore di input <b>X</b>.

+++
