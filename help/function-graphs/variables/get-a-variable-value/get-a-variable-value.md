---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Scopri come recuperare i valori delle variabili nei grafici delle funzioni di Substance 3D Designer utilizzando il nodo Ottieni variabile.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ottieni un valore di variabile
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Ottieni un valore di variabile

Per utilizzare una variabile in una funzione, è necessario &quot;chiamarla&quot;, ovvero importare il valore della variabile nella funzione.

A tale scopo, è necessario utilizzare un nodo *Get*:

![](../../../assets/image2015-12-21-7-29-51.png)

Esistono diversi tipi di nodi Get: scegliere quello corretto in base al tipo di valore che si desidera importare:

![](../../../assets/image2015-12-21-7-31-4.png)

## Assegnare una variabile a un nodo Get

Per impostazione predefinita, un nodo get visualizzerà un segno di avviso: significa che non è ancora collegato ad alcuna variabile.

Per collegare una variabile, passare ai parametri e scegliere una variabile nell&#39;elenco &quot;Variabili/Get \*\*\*&quot; (\*\*\*verrà sostituito dal tipo di valore che può essere chiamato dal nodo Get).

Il nome della variabile verrà visualizzato nel nodo:

![](../../../assets/assign-getfloat.gif)

Si noti che nell&#39;elenco verranno visualizzate solo le variabili appartenenti allo stesso tipo del nodo Get.

>[!WARNING]
>
> Le variabili create con un nodo *Set* non verranno visualizzate in un elenco di nodi *Get*.
> 
> È comunque possibile ottenere la variabile scrivendo manualmente il nome nell&#39;elenco.
> 
> È possibile chiamare una variabile creata con un nodo Set solo se:
> 
> * I nodi Get e Set si trovano nei grafici delle funzioni che controllano i parametri di uno stesso nodo
> * Il parametro controllato dal grafico del nodo *Get* è lo stesso o si trova sotto il parametro del grafico del nodo *Set* nello stack dei parametri.
