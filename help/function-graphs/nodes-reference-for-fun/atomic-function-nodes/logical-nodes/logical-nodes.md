---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Accedere ai nodi logici nei grafici delle funzioni di Substance 3D Designer per eseguire operazioni logiche booleane e confronti.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Logico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nodi logici

I nodi logici vengono utilizzati per aggiungere più condizioni al grafico:

![](logical-nodes.resources/logical-nodes-01.png)

## Nodo *And*

![](logical-nodes.resources/logical-nodes-02.png)

Il nodo And accetta due nodi booleani come input:

* Se entrambi gli input sono True, l&#39;output del nodo *And* sarà *True*
* In qualsiasi altro caso il nodo *And* restituirà *False*

## Nodo *O*

![](logical-nodes.resources/logical-nodes-03.png)

Il nodo Or accetta due nodi booleani come input:

* Se almeno uno degli input è True (1), l&#39;output del nodo *Or* sarà *True*
* Se entrambi gli input sono False, il nodo *Or* restituirà *False*

## Nodo *Not*

![](logical-nodes.resources/logical-nodes-04.png)

Il nodo Not assume un valore booleano come input: esaminerà il valore di input e restituirà il suo opposto:

* L&#39;input *True* restituisce l&#39;output *False*
* L&#39;input *False* restituisce l&#39;output *True*
