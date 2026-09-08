---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: Utilizzare il nodo Quadratico Poly spline per creare spline quadratiche complesse con più punti di controllo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Poly Quadratic)
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Spline (Poly Quadratic)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-poly-quadratic-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una spline lungo diversi punti. La quantità e le posizioni di questi punti potrebbero essere arbitrarie o raccolte da un nodo [Elenco di punti](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

</td>
</tr>
</table>

La traiettoria della spline può essere smussata dai suoi punti intermedi, in quanto ogni punto intermedio è il punto di incontro delle tangenti &quot;out&quot; e &quot;in&quot; dei suoi vicini.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |
| <b>Anteprima punti</b> <i>Scala di grigi</i> | Anteprima dei punti come immagine in scala di grigio. |
| <b>Elenco dei punti di input</b> <i>Colore</i> | (disponibile quando &quot;Usa elenco punti di input&quot; è True) Un elenco di punti codificati nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Parte intera: Smoothness;<br> - Parte frazionale: Thickness. |
| <b>Numero punto</b> <i>Numero intero</i> | (disponibile quando &quot;Usa elenco dei punti di input&quot; è True) Il numero di punti. |

>[!IMPORTANT]
>
> I connettori <b>Elenco punti</b> e <b>Numero punto</b> sono *incompatibili* con <b>Coord spline</b>, <b>Dati spline</b> e <b>Quantità spline</b>, in quanto si basano su dati diversi.

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Quantità punti</b> <i>Numero intero</i> | Numero arbitrario di punti utilizzati per creare la spline. |
| <b>Modalità connessione spline di input</b> <i>Numero intero</i> | Metodo utilizzato per connettere le spline di input:<br>- <i>Automatico:</i> L&#39;estremità dell&#39;ultima spline di input è connessa all&#39;inizio della spline generata e l&#39;estremità della spline generata è connessa all&#39;inizio della prima spline di input;<br>- <i>Manuale:</i> È possibile specificare quale delle spline di input deve essere connessa alle estremità della spline generata e dove sulle spline di input queste connessioni devono atterrare. |
| <b>Chiudi spline</b> <i>Booleano</i> | Controlla se il punto finale della spline deve essere collegato al punto iniziale.<br>La smussatura applicata alla spline nei punti iniziale e finale è specificata dai valori di Smoothness di tali punti. |
| <b>Direzione capovolgimento</b> <i>Booleano</i> | Inverte la direzione della spline. |
| <b>Usa elenco punti di input</b> <i>Booleano</i> | Utilizzare l&#39;elenco di punti fornito ai connettori di input Elenco punti di input e Numero punto invece di un elenco arbitrario di punti.<br>L&#39;elenco di punti può essere fornito da un nodo [Elenco punti](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md). |
| <b>Collega avvio a spline di input</b> <i>Booleano</i> | Se è impostato su True, l&#39;inizio della spline generata viene collegato all&#39;ultimo punto dell&#39;ultima spline nelle spline di input. |
| <b>Avvia indice spline connessione</b> <i>Numero intero</i> | (disponibile quando la modalità di connessione della spline di input è impostata su &quot;Manuale&quot; e l&#39;opzione &quot;Collega inizio a spline di input&quot; è impostata su &quot;True&quot;) L&#39;indice della spline di input che deve essere collegato all&#39;inizio della spline generata. |
| <b>Avvia posizione connessione</b> <i>Mobile</i> | (disponibile quando la modalità di connessione della spline di input è impostata su &quot;Manuale&quot; e l&#39;opzione &quot;Connetti inizio a spline di input&quot; è impostata su &quot;True&quot;) La posizione sulla spline di input selezionata in cui dovrebbe terminare il collegamento con l&#39;inizio della spline generata.<br>Questo valore rappresenta la lunghezza normalizzata della spline di input selezionata. |
| <b>Connetti estremità alla spline di input</b> <i>Booleano</i> | Se è True, l&#39;estremità della spline generata viene connessa al primo punto della prima spline nelle spline di input. |
| <b>Fine indice spline connessione</b> <i>Numero intero</i> | (disponibile quando &quot;Modalità connessione spline di input&quot; è impostata su &quot;Manuale&quot; e &quot;Connetti estremità a spline di input&quot; è impostata su &quot;True&quot;) L&#39;indice della spline di input che deve essere collegata all&#39;estremità della spline generata. |
| <b>Posizione di fine connessione</b> <i>Mobile</i> | (disponibile quando la modalità di connessione della spline di input è impostata su &quot;Manuale&quot; e l&#39;opzione &quot;Connetti estremità alla spline di input&quot; è impostata su &quot;Vero&quot;) La posizione sulla spline di input selezionata in cui dovrebbe verificarsi il collegamento all&#39;estremità della spline generata.<br>Questo valore rappresenta la lunghezza normalizzata della spline di input selezionata. |
| <b>Distribuzione uniforme</b> <i>Booleano</i> | Se è impostato su True, i punti della spline sono distribuiti uniformemente dall&#39;inizio alla fine. |
| <b>Aggiungi spline di input</b> <i>Booleano</i> | Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline in risoluzioni non quadrate.<br>Questo influisce anche sulla distribuzione uniforme. |
| <b>Regolazione Smoothness globale</b> <i>Mobile</i> | Applica un offset uniforme al valore di smoothness di tutti i punti.<br>Il valore di smoothness risultante è fissato all&#39;intervallo [0;1]. |
| <b>Proprietà punti</b> |  |
| <b>p# Proprietà</b> <i>Float3</i> | Imposta le proprietà del punto p#.<br>- <i>Height:</i> Regola il height del punto in cui un valore inferiore indica una posizione inferiore o più profonda;<br>- <i>Smoothness:</i> Sposta l&#39;inizio dell&#39;arrotondamento della spline in corrispondenza di p#, in cui un valore pari a 0 determina una traiettoria rigida e 1 in una completamente arrotondata;<br>- <i>Thickness:</i> Regola il thickness della spline in corrispondenza di p#. Thickness viene utilizzato da nodi Spline specifici. |
| <b>Coordinate punti</b> |  |
| <b>p#</b> <i>Float2</i> | Imposta la posizione del punto p# nello spazio della texture. |
| <b>Anteprima</b> |  |
| <b>Mostra tangenti</b> <i>Booleano</i> | Visualizza le tangenti dei punti p1 e p3 a p2 nell&#39;output Preview. |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Mostra busta Thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Mostra etichetta punti</b> <i>Booleano</i> | Per ogni punto, visualizza il nome del punto accanto nell&#39;output &quot;Anteprima&quot;. |
| <b>Dimensioni etichetta punti</b> <i>Mobile</i> | (Disponibile quando &#39;Mostra etichetta punti&#39; è impostato su &#39;True&#39;) Dimensione dell&#39;etichetta per ogni punto nello spazio della texture, dove 0,1 è un decimo della larghezza della texture. |
| <b>Mostra punti</b> <i>Booleano</i> | Visualizza i punti di controllo della spline. |
| <b>Dimensioni Punti</b> <i>Mobile</i> | (Disponibile quando &#39;Mostra punti&#39; è impostato su &#39;True&#39;) Raggio dei punti nello spazio della texture, dove 0,1 è un decimo della larghezza della texture. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.<br>Un valore più elevato determina una linea più fluida. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>
