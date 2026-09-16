---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ""
description: Utilizzate il nodo Sfumatura (Dinamica) per creare sfumature dinamiche che possono essere controllate dai parametri e dai valori di input.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfumatura (dinamica)
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 8%
---

# Sfumatura (dinamica)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Sfumatura dinamica](gradient-dynamic.resources/comp_dyngradient_1.png "Nodo atomico: Sfumatura dinamica")

</td>
<td style="border: 0;" valign="top">

Modifica i valori in scala di grigi di un’immagine utilizzando una sfumatura fornita da una riga o colonna di pixel in un’altra immagine.

Funziona come una leggera alternativa al nodo sfumatura, ma a differenza del nodo sfumatura, i tasti colore sfumatura non sono definiti internamente, ma provengono da un input esterno.

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="gradient-dynamic.resources/gradient-dynamic-tooltip.gif" alt="descrizione-dinamica-sfumatura" /></div>

Ciò consente principalmente di evitare il problema in cui i parametri non possono essere esposti, in quanto i parametri per il colore vengono spostati all&#39;esterno del nodo. Questo è ciò che lo rende &quot;dinamico&quot;.

Anche se Sfumatura (Dinamica) non è un nodo difficile da usare da solo, i suoi casi d&#39;uso sono un po&#39; più avanzati: la maggior parte degli usi standard possono essere coperti dal normale nodo Sfumatura.

Questo nodo viene riprodotto quando il sistema chiave dell’editor sfumatura ti limita e desideri che i colori e le posizioni della sfumatura siano guidati da altri input, parametri e parti del grafico.

In alternativa, il cursore Posizione input sfumatura può essere utilizzato per alternare più sfumature memorizzate all’interno di un singolo input sfumatura.



## Parametri

|  |  |
| --- | --- |
| <b>Indirizzamento sfumatura</b> *Booleano* | Consente di impostare se la sfumatura deve essere ripetuta (affiancata) o bloccata.   Questo parametro determina come vengono gestiti i pixel HDR fuori dall’intervallo [0, 1] dell’input in scala di grigio: bloccati o piegati fino a [0, 1]. |
| <b>Orientamento sfumatura</b> *Numero intero* | Imposta l’asse lungo il quale deve essere campionato l’input della sfumatura:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Orizzontale:</i> campionare una riga di pixel sull&#39;asse X.</li> <li data-preserve-html="true"><i>Verticale:</i> campionare una colonna di pixel sull&#39;asse Y.</li> </ul> |
| <b>Posizione di input sfumatura</b> *Mobile* | Posizione normalizzata della riga o colonna di pixel da campionare nell’input sfumatura. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input in scala di grigi</b> *Scala di grigi* PRIMARIO | Immagine in scala di grigio da ridefinire. |
| <b>Input sfumatura</b> *Colore/Scala di grigi* | La sfumatura viene campionata da questa immagine |


## Esempi

*Disponibile a breve.*
