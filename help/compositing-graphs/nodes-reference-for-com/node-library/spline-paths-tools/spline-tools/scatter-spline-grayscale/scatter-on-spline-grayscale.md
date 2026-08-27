---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dispersione su spline scala di grigi per distribuire gli elementi in scala di grigi lungo i tracciati spline per i pattern procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersione su scala di grigi spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '2812'
ht-degree: 0%

---


# Dispersione su scala di grigi spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/scatter-on-spline-grayscale-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disegna i pattern specificati lungo le spline di input sullo sfondo di input.

</td>
</tr>
</table>

Il nodo offre opzioni di personalizzazione avanzate per controllare la modalità di dispersione dei pattern.

Alcuni aspetti della dispersione possono essere controllati utilizzando immagini provenienti da altri nodi nel grafico per migliorare l’aspetto dinamico del risultato.

>[!NOTE]
>
> Vedere anche [Dispersione su Spline Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md).

## Connettori di ingresso

<b>Sfondo </b>*Scala di grigi* (primaria)Immagine in scala di grigi su cui devono essere disegnate spline.

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

<b>Input pattern n. </b> *Scala di grigi* Motivi che devono essere sparsi lungo le spline.

<b>Mappa scala</b> *Scala di grigi* Mappa che controlla la scala dei pattern diffusi. L’effetto di questa mappa è controllato dal parametro &quot;Moltiplicatore input mappa scala&quot; ed è combinato con gli altri parametri del gruppo &quot;Dimensione&quot;.

<b>Mappa Height</b> *Scala di grigi* Mappa che controlla il height dei pattern sparsi. L’effetto di questa mappa è controllato dal parametro &quot;Moltiplicatore di input di Height&quot; ed è combinato con gli altri parametri &quot;Colore&quot; del gruppo &quot;Colore&quot;.

<b>Mappa maschera</b> *Scala di grigi* Mappa che controlla la mascheratura dei pattern sparsi. L’effetto di questa mappa è controllato dal parametro &quot;Soglia mappa maschera&quot; ed è combinato con gli altri parametri &quot;Maschera&quot; nel gruppo &quot;Colore&quot;.

## Connettori di uscita

<b>Output</b> *Scala di grigi* Immagine che rappresenta i pattern distribuiti lungo la spline di input sullo sfondo dell&#39;input.

## Parametri

<b>Input spline</b> *Intero* Metodo di selezione delle spline da utilizzare per i pattern di dispersione:
* *Tutte le spline*: utilizzare tutte le spline nell&#39;elenco di input;
* *Spline singola*: utilizzare solo la spline specificata dall&#39;elenco di input;
* *Intervallo spline*: utilizzare solo le spline dell&#39;intervallo specificato dall&#39;elenco di input.

<b>Indice spline</b> *Intero* (disponibile quando &quot;Input spline&quot; è impostato su &quot;Single Spline&quot;)Indice di elenco della spline da utilizzare per i pattern di dispersione.

<b>Intervallo spline</b> *Intero2* (disponibile quando &quot;Input spline&quot; è impostato su &quot;Intervallo spline&quot;)Intervallo di indici di elenco, incluse le spline, che devono essere utilizzate per i pattern di dispersione.

<b>Modalità Dispersione</b> *Intero* Metodo di dispersione dei pattern lungo le spline, che influisce sulla quantità di pattern su ciascuna spline:
* Quantità forma: la quantità specificata di motivi uniformemente distribuiti;
* Spaziatura tra forme: il numero di pattern viene regolato automaticamente in modo da adattarsi alla spaziatura uniforme specificata.\
  In entrambi i casi, il primo e l&#39;ultimo pattern si trovano esattamente all&#39;inizio e alla fine di ciascuna spline.

<b>Quantità forma</b> *Intero* (disponibile quando &quot;Modalità Dispersione&quot; è impostato su &quot;Quantità forma&quot;)Quantità di motivi uniformemente distribuiti lungo ciascuna spline.

<b>Distribuzione della forma lungo la spline</b> *Intero* (disponibile quando &quot;Modalità Dispersione&quot; è impostato su &quot;Quantità forma&quot;)Metodo di distribuzione dei pattern lungo una spline:
* *Dall&#39;origine*: la spaziatura dei motivi è influenzata dalle tangenti del punto della spline, in cui le forme sono più distanti vicino a punti con tangenti lunghe;
* *Uniforme*: i pattern sono distribuiti uniformemente lungo la spline indipendentemente dalle tangenti e dalla traiettoria.

