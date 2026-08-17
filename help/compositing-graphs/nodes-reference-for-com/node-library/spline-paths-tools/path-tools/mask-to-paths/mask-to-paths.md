---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# Maschera su tracciati

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/mask-to-paths-icon.png "Icona nodo")

<b>In:</b> Strumenti spline e tracciati > Strumenti tracciato

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Converte un pattern di input in scala di grigio <b>Maschera</b> in un elenco di segmenti di percorso codificati nell&#39;output <b>Tracciati</b>.

Sono disponibili controlli sulla posizione iniziale dei percorsi generati e sul relativo ordine nell&#39;elenco.

I tracciati generati possono essere ulteriormente elaborati utilizzando nodi dedicati, ad esempio [Trasformazione 2D tracciato](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md), [Alterazione tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md), oppure convertiti in spline utilizzando il nodo [Tracciato fino alla spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per mappare o dispersione le forme lungo di essi.

</td>
</tr>
</table>

>[!NOTE]
>
> Il metodo utilizzato per codificare i percorsi è descritto nella pagina [Specifiche formato percorsi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md).

## Connettori di ingresso

<b>Maschera</b> *Scala di grigi*\
Il pattern di input che deve essere convertito in un elenco di percorsi.

## Connettori di uscita

<b>Anteprima</b> *Colore* Un&#39;anteprima composta sopra la maschera per visualizzare gli effetti dei parametri.

<b>Tracciati</b> *Colore*\
Un elenco di tracciati codificati in un’immagine a colori. ogni percorso descrive un elenco di segmenti codificati.\
Il risultato può essere elaborato utilizzando un altro nodo di elaborazione dei percorsi oppure inviato a un nodo [Percorsi nella spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) per elaborarlo ulteriormente come spline.

## Parametri

<b>Maschera uniforme</b> *Mobile*\
Applica arrotondamento alla maschera di input.\
È utile quando il pattern di input ha bordi molto netti, che di solito causano artefatti.

<b>Valore soglia maschera</b> *Mobile* Valore in scala di grigio di <b>Maschera</b> che verrà utilizzato per separare l&#39;esterno (valori &lt; Valore soglia maschera) e l&#39;interno (valori > Valore soglia maschera) della forma.

<b>Decimate Path</b> *Float* Controlla in modo implicito la quantità di segmenti che verranno generati.\
Un&#39;elevata quantità di decimazione renderà le forme rotonde un po&#39; poligonali, mentre nessuna decimazione genererà quasi un segmento per pixel.\
Una quantità ragionevole corrisponderà meglio alla forma sia delle linee rette che delle curve senza creare molti punti intermedi per le linee rette.

<b>Chiudere i tracciati aperti</b> *Booleani* Creare un segmento tra i vertici iniziale e finale dei tracciati aperti.\
La disattivazione di questa opzione può correggere le linee indesiderate che attraversano il pattern in modo imprevisto, tuttavia i percorsi potrebbero non essere più chiusi.

<b>Soglia angolo</b> *Mobile*\
Ogni vertice codificato nei tracciati può contenere un flag che indica se è rigido (ad esempio, un angolo) o uniforme.\
Questo parametro consente di contrassegnare più o meno angoli in base all’angolo tra i segmenti adiacenti.\
*Nota:* questo flag &#39;corner&#39; non è attualmente supportato da alcun nodo esistente, ma può essere utilizzato in un nodo [Path Vertex Processor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md). È inoltre possibile visualizzare gli angoli con il nodo [Anteprima tracciati](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md).

<b>Modalità di avvio percorso</b> *Intero* Metodo per selezionare quale vertice deve essere l&#39;inizio di ogni tracciato generato attorno alle forme nella maschera.\
Ciò ha un impatto significativo durante la conversione dei <b>percorsi in spline</b> generati utilizzando il nodo dedicato, poiché più nodi della spline utilizzano l&#39;inizio e la fine delle spline.\
*- Vertice più acuto:* Il vertice che forma l&#39;angolo più basso con i vertici precedente e successivo\
*- Vertice all&#39;estremità di una direzione specificata:* Ultimo vertice in una determinata direzione\
*- Vertice più vicino alla posizione specificata
* Vertice più lontano da una posizione specificata
* Funzione di avvio personalizzata:* Utilizzare una funzione personalizzata per selezionare il vertice da utilizzare come inizio di ogni percorso

<b>Direzione di avvio</b> *Mobile* Angolo che descrive la direzione utilizzata per selezionare il vertice di avvio. Per ogni tracciato viene selezionato l’ultimo vertice in questa direzione.\
Il valore è un *numero di giri* utilizzato per ruotare un vettore X-leftdirection. Questo significa che 0 imposta un vettore di direzione di (-1, 0) e 0,25 (90 gradi) imposta un vettore di direzione di (0, 1).\
*Nota:* questo parametro è disponibile quando <b>Modalità di avvio percorso</b> è impostata su &#39;Vertice all&#39;estremo di una direzione specificata&#39;

<b>Posizione di destinazione di avvio</b> *Float2* Posizione nell&#39;immagine utilizzata per selezionare il vertice di avvio.\
Per ogni percorso, viene selezionato il vertice più vicino o più lontano da questa posizione, in base alla <b>Modalità di avvio percorso</b> selezionata.\
*Nota:* questo parametro è disponibile quando <b>Modalità di avvio percorso</b> è impostato su &#39;Vertice più vicino a una posizione specificata&#39; o &#39;Vertice più lontano da una posizione specificata&#39;

<b>Funzione di avvio</b> *Mobile* Funzione utilizzata per selezionare il vertice di avvio. Restituisce un valore Float.\
Per ogni vertice viene eseguita la funzione e viene selezionato il vertice per il quale la funzione restituisce il *risultato più alto*.\
Variabili disponibili:\
*-* vertex.cornerness(Float)*:* Il punteggio del vertice come candidato per essere un angolo\
*-* vertex.pos(Float2)*:* Posizione del vertice nello spazio dell&#39;immagine\
*Nota:* questo parametro è disponibile quando Modalità avvio percorso è impostato su &#39;Vertice più vicino a una posizione specificata&#39; o &#39;Funzione di avvio personalizzata&#39;

<b>Modalità ordine</b> *Intero* Metodo di ordinamento dei tracciati generati.\
È possibile utilizzare il *riquadro di delimitazione* dei percorsi di posizione o dimensione (Bbox) come criterio per ordinare i percorsi.\
Questo ha un impatto significativo quando si convertono i <b>tracciati generati in spline</b> utilizzando il nodo dedicato, poiché più nodi spline utilizzano l&#39;ordine delle spline.\
*- Precedente (veloce):* Metodo utilizzato nella versione precedente di questo nodo, che offre prestazioni notevolmente migliori\
*- Per posizione centrale della casella di testo lungo la direzione:* I tracciati vengono ordinati in base alla posizione del centro della casella di testo, dal primo all&#39;ultimo lungo la direzione specificata\
*- Per casella di testo Posizione superiore sinistra della casella di testo lungo la direzione:* I tracciati vengono ordinati in base alla posizione dell&#39;angolo superiore sinistro della casella di testo, dal primo all&#39;ultimo lungo la direzione specificata\
*- In base alle dimensioni della casella - Da più grande a più piccolo:* i percorsi vengono ordinati in base alle dimensioni della casella, dal più grande al più piccolo\
*- In base alle dimensioni della casella - Da più piccolo a più grande:* i tracciati sono ordinati in base alle dimensioni della casella, dal più piccolo al più grande\
*- Funzione di ordinamento personalizzata:* Utilizzare una funzione personalizzata per ordinare i percorsi

<b>Direzione di ordinamento</b> *Mobile* Angolo che descrive la direzione utilizzata per ordinare i tracciati dal primo all&#39;ultimo lungo tale direzione.\
Il valore è un *numero di giri* utilizzato per ruotare un vettore di direzione X-left. Questo significa che 0 imposta un vettore di direzione di (-1, 0) e 0,25 (90 gradi) imposta un vettore di direzione di (0, 1).

<b>Funzione di ordinamento</b> *Mobile* Funzione utilizzata per ordinare i percorsi. Restituisce un valore Float.\
I percorsi vengono ordinati in *ordine crescente* in base al valore di questa funzione. In altre parole, il risultato della funzione per ogni percorso è la *chiave di ordinamento* utilizzata per ordinare i percorsi.\
Variabili disponibili:
* bbox.center (Float2): posizione del centro della casella Tracciato
* bbox.topleft (Float2): la posizione dell&#39;angolo superiore sinistro della casella Tracciato
* bbox.size (Float2): la dimensione della casella Tracciato (X: width, Y: height)

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths-Variant1-After">
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

![Esempio di nodo 2](../../../../../../assets/MaskToPaths-Demo2.gif "Esempio di nodo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/MaskToPaths-Demo1.gif "Esempio di nodo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 3: modalità di avvio](../../../../../../assets/MaskToPaths-Demo3.gif "Esempio di nodo 3: modalità di avvio"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 3: modalità di ordinamento](../../../../../../assets/MaskToPaths-Demo4.gif "Esempio di nodo 3: modalità di ordinamento"){zoomable="yes"}

</td>
</tr>
</table>
