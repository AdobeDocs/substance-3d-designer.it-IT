---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Utilizzate il nodo Mappatura flusso spline per creare pattern di texture fluide lungo tracciati spline per ottenere effetti organici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Flow Mapper
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# Spline Flow Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-flow-mapper-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disegna una mappa di flusso in cui i dati vettoriali di flusso vengono disegnati lungo le spline di input.

In questo modo potete utilizzare le spline per controllare la direzione, la traiettoria, l&#39;intensità e il thickness del flusso, nonché la sfumatura utilizzata per sfumare i dati disegnati sullo sfondo neutro.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Il risultato può includere artefatti indesiderati all&#39;esterno dell&#39;inviluppo della spline quando si utilizzano valori di thickness molto bassi. Questo è un problema noto.

## Connettori di ingresso

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:\
<b> R</b> - Posizione X\
<b> G</b> - Posizione Y\
<b> B</b> - Height\
    <b>A</b> - Dati compressi:\
        * Segno: la spline è chiusa (negativa) o aperta (positiva);\
        * Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.\
<b> R</b> - Tangenti X\
<b> G</b> - Tangenti Y\
<b> B</b> - Non in uso\
<b> A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di input.

<b>Curva del profilo di attenuazione</b> *Scala di grigi*<span id="_Hlk135812146"></span> Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Quando il parametro Profilo di attenuazione è impostato su Curva profilo di input, questo input viene utilizzato per controllare la sfumatura per l&#39;attenuazione dei dati del vettore di flusso tracciati lungo la spline.\
È possibile utilizzare un nodo [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) per creare la curva.

## Connettori di uscita

<b>Output</b> *Colore* La mappa del flusso di output codificata in un&#39;immagine a colori.

## Parametri

<b>Importo segmenti</b> *Interi* Le spline vengono semplificate in segmenti prima che i dati del flusso vettoriale li attraversino.\
Una maggiore quantità di segmenti determina una mappatura del flusso più fluida lungo le curve.

<b>Modalità</b> *Intero* Metodo di selezione delle spline lungo le quali devono essere disegnati i dati del flusso vettoriale:\
*- Disegna elenco spline*: vengono utilizzate tutte le spline nell&#39;elenco di input;\
*- Disegna spline singola*: viene utilizzata solo la spline con l&#39;indice specificato;\
*- Disegna intervallo spline*: vengono utilizzate solo le spline incluse nell&#39;intervallo specificato.

<b>Disegna indice spline</b> *Intero* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna spline singola&quot;)Indice della spline lungo la quale devono essere disegnati i dati del flusso vettoriale.

<b>Disegna intervallo spline</b> *Intero2* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna intervallo spline&quot;)Intervallo di indici per le spline lungo le quali devono essere disegnati i dati del flusso vettoriale.

<b>Modalità Thickness</b> *Intero* Metodo di impostazione del thickness dei dati di flusso vettoriali disegnati\
*- Manuale*: impostare il thickness in modo esplicito con un valore arbitrario;\
*- Da spline*: utilizzare il thickness della spline.

<b>Thickness</b> *Float* (disponibile quando &quot;Modalità Thickness&quot; è impostato su &quot;Manuale&quot;)Valore arbitrario per il thickness dei dati del flusso vettoriale disegnati lungo le spline.<b></b>

<b>Moltiplicatore Thickness</b> *Float* (disponibile quando &quot;Modalità Thickness&quot; è impostato su &quot;Da spline&quot;)Moltiplicatore globale per il thickness dei dati del flusso vettoriale disegnati lungo le spline, quando tale thickness è guidato da quello delle spline.

<b>Direzione</b> *Intero* Direzione del flusso vettoriale in relazione alla spline.\
*- Tangente*: utilizzate il vettore tangente della spline;\
*- Normale*: utilizza il vettore normale della spline;\
*- Con mirroring normale*: utilizzare la versione specchiata del vettore normale della spline.

<b>Direzione capovolgimento</b> *Booleano* Inverte la direzione delle spline, che influisce anche sulla direzione del vettore di flusso.

<b>Profilo di attenuazione</b> *Intero* La sfumatura utilizzata per disegnare l&#39;attenuazione dei dati vettoriali di flusso disegnati lungo la spline:\
*- Lineare*: utilizza una sfumatura lineare;\
*- Gaussiano*: utilizzare una sfumatura gaussiana\
*- Curva profilo di input*: utilizza la curva fornita all&#39;input Curva profilo di attenuazione come sfumatura.

<b>Avvia attenuazione</b> *Booleano*<span id="_Hlk135769398"></span> Aggiunge un semicerchio all&#39;inizio della spline. Il semicerchio usa la stessa attenuazione della spline.

<b>Termina attenuazione</b> *Booleano* Aggiunge un semicerchio alla fine della spline. Il semicerchio usa la stessa attenuazione della spline.

<b>Attenuazione Height spline</b> *Mobile* L&#39;intensità dei dati vettoriali di flusso disegnati lungo la spline viene moltiplicata sul height della spline, dove i dati disegnati sfumano al colore neutro (0,5, 0,5, 0) dello sfondo man mano che il height si avvicina a 0.

<b>Correzione non quadrata </b>*Booleano* Regola le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineFlowMapper-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>