<b>Spaziatura tra forme</b> *Mobile* (disponibile quando &quot;Modalità Dispersione&quot; è impostato su &quot;Spaziatura forma&quot;)La distanza minima lungo una spline in base alla quale i pattern devono essere distanziati, mentre il primo e l&#39;ultimo pattern devono ancora atterrare rispettivamente all&#39;inizio e alla fine di ogni spline.

<b>Inizio</b> *Mobile*<span id="_Hlk135680521"></span> Sposta il punto dall&#39;inizio di una spline nel punto in cui inizia la dispersione. Il valore è la lunghezza normalizzata di ogni spline.

<b>Fine</b> *Mobile* Sposta il punto dall&#39;inizio di una spline nel punto in cui termina la dispersione. Il valore è la lunghezza normalizzata di ogni spline.

<b>Pivot forma</b> *Float2* Sposta il perno del pattern X e Y nello spazio tangente della spline.\
Considerando che il perno è ciò che viene posizionato sulla spline, questo sposta efficacemente i pattern lungo o perpendicolarmente alla spline.\
Nota: le posizioni dei perni influiscono sull’effetto dei parametri &quot;Scala&quot; e &quot;Rotazione (pivot)&quot;.

+++Motivo
<b>Pattern</b> *Intero* Motivo che deve essere sparso lungo le spline:\
*- Input pattern*: utilizzare i pattern forniti agli input ‘Pattern Input #’;\
*- Quadrato;
* Disco;
* Paraboloide;
* Campana;
* gaussiana;
* Spina;
* Piramide;
* mattoni;
* Gradazione;
* Onde;
* Mezza campana;
* Campana Ridotta;
* Mezzaluna;
* Capsula;
* Cono;
* Gradazione w. offset;
* Emisfero*.

<b>Numero di input del modello</b> *Intero* (disponibile quando &quot;Pattern&quot; è impostato su &quot;Pattern Input&quot;)Seleziona l&#39;indice del pattern di input da diffondere.

<b>Distribuzione input pattern</b> *Intero* (disponibile quando &quot;Pattern&quot; è impostato su &quot;Pattern Input&quot;)Metodo utilizzato per selezionare i pattern di input da diffondere su una spline specifica:\
*- Casuale*: un pattern selezionato in modo casuale;\
*- Lungo la spline*: l&#39;indice del pattern aumenta gradualmente lungo la spline;\
*- Indice pattern*: esegue un ciclo sull&#39;indice dei pattern di input lungo ogni spline;\
*- Indice spline*: esegue il ciclo sull&#39;indice dei pattern di input da una spline all&#39;altra nell&#39;elenco delle spline di input.

<b>Variazione distribuzione</b> *Mobile* (disponibile quando &quot;Distribuzione input pattern&quot; è impostato su &quot;Lungo spline&quot;) Aumenta o diminuisce casualmente l&#39;indice selezionato dei pattern sulla spline.

<b>Sostituisci primo modello</b> *Booleano* Selezionare manualmente l&#39;indice del pattern da posizionare all&#39;inizio di ogni spline.

