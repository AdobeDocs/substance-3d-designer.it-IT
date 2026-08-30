---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: Utilizzate il nodo Maschera su tracciati per convertire le texture della maschera in dati di tracciato per la generazione procedurale del tracciato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Maschera su tracciati
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Maschera su tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](mask-to-paths.resources/mask-to-paths-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Converte un pattern di input in scala di grigio <b>Maschera</b> in un elenco di segmenti di percorso codificati nell&#39;output <b>Tracciati</b>.

Sono disponibili controlli sulla posizione iniziale dei percorsi generati e sul relativo ordine nell&#39;elenco.

I tracciati generati possono essere ulteriormente elaborati utilizzando nodi dedicati, ad esempio [Trasforma 2D tracciato](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Alterazione tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md), oppure convertiti in spline utilizzando il nodo [Tracciato fino alla spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per mappare o dispersione le forme lungo di essi.

</td>
</tr>
</table>

>[!NOTE]
>
> Il metodo utilizzato per codificare i percorsi è descritto nella pagina [Specifiche formato percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera</b> <i>Scala di grigi</i> | Il pattern di input che deve essere convertito in un elenco di percorsi. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Colore</i> | Anteprima composta sopra la maschera per visualizzare gli effetti dei parametri. |
| <b>Tracciati</b> <i>Colore</i> | Un elenco di tracciati codificati in un’immagine a colori. ogni percorso descrive un elenco di segmenti codificati.<br>Il risultato può essere elaborato utilizzando un altro nodo di elaborazione dei percorsi oppure inviato a un nodo [Percorsi nella spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Maschera uniforme</b> <i>Mobile</i> | Applica arrotondamento alla maschera di input.<br>Utile quando il pattern di input presenta bordi molto netti, che in genere causano artefatti. |
| <b>Valore soglia maschera</b> <i>Mobile</i> | Il valore in scala di grigi di <b>Maschera</b> che verrà utilizzato per separare l&#39;esterno (valori &lt; Valore soglia maschera) e l&#39;interno (valori > Valore soglia maschera) della forma. |
| <b>Decimare il percorso</b> <i>Mobile</i> | Controlla in modo implicito la quantità di segmenti che verranno generati.<br>Un numero elevato di decimazioni renderà le forme rotonde leggermente poligonali, mentre nessuna decimazione genererà quasi un segmento per pixel.<br>Una quantità ragionevole corrisponderà meglio alla forma sia delle linee rette che delle curve senza creare molti punti intermedi per le linee rette. |
| <b>Chiudere i tracciati aperti</b> <i>Booleano</i> | Create un segmento tra i vertici iniziale e finale dei tracciati aperti.<br>Se si disabilita questa opzione, è possibile che le linee indesiderate che attraversano il pattern vengano corrette in modo imprevisto, tuttavia i percorsi potrebbero non essere più chiusi. |
| <b>Soglia angolo</b> <i>Mobile</i> | Ogni vertice codificato nei tracciati può contenere un flag che indica se è rigido (ad esempio, un angolo) o uniforme.<br>Questo parametro consente di contrassegnare più o meno angoli in base all&#39;angolo tra i segmenti adiacenti.<br><i>Nota:</i> Questo flag &#39;corner&#39; non è attualmente supportato da alcun nodo esistente, ma può essere utilizzato in un nodo [Path Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). È inoltre possibile visualizzare gli angoli con il nodo [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md). |
| <b>Modalità di avvio percorso</b> <i>Numero intero</i> | Metodo di selezione del vertice che deve essere l&#39;inizio di ogni tracciato generato attorno alle forme nella maschera.<br>Questo metodo ha un impatto significativo quando si convertono i <b>tracciati in spline</b> generati utilizzando il nodo dedicato, in quanto più nodi della spline utilizzano l&#39;inizio e la fine delle spline.<br>*- Vertice più acuto:* Il vertice che forma l&#39;angolo più basso con i vertici precedente e successivo <br>*- Vertice all&#39;estremo di una direzione specificata:* Ultimo vertice in una determinata direzione <br>*- Vertice più vicino a una posizione specificata<br>* Vertice più lontano da una posizione specificata<br> funzione di avvio:* Utilizzare una funzione personalizzata per selezionare il vertice da utilizzare come inizio di ogni percorso |
| <b>Direzione di avvio</b> <i>Mobile</i> | Angolo che descrive la direzione utilizzata per selezionare il vertice di avvio. Per ogni tracciato viene selezionato l’ultimo vertice in questa direzione.<br>Il valore è un *numero di giri* utilizzato per ruotare un vettore X-leftdirection. Questo significa che 0 imposta un vettore di direzione di (-1, 0) e 0,25 (90 gradi) imposta un vettore di direzione di (0, 1).<br><i>Nota:</i> Questo parametro è disponibile quando <b>Modalità di avvio percorso</b> è impostato su &#39;Vertice all&#39;estremo di una direzione specificata&#39; |
| <b>Posizione di destinazione di avvio</b> <i>Float2</i> | Posizione nell’immagine utilizzata per selezionare il vertice di avvio.<br>Per ogni percorso, viene selezionato il vertice più vicino o più lontano da questa posizione, in base alla <b>Modalità di avvio del percorso</b> selezionata.<br><i>Nota:</i> Questo parametro è disponibile quando <b>Modalità di avvio del percorso</b> è impostato su &#39;Vertice più vicino a una posizione specificata&#39; o &#39;Vertice più lontano da una posizione specificata&#39; |
| <b>Funzione di avvio</b> <i>Mobile</i> | Funzione utilizzata per selezionare il vertice di avvio. Restituisce un valore Float.<br>Per ogni vertice, la funzione viene eseguita e viene selezionato il vertice per il quale la funzione restituisce il *risultato più elevato*.<br>Variabili disponibili:<br>*-* vertex.cornerness(Virgola mobile)*:* Il punteggio del vertice come candidato per essere un angolo <br>*-* vertex.pos(Virgola mobile 2)*:* La posizione del vertice nello spazio immagine<br><i>Nota:</i> Questo parametro è disponibile quando la modalità di avvio del percorso è impostata su &#39;Vertice più vicino a una posizione specificata&#39; o &#39;Funzione di avvio personalizzata&#39; |
| <b>Modalità ordine</b> <i>Numero intero</i> | Metodo di ordinamento dei percorsi generati.<br>È possibile utilizzare la posizione o le dimensioni del *rettangolo di selezione* (Bbox) dei percorsi come criterio per l&#39;ordinamento dei percorsi.<br>Ciò influisce in modo significativo sulla conversione dei <b>percorsi in spline</b> generati utilizzando il nodo dedicato, poiché più nodi spline utilizzano l&#39;ordine delle spline.<br>*- Legacy (fast):* Il metodo utilizzato nella versione precedente di questo nodo, che offre prestazioni notevolmente migliori <br>*- Per casella di selezione la posizione centrale lungo la direzione:* i percorsi vengono ordinati in base alla posizione del centro della casella di raggruppamento, dal primo all&#39;ultimo lungo la direzione specificata <br>*- Per casella di testo Posizione superiore sinistra della casella di testo lungo la direzione:* I tracciati sono ordinati in base alla posizione dell&#39;angolo superiore sinistro della casella di testo, dal primo all&#39;ultimo lungo la direzione specificata <br>*- Per casella di testo - Da più grande a più piccolo:* I tracciati sono ordinati in base alle dimensioni della casella di testo, da più grande a più piccolo <br>*- Per casella di testo - Da più piccolo a più grande:* I tracciati sono ordinati in base alle dimensioni della casella di testo, da più piccolo a più grande <br>*- Ordinamento personalizzato funzione:* Utilizzare una funzione personalizzata per ordinare i percorsi |
| <b>Direzione ordinamento</b> <i>Mobile</i> | Angolo che descrive la direzione utilizzata per ordinare i tracciati dal primo all&#39;ultimo lungo tale direzione.<br>Il valore è un *numero di giri* utilizzato per ruotare un vettore di direzione X-left. Questo significa che 0 imposta un vettore di direzione di (-1, 0) e 0,25 (90 gradi) imposta un vettore di direzione di (0, 1). |
| <b>Funzione di ordinamento</b> <i>Mobile</i> | Funzione utilizzata per ordinare i tracciati. Restituisce un valore Float.<br>I percorsi sono ordinati in *ordine crescente* in base al valore di questa funzione. In altre parole, il risultato della funzione per ogni percorso è la *chiave di ordinamento* utilizzata per ordinare i percorsi.<br>Variabili disponibili:<br>* bbox.center (Virgola mobile 2): la posizione del centro della casella percorso<br>* bbox.topleft (Virgola mobile 2): la posizione dell&#39;angolo superiore sinistro della casella percorso<br>* bbox.size (Virgola mobile 2): la dimensione della casella percorso (X: larghezza, Y: height) |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="mask-to-paths.resources/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 2](mask-to-paths.resources/MaskToPaths-Demo2.gif "Esempio di nodo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 1](mask-to-paths.resources/MaskToPaths-Demo1.gif "Esempio di nodo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 3: modalità di avvio](mask-to-paths.resources/MaskToPaths-Demo3.gif "Esempio di nodo 3: modalità di avvio"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 3: modalità di ordinamento](mask-to-paths.resources/MaskToPaths-Demo4.gif "Esempio di nodo 3: modalità di ordinamento"){zoomable="yes"}

</td>
</tr>
</table>
