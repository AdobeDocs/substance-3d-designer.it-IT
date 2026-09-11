---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/sampler-nodes.html"
breadcrumb-title: ''
description: Accedete ai nodi campionatori nei grafici delle funzioni di Substance 3D Designer per campionare le texture ed estrarre i valori cromatici.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Samplers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Campionatori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Nodi di Sampler

![Nodi Sampler](../../../../assets/image2016-1-12-14-45-43.png "Nodi Sampler")

Questi nodi campionano un valore in un&#39;immagine di input alle coordinate 2D fornite:

<b>Grigio campione</b> esegue il campionamento di un valore di luminanza in corrispondenza della <b>Posizione</b> di input in un&#39;immagine in scala di grigio e lo genera come valore <b>Mobile</b>.

<b>Colore campione</b> campiona un valore RGBA in corrispondenza della <b>posizione </b>di input in un&#39;immagine a colori e lo genera come valore <b>Float4</b> in cui i componenti R,G,B e A sono mappati rispettivamente ai componenti X, Y, Z e W.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Le coordinate iniziano dall’angolo superiore sinistro di un input e variano da 0 a 1 in orizzontale e verticale.

Le posizioni al di fuori di questo intervallo vengono gestite in base alla <b>modalità di indirizzamento</b> selezionata (vedere di seguito).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Coordinate pixel](../../../../assets/samplercoords.png "Coordinate pixel")

</td>
</tr>
</table>

>[!NOTE]
>
> L&#39;input <b>Position</b> deve essere un valore Float2 in cui le coordinate X e Y dell&#39;immagine sono mappate rispettivamente ai componenti X e Y del valore

## Parametri

+++Immagine di input
Consente di selezionare l&#39;input del nodo da utilizzare per il campionamento.

L&#39;elenco si adatta dinamicamente agli input attualmente connessi. Questo significa che le voci vengono aggiunte durante la connessione degli input del nodo.

La numerazione degli input inizia da 0, in modo che un&#39;immagine connessa al primo input del nodo venga elencata come *Immagine di input 0*.

+++

+++Modalità filtro
Consente di definire come gestire l’interpolazione quando i pixel dell’immagine campionata non vengono mappati esattamente all’immagine di output a causa delle differenze di risoluzione.

<b>Più Vicino</b>\
Il pixel verrà mappato alla destinazione *così com&#39;è* in corrispondenza della coordinata corrispondente. Se la destinazione è di risoluzione inferiore, il pixel può essere completamente ignorato. Se la destinazione ha una risoluzione maggiore, verrà mappata a tutti i pixel che la coprono. L&#39;output è *più nitido* e avrà un aspetto leggermente *con alias*.

<b>Filtro bilineare</b>\
All&#39;immagine sorgente viene applicato un processo di filtro in modo che i pixel vengano mappati alla risoluzione di destinazione in modo da *attenuare* le transizioni tra i pixel. L&#39;output è *più uniforme* e avrà un aspetto leggermente *sfocato*.

+++

+++Modalità Indirizzamento
Controlla la gestione dei valori di posizione esterni all&#39;intervallo [0;1].

<b>Ripeti</b>\
Esegue il ciclo nell&#39;intervallo [0;1] man mano che il valore aumenta.\
Ad esempio: 3,4 è 0,4, -1,7 è 0,3.

<b>Blocca al bordo</b>\
Blocca i valori all&#39;esterno dell&#39;intervallo [0;1] al limite più vicino.\
Esempio: .3.4 è 1, -1.7 è 0.

+++