<b>Indice di input primo modello</b> *Intero* (disponibile quando l&#39;opzione &quot;Ignora primo pattern&quot; è impostata su &quot;True&quot;)Indice del pattern che deve essere posizionato all&#39;inizio di ogni spline.

<b>Sostituisci ultimo modello</b> *Booleano* Selezionare manualmente l&#39;indice del pattern da posizionare alla fine di ogni spline.

<b>Indice di input ultimo modello</b> *Intero* (disponibile quando l&#39;opzione &quot;Ignora ultimo pattern&quot; è impostata su &quot;True&quot;) Indica l&#39;indice del pattern che deve essere posizionato alla fine di ogni spline.

+++

+++Duplicati
<b>Modalità di distribuzione</b> *Numero intero* Metodo utilizzato per inserire i pattern duplicati:\
*- Lineare*: i duplicati sono distribuiti uniformemente lungo la normale della spline rispetto alla posizione originale del pattern;\
*- Circolare*: i duplicati sono disposti lungo un cerchio virtuale centrato sulla spline nella posizione originale del pattern.

<b>Quantità duplicata</b> *Numero intero* Numero di pattern duplicati.

<b>Scostamento</b> *Float2* (disponibile quando &quot;Modalità distribuzione&quot; è impostato su &quot;Lineare&quot;)Applica uno scostamento alle posizioni dei duplicati lungo la tangente (parallela) e la normale (perpendicolare) della spline.\
I duplicati sui lati opposti della spline vengono spostati in direzioni opposte.

<b>Centro offset</b> *Float2* (disponibile quando &quot;Modalità distribuzione&quot; è impostato su &quot;Lineare&quot;) Applica uno scostamento ai duplicati lungo la spline su X (parallelo) e Y (perpendicolare).

<b>Angolo di diffusione</b> *Mobile* (disponibile quando &quot;Modalità di distribuzione&quot; è impostata su &quot;Circolare&quot;)L&#39;arco del cerchio virtuale lungo il quale vengono distribuiti i duplicati, come l&#39;angolo dell&#39;arco in cui 1 rappresenta il cerchio completo.

<b>Distanza di offset</b> *Mobile* (disponibile quando &quot;Modalità di distribuzione&quot; è impostata su &quot;Circolare&quot;)Raggio del cerchio virtuale lungo il quale vengono distribuiti i duplicati.

<b>Rotazione</b> *Mobile* Ruota il cerchio virtuale lungo il quale vengono distribuiti i duplicati.

<b>Attenuazione inizio/fine offset</b> *Float2* Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine, quando si applicano offset ai duplicati.\
Ciò significa che gli scostamenti vengono diminuiti per i duplicati più vicini alle estremità di una spline.

<b>Offset attenuazione per Thickness</b> *Fluttuare* Fattori nel thickness della spline quando si applicano offset ai duplicati.\
Ciò significa che gli scostamenti vengono diminuiti per i duplicati su una porzione di una spline con un thickness inferiore.

+++

+++Dimensioni
<b>Modalità dimensioni</b> *Intero* Metodo di impostazione delle dimensioni dei pattern diffusi:\
*- Normale*: la dimensione viene controllata in modo uniforme utilizzando un parametro globale &quot;Scale&quot;;\
*- Usa Thickness dalla spline*: le dimensioni dipendono dal thickness della spline.

<b>Il Thickness ha effetto</b> *Intero* (disponibile quando l’opzione &quot;Modalità dimensioni&quot; è impostata su &quot;Usa Thickness da spline&quot;)Specifica l’asse della scala di un pattern che deve essere guidato dal thickness della spline:
* X &amp; Y: il Thickness viene moltiplicato per la dimensione sull’asse X e sull’asse Y;\
  <span id="_Hlk135741125"></span>- X: il Thickness viene moltiplicato per le dimensioni solo sull&#39;asse X;
* Y: il Thickness viene moltiplicato per le dimensioni solo sull’asse Y.\
  Se non viene moltiplicato, la scala originale del pattern corrisponde all’intera estensione dell’immagine.\
  Ciò significa che in modalità &quot;X&quot; le dimensioni sull’asse Y corrispondono all’intera estensione dell’immagine e devono essere regolate utilizzando il parametro Dimensione. Lo stesso vale per le dimensioni sull’asse X quando si utilizza la modalità &quot;Y&quot;.

<b>Dimensioni</b> *Float2* Dimensioni originali dei pattern in X e Y prima che altre regolazioni vengano eseguite da altri parametri.

<b>Dimensioni casuali</b> *Float2* Applica un moltiplicatore casuale fino al valore specificato per ridurre le dimensioni dei pattern in X e Y.

<b>Scala Thickness</b> *Mobile* (disponibile quando &quot;Modalità dimensioni&quot; è impostato su &quot;Usa Thickness da spline&quot;)Moltiplicatore aggiuntivo per la scala dei pattern quando guidato dal thickness della spline.

<b>Scala</b> *Mobile* (disponibile quando &quot;Modalità dimensioni&quot; è impostato su &quot;Normale&quot;)Un controllo globale per le dimensioni di tutti i pattern, dove 1 rappresenta l&#39;intera estensione dell&#39;immagine.\
Il ridimensionamento viene applicato relativamente al perno di un pattern. La posizione dei punti cardini può essere sfalsata mediante il parametro &quot;Shape Pivot&quot;.

<b>Scala casuale</b> *Mobile* Applica un moltiplicatore casuale fino al valore specificato per ridurre le dimensioni dei pattern.

<b>Moltiplicatore input mappa scala</b> *Mobile* Controlla l&#39;intensità dell&#39;input Mappa scala. Questa mappa funge da moltiplicatore per le dimensioni correnti dei pattern.\
L’effetto di questa mappa è combinato con gli altri parametri del gruppo &quot;Dimensioni&quot;.

<b>Modalità campionamento input scala</b> *Spazio texture* Il metodo di mappatura dei valori nella mappa scala sulle spline:\
*- Spazio texture*: i valori vengono applicati alle spline in cui si troverebbero se fossero inseriti in una texture utilizzando le coordinate UV della texture. In questo modo si applica effettivamente il valore alle spline &quot;in posizione&quot;;\
*- Orizzontale lungo la spline*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;\
*- Ora. lungo spline (rand. offset X)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coords spline), con uno scostamento orizzontale casuale nella mappa di scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);\
*- Ora. lungo spline (rand. offset Y)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline).

