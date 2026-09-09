---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Utilizzare il nodo Ombre RT per calcolare le informazioni in tempo reale sulle ombre dalla geometria per creare effetti di illuminazione dinamici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombre RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Ombre RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo Ombre RT](rt-shadow.resources/rt-shadow.png "Icona nodo Ombre RT")

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera le ombre ray tracing da un input mappa height.

Questo nodo non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Esempi</b> <i>Numero intero</i> | Numero di raggi utilizzati per calcolare le ombre.<br>Un valore più elevato fornisce un risultato più uniforme e preciso, a scapito delle prestazioni. |
| <b>Modalità</b> <i>Numero intero</i> | Metodo di disegno delle ombre sulla superficie. |
| <b>Scala Height</b> <i>Mobile</i> | Un moltiplicatore per l’intensità della mappa del height di input. |
| <b>Posizione chiara</b> <i>Float2</i> | Posizione della sorgente luminosa su una sfera che racchiude la superficie:<br><br>- <b>X</b>: posizione orizzontale, in numero di giri;<br>- <b>Y</b>: posizione verticale, dove 0,5 è lo zenit e 0/1 è l&#39;orizzonte. |
| <b>Intensità luce</b> <i>Mobile</i> | Intensità della sorgente luminosa. |
| <b>Dimensioni Chiare</b> <i>Float2</i> | (Disponibile se <b>Modalità</b> è impostato su <i>Ombreggiato</i>) La dimensione della sorgente luminosa come rettangolo. |
| <b>Scala luminosa (ombre morbide)</b> <i>Mobile</i> | Moltiplicatore per il contributo delle <b>dimensioni della luce</b> alla direzione dei raggi.<br>Un valore più elevato determina ombre più omogenee. |
| <b>Luce sopra l&#39;orizzonte</b> <i>Booleano</i> | Se <b>Posizione luce</b> è impostato in modo da posizionare la luce sotto l&#39;orizzonte, questo parametro impedisce alla luce di superare tale soglia, il che significa che i valori Y sono bloccati nell&#39;intervallo [0;1]. |
| <b>Opacità ombra</b> <i>Mobile</i> | Moltiplicatore per l’opacità delle ombre disegnate sulla superficie. |
| <b>Attenuazione ombra</b> <i>Mobile</i> | Moltiplicatore per l&#39;attenuazione delle ombre più lontane sono dall&#39;ingombro.<br>Un valore pari a 0 genera ombre uniformi (vengono comunque applicate ombre morbide). |
| <b>Lunghezza massima ombre</b> <i>Mobile</i> | Distanza massima a cui è possibile disegnare un&#39;ombra dal relativo caster.<br>Un valore pari a 0 non produce ombre visibili. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-01.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/RTShadows-03.jpg" />
        </td>
    </tr>
</table>
