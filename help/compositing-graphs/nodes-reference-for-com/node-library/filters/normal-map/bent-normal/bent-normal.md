---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: Utilizzare il nodo Normale piegatura per generare mappe normali piegate che tengano conto dell'occlusione ambientale e dell'illuminazione indiretta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura della normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# Curvatura della normal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Icona nodo normale piegato](../../../../../../assets/rt-bent-normal.png "Icona nodo normale piegato")

<b>Ingresso:</b> *Filtri/Mappa normale*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Genera una mappa normale piegata in base all&#39;input di una mappa del height. Una mappa Normale piegata è una versione speciale di [Normale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) e [Occlusione ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md), che genera una mappa normale con occlusione ambiente incorporata.\
Questo può essere utilizzato nei motori in tempo reale per fare in modo che l&#39;Occlusione ambientale sia inclusa nella mappa normale, ad esempio per riflessioni di occlusione più accurate sui metalli.

Questo nodo non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo.

</td>
</tr>
</table>

## Parametri

<b>Usa Dimensioni fisiche</b> *Booleano*\
Attivate/disattivate per utilizzare le impostazioni della Dimensioni fisiche per determinare la scala del height.

<b>Dimensioni fisiche</b> *Float3* (disponibile quando <b>Usa Dimensioni fisiche</b> è impostato su *Vero*)\
Regola la scala del height in base alla dimensioni fisiche reale della superficie.

<b>Esempi</b> *Numero intero*\
Numero di raggi utilizzati per calcolare la normale piegata.\
Un valore più alto fornisce un risultato più uniforme e preciso a costo delle prestazioni.

<b>Scala Height</b> *Mobile (disponibile quando Usa Dimensioni fisiche è impostato su False)*\
Moltiplicatore per l&#39;intensità dell&#39;input della mappa del height.

<b>Distribuzione</b> *Numero intero*\
Imposta il metodo di distribuzione. Influisce sul decadimento verso le aree in ombra.

<b>Distanza Massima</b> *Mobile*\
Consente di impostare la distanza massima percorribile dai raggi per l’occlusione.

<b>Angolo di diffusione</b> *Mobile*\
Consente di impostare l’angolo di diffusione dei raggi da riprendere. Un valore pari a 1 è un emisfero completo.

<b>Formato Normale</b> *Numero Intero*\
Inverte il canale verde dell’output.

## Immagini di esempio

![Nodo normale piegato - Esempio 1](../../../../../../assets/bent-normal-ex-1.jpg "Nodo normale piegato - Esempio 1")