<b>Attenuazione inizio/fine</b> *Float2* Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine quando si ridimensionano i pattern.\
Ciò significa che la dimensione viene ridotta per i pattern più vicini alle estremità di una spline.

+++

+++Posizione
<b>Offset locale</b> *Float2* Applica uno scostamento alle posizioni dei pattern lungo la tangente (parallela) e la normale (perpendicolare) della spline.

<b>Scostamento locale casuale</b> *Float2* Applica uno scostamento casuale aggiuntivo alle posizioni dei pattern lungo la tangente (parallela) e la normale (perpendicolare) della spline.

<b>Centro casuale scostamento locale</b> *Float2* Sposta il centro dello scostamento casuale applicato dal parametro Scostamento casuale locale lungo la tangente (parallela) e la normale (perpendicolare) della spline.

<b>Attenuazione inizio/fine scostamento locale</b> *Float2* Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine quando si applicano offset di posizione ai pattern.\
Ciò significa che gli scostamenti vengono diminuiti per i pattern più vicini alle estremità di una spline.

<b>Attenuazione offset locale per Thickness</b> *Fluttuare* Fattori nel thickness della spline quando si applicano gli scostamenti ai pattern.\
Ciò significa che gli scostamenti vengono diminuiti per i duplicati su una porzione di una spline con un thickness inferiore.

<b>Scostamento sulla spline</b> *Mobile* Applica uno scostamento di posizione ai motivi lungo le spline.

<b>Scostamento casuale sulla spline</b> *Mobile* Applica uno scostamento di posizione aggiuntivo ai motivi lungo le spline.

+++

+++Rotazione
<b>Allinea con tangente</b> *Booleano* Ruota i pattern in modo che corrispondano alla direzione della spline nella loro posizione.

<b>Rotazione (pivot)</b> *Mobile* Ruota i pattern attorno ai loro perni.\
La posizione dei punti cardini può essere sfalsata mediante il parametro &quot;Shape Pivot&quot;.

<b>Rotazione casuale (pivot)</b> *Mobile* Applica una rotazione casuale aggiuntiva ai pattern attorno ai loro perni.\
La posizione dei punti cardini può essere sfalsata mediante il parametro &quot;Shape Pivot&quot;.

<b>Rotazione al centro casuale (pivot)</b> *Mobile* Ruota attorno ai perni del pattern al centro delle rotazioni casuali applicate dal parametro Rotazione casuale.

<b>Rotazione (al centro)</b> *Mobile* Ruota i pattern attorno al loro centro.

<b>Rotazione casuale (al centro)</b> *Mobile* Applica una rotazione casuale aggiuntiva ai pattern attorno al loro centro.

<b>Rotazione al centro casuale (al centro)</b> *Mobile* Ruota attorno al centro del pattern rispetto al centro delle rotazioni casuali applicate dal parametro Rotazione casuale.

+++

+++Colore
<b>Metodo fusione</b> *Intero* Metodo per fondere i colori dei pattern con lo sfondo e altri pattern sovrapposti:\
*- Max*: usa il colore più chiaro;\
*- Aggiungi*: aggiungi i colori.

<b>Colore base forma</b> *Mobile* Colore di base dei pattern.

