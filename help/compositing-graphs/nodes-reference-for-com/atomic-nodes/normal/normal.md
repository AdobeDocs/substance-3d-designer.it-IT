---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Utilizzare il nodo Normale per elaborare e manipolare le texture delle mappe normali per controllare i dettagli e l'illuminazione delle superfici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Normale](../../../../assets/comp_normal_1.png "Nodo atomico: Normale"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcola una mappa della normale da un&#39;immagine in scala di grigi interpretata come mappa dell&#39;altezza.

Il nodo converte una mappa in scala di grigi di input in un output di Mappa normale nello spazio tangente. Ha alcune opzioni per l&#39;utente per impostare l&#39;intensità e la codifica.

</td>
</tr>
</table>

Si tratta di un nodo molto utile che viene spesso utilizzato per convertire l&#39;input della mappa di altezza in mappa normale per materiali pronti in tempo reale. Esistono alternative in [Sobel normale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) e nelle unità Height-mondo normali.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Intensità</b> *Virgola mobile* | Modifica l’intensità della mappa dell’altezza.   Consente di impostare l’intensità di interpretazione della mappa dell’altezza di input per la conversione in valori normali. A seconda delle mappe di input, i valori superiori a 100 hanno un effetto leggermente maggiore. |
| <b>Formato normale</b> *Booleano* | Inverte le coordinate Y della mappa dell’altezza (OpenGL).   Consente di impostare la codifica del canale Verde (Y). Sostanzialmente un interruttore &quot;Flip Green/Y&quot;. |
| <b>Contenuto Canale alfa</b> *Booleano* | Riempire il canale alfa della mappa normale con la texture di input.   Riempi Alpha con input/Forza Alpha a 1: consente di impostare il Canale alfa su solido, invece di utilizzare l’input come Alpha aggiuntivo. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi* PRIMARIO | Immagine di input interpretata come mappa di altezza. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Colore* |  |

## Esempi

*Disponibile a breve.*
