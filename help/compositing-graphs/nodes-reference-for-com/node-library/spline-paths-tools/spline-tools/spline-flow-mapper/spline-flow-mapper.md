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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# Spline Flow Mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-flow-mapper.resources/spline-flow-mapper-01.png "Icona nodo")

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

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |
| <b>Curva del profilo di attenuazione</b> <i>Scala di grigi</i> | <span id="_Hlk135812146"></span>Immagine che descrive una curva utilizzando i valori della prima riga di pixel. Quando il parametro Profilo di attenuazione è impostato su Curva profilo di input, questo input viene utilizzato per controllare la sfumatura per l&#39;attenuazione dei dati del vettore di flusso tracciati lungo la spline.<br>È possibile utilizzare un nodo [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) per creare la curva. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | La mappa del flusso di output codificata in un’immagine a colori. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Importo segmenti</b> <i>Numero intero</i> | Le spline vengono semplificate in segmenti prima che i dati del flusso vettoriale le attraversino. Una maggiore quantità di segmenti determina una mappatura del flusso più fluida lungo le curve. |
| <b>Modalità</b> <i>Numero intero</i> | Metodo di selezione delle spline lungo le quali devono essere disegnati i dati del flusso vettoriale:<br><br>- <i>Disegna elenco spline</i>: vengono utilizzate tutte le spline nell&#39;elenco di input;<br>- <i>Disegna spline singola</i>: viene utilizzata solo la spline con l&#39;indice specificato;<br>- <i>Disegna intervallo spline</i>: vengono utilizzate solo le spline che l&#39;indice è incluso nell&#39;intervallo specificato. |
| <b>Disegna indice spline</b> <i>Intero</i> (disponibile quando &#39;Modalità&#39; è impostato su &#39;Disegna singola spline&#39;) | Indice della spline lungo la quale devono essere disegnati i dati del flusso vettoriale. |
| <b>Disegna intervallo spline</b> <i>Intero2</i> (disponibile quando &#39;Modalità&#39; è impostato su &#39;Disegna intervallo spline&#39;) | Intervallo di indici per le spline lungo le quali devono essere disegnati i dati del flusso vettoriale. |
| <b>Modalità Thickness</b> <i>Numero intero</i> | Metodo di impostazione del thickness dei dati del flusso vettoriale disegnati<br><br>- <i>Manuale</i>: impostare il thickness in modo esplicito con un valore arbitrario;<br>- <i>Da spline</i>: utilizzare il thickness della spline. |
| <b>Thickness</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità Thickness&#39; è impostato su &#39;Manuale&#39;) | Valore arbitrario per il thickness dei dati di flusso vettoriali disegnati lungo le spline. |
| <b>Moltiplicatore Thickness</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità Thickness&#39; è impostato su &#39;Da spline&#39;) | Moltiplicatore globale per il thickness dei dati di flusso vettoriali disegnati lungo le spline, quando quel thickness è guidato da quello delle spline. |
| <b>Direzione</b> <i>Numero intero</i> | Direzione del flusso vettoriale in relazione alla spline.<br><br>- <i>Tangente</i>: utilizzare il vettore tangente della spline;<br>- <i>Normale</i>: utilizzare il vettore normale della spline;<br>- <i>Specchiato normale</i>: utilizzare la versione specchiata del vettore normale della spline. |
| <b>Direzione capovolgimento</b> <i>Booleano</i> | Inverte la direzione delle spline, influendo anche sulla direzione del vettore di flusso. |
| <b>Profilo di attenuazione</b> <i>Numero intero</i> | La sfumatura utilizzata per disegnare l&#39;attenuazione dei dati del vettore di flusso disegnati lungo la spline:<br><br>- <i>Lineare</i>: utilizzare una sfumatura lineare;<br>- <i>Gaussiano</i>: utilizzare una sfumatura gaussiana<br>- <i>Curva profilo di input</i>: utilizzare la curva fornita all&#39;input della curva profilo di attenuazione come sfumatura. |
| <b>Avvia attenuazione</b> <i>Booleano</i> | <span id="_Hlk135769398"></span>Aggiunge un semicerchio all&#39;inizio della spline. Il semicerchio usa la stessa attenuazione della spline. |
| <b>Termina attenuazione</b> <i>Booleano</i> | Aggiunge un semicerchio alla fine della spline. Il semicerchio usa la stessa attenuazione della spline. |
| <b>Attenuazione Height spline</b> <i>Mobile</i> | L&#39;intensità dei dati vettoriali di flusso disegnati lungo la spline viene moltiplicata sul height della spline, dove i dati disegnati vengono dissolti con il colore neutro (0,5, 0,5, 0) dello sfondo quando il height si avvicina a 0. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate. Questo incide anche sulla distribuzione uniforme. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-flow-mapper.resources/spline-flow-mapper-02.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-flow-mapper.resources/spline-flow-mapper-03.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-flow-mapper.resources/spline-flow-mapper-04.gif "Esempio di nodo 2")

</td>
</tr>
</table>