<b>Moltiplicatore colore di base forma</b> *Mobile* L&#39;intensità del colore di base della forma dei pattern.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Moltiplicatore Thickness spline</b> *Fluttuazione* L&#39;intensità con cui il colore di ogni pattern viene moltiplicato rispetto al thickness della spline nella relativa posizione.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Moltiplicatore Indice Forma</b> *Fluttuazione* Intensità per la quale il colore di ogni pattern viene moltiplicato rispetto al relativo indice normalizzato.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Modalità Height emisfero</b> *Intero* (disponibile quando &quot;Pattern&quot; è impostato su &quot;Emisfero&quot;)L&#39;effetto del height della spline su un pattern di emisfero disseminato su di esso:\
*- Offset*: il height spline viene aggiunto al height dell&#39;emisfero;\
*- Scala*: il height spline viene moltiplicato per il height dell&#39;emisfero.

<b>Moltiplicatore Height spline</b> *Fluttuazione* L&#39;intensità con cui il colore di ogni pattern viene moltiplicato rispetto al height della spline nella relativa posizione.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Moltiplicatore scala forme</b> *Fluttuazione* L&#39;intensità con cui il colore di ogni pattern viene moltiplicato rispetto alla scala.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Luminanza casuale</b> *Mobile* Applica un moltiplicatore casuale fino al valore specificato per ridurre la luminanza dei pattern.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Moltiplicatore di input Height</b> *Mobile* Controlla l&#39;intensità dell&#39;input Mappa Height. Questa mappa funge da moltiplicatore per la luminanza corrente dei pattern.\
L’effetto di questa mappa è combinato con gli altri parametri del gruppo &quot;Colore&quot;.\
Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore.

<b>Modalità campionamento input mappa Height</b> *Intero* Metodo di mappatura dei valori nella mappa di Height alle spline:\
*- Spazio texture*: i valori vengono applicati alle spline in cui si troverebbero se fossero inseriti in una texture utilizzando le coordinate UV della texture. In questo modo si applica effettivamente il valore alle spline &quot;in posizione&quot;;\
*- Orizzontale lungo la spline*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;\
*- Ora. lungo spline (rand. offset X)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coords spline), con uno scostamento orizzontale casuale nella mappa di scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);\
*- Ora. lungo spline (rand. offset Y)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline).

<b>Maschera casuale</b> *Mobile* Regola l’intervallo della mascheratura casuale dei pattern, dove 0 significa che non viene mascherato alcun pattern e 1 significa che lo sono tutti i pattern.

<b>Soglia mappa maschera</b> *Mobile* I valori nella mappa maschera al di sotto di questo valore di soglia vengono elaborati come nero, mentre i valori al di sopra della soglia vengono elaborati come bianchi.\
Questo significa che tutti i pattern nelle aree della Mappa maschera sotto questo valore verranno mascherati.

<b>Modalità campionamento input mappa maschera</b> *Intero* Metodo di mappatura dei valori nella mappa maschera sulle spline:\
*- Spazio texture*: i valori vengono applicati alle spline in cui si troverebbero se fossero inseriti in una texture utilizzando le coordinate UV della texture. In questo modo si applica effettivamente il valore alle spline &quot;in posizione&quot;;\
*- Orizzontale lungo la spline*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;\
*- Ora. lungo spline (rand. offset X)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coords spline), con uno scostamento orizzontale casuale nella mappa di scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);\
*- Ora. lungo spline (rand. offset Y)*: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero, ogni riga nelle coordinate spline).

<b>Inverti mappa maschera</b> *Booleano* Inverte i valori della mappa maschera con un&#39;operazione di tipo &quot;Uno meno&quot; (1 - x).

<b>Inversione maschera</b> *Booleano* Inverte la mascheratura dei pattern.

+++

<b>Correzione non quadrata</b> *Booleano* Regolate le posizioni dei punti per mantenere la forma della spline con risoluzioni non quadrate.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGreyscale-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant1-After.jpg" alt="ScatterOnSplineGreyscale-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGreyscale-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/ScatterOnSplineGrayscale-Variant2-After.jpg" alt="ScatterOnSplineGreyscale-Variant2-After">
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

![Esempio di nodo 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo.gif "Esempio di nodo 2")

</td>
<td style="border: 0;" valign="top">

![Demo nodo 2](../../../../../../assets/ScatterOnSplineGrayscale-Demo2.gif "Demo nodo 2")

</td>
</tr>
</table>
