---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Usate il nodo Multi Switch per passare da una texture di input a un’altra in base a un selettore per la selezione di texture condizionale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Switch multipli
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# Switch multipli

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## Switch multipli (scala di grigi)

**Ingresso:** *Filtri/Fusione*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Funziona come una casella di selezione, passando solo attraverso l&#39;input definito dal parametro &#39;Input Selection&#39;. Pertanto, se sono collegati due Input, ne verrà restituito solo uno (non modificato), a seconda della scelta dell’utente.

Molto utile per aggiungere a un grafico molte opzioni diverse. In combinazione con [l&#39;esposizione](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) (preferibilmente come elenco a discesa), è possibile apportare molte personalizzazioni.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usare &quot;Multi Switch&quot; per gli ingressi di colore e &quot;Multi Switch Grayscale&quot; per gli ingressi in scala di grigi.

## Parametri

### Input

* **Input 1-20**: *Input colore*

### Parametri

* **Numero di input**: *2 - 20* Quantità di input da esporre. Importante: non rimuove le connessioni quando il numero viene ridotto.
* **Selezione input**: *1 - 20* Specifica l&#39;input da restituire come risultato.

## Immagini di esempio

</td>
</tr>
</table>
