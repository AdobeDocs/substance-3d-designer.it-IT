---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/cross-section.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sezione trasversale per creare maschere di sezione trasversale in base alle mappe di altezza per gli effetti di taglio e suddivisione in sezioni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Cross Section
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sezione trasversale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Sezione trasversale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![&#39;Icona nodo sezione trasversale&#39;](cross-section.resources/cross-section-2.png "&#39;Icona nodo sezione trasversale&#39;"){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disegna un profilo di sezione trasversale di un input. Può essere regolata in verticale o orizzontale e dispone di controlli per lo stile del disegno e lo scostamento del grafico e il ridimensionamento.

</td>
</tr>
</table>

Questo nodo è particolarmente utile per il debug e l&#39;analisi delle mappe di altezza. offre una vista del profilo con perfezionamento pixel, senza la necessità di nodi complessi o di una configurazione lunga e meno precisa nel vista 3D.

In alternativa, può essere utilizzato per creare forme e silhouette 2D difficili da ottenere altrimenti. In combinazione con un [nodo curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)può visualizzare direttamente il profilo della curva applicato a una sfumatura lineare.

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Coordinata sezione trasversale</b> *Virgola mobile* | Impostate le coordinate di campionamento della sezione. Può essere una coordinata X o Y a seconda dell&#39;asse di sezione. |
| <b>Asse di sezione</b> *Numero intero* | Impostate questa opzione se la sezione è verticale o orizzontale. |
| <b>Mostra helper</b> *Booleano* | Attiva una sovrapposizione che mostra la posizione della sezione sull’immagine di input. |
| <b>Impostazioni helper</b> |  |
| <b>Scala helper</b> *Virgola mobile* | La dimensione della sovrapposizione espressa come multiplo, dove 1,0 è l’intera immagine. |
| <b>Posizione helper</b> *Virgola mobile 2* | Posizione (X, Y) della sovrapposizione nell’immagine di output, dove (0,0, 0,0) è in alto a sinistra e (1,0, 1,0) è in basso a destra. |
| <b>Scala Height</b> *Virgola mobile* | Riduce l&#39;intero grafico. Utile per la visualizzazione dell’HDR. |
| <b>Offset Height</b> *Virgola mobile* | Sposta l’intero grafico in alto o in basso. Utile per la visualizzazione dell’HDR. |
| <b>Stile disegno</b> *Numero intero* | Consente di passare dal riempimento pieno al disegno con linea. |
| <b>Inverti sfumatura</b> *Booleano* | Se lo stile di disegno è impostato su *Sfumatura* o *Sfumatura specchiata*, consente di invertire la sfumatura senza influire sullo sfondo.<br><br>*Nota:* disponibile solo quando &quot;Stile di disegno&quot; è impostato su &quot;Sfumatura&quot; o &quot;Sfumatura specchiata&quot;. |
| <b>Uniforme/Poligonale</b> *Booleano* | Alterna la forma tra un profilo morbido perfetto o un profilo poligonale frastagliato.<br><br>*Nota:* disponibile solo quando &#39;Stile disegno&#39; è impostato su &#39;Uniforme&#39;, &#39;Sfumatura&#39; o &#39;Sfumatura speculare&#39;. |
| <b>Importo segmento</b> *Numero intero* | Imposta la quantità di segmenti da disegnare in stile poligonale o in stile linea.<br><br>*Nota:* disponibile solo quando &#39;Uniforme/Poligonale&#39; è impostato su &#39;Poligonale&#39; o quando &#39;Stile disegno&#39; è impostato su &#39;Linea&#39;. |
| <b>thickness di righe</b> *Virgola mobile* | Imposta il thickness della linea.<br><br>*Nota:* disponibile solo quando &#39;Stile disegno&#39; è impostato su &#39;Linea&#39;. |
| <b>Stile linea</b> *Numero intero* | Consente di scegliere la colorazione e il decadimento della linea.<br><br>*Nota:* disponibile solo quando &#39;Stile disegno&#39; è impostato su &#39;Linea&#39;. |
| <b>smoothness riga</b> *Virgola mobile* | Imposta il decadimento della sfumatura della linea.<br><br>*Nota:* disponibile solo quando &#39;Stile disegno&#39; è impostato su &#39;Linea&#39;. |
| <b>Colore</b> *Virgola mobile* | Colore in scala di grigi della linea o della forma.<br><br>*Nota:* disponibile solo quando &#39;Stile disegno&#39; è impostato su &#39;Tinta unita&#39; o &#39;Linea&#39; e &#39;Stile linea&#39; è impostato su &#39;Uniforme&#39; o &#39;Tinta unita&#39;. |
| <b>Colore di sfondo</b> *Virgola mobile* | Colore in scala di grigi dello sfondo.<br><br>*Nota:* non disponibile quando &#39;Stile disegno&#39; è impostato su &#39;Linea&#39; e &#39;Stile linea&#39; è impostato su &#39;ID segmento&#39; o &#39;Sfumatura lungo la linea&#39;. |

## Esempi

![Sezione trasversale: esempio 1](cross-section.resources/cross-section-example-01.gif "Sezione trasversale: esempio 1")

![Sezione trasversale: esempio 2](cross-section.resources/cross-section-example-02.gif "Sezione trasversale: esempio 2")

![Sezione trasversale: esempio 3](cross-section.resources/cross-section-example-03.png "Sezione trasversale: esempio 3")

![Sezione trasversale: esempio 4](cross-section.resources/cross-section-example-04.png "Sezione trasversale: esempio 4")
