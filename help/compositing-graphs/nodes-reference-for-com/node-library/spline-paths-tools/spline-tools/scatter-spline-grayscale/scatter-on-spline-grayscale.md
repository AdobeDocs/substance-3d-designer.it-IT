---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '2853'
ht-degree: 0%

---


# Dispersione su scala di grigi spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-01.png "Icona nodo")

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

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Sfondo</b> <i>Scala di grigi</i> (primaria) | Immagine in scala di grigio su cui devono essere disegnate spline. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |
| <b>Input pattern n. </b> <i>Scala di grigi</i> | Motivi che devono essere distribuiti lungo le spline. |
| <b>Mappa scala</b> <i>Scala di grigi</i> | La mappa che controlla la scala dei pattern sparsi. L&#39;effetto di questa mappa è controllato dal parametro &#39;Scale Map Input Multiplier&#39; ed è combinato con gli altri parametri nel gruppo &#39;Size&#39;. |
| <b>Mappa Height</b> <i>Scala di grigi</i> | La mappa che controlla il height dei pattern sparsi. L&#39;effetto di questa mappa è controllato dal parametro &#39;Moltiplicatore input Height&#39; ed è combinato con gli altri parametri &#39;Colore&#39; nel gruppo &#39;Colore&#39;. |
| <b>Mappa maschera</b> <i>Scala di grigi</i> | La mappa che controlla la mascheratura dei pattern sparsi. L&#39;effetto di questa mappa è controllato dal parametro &quot;Soglia mappa maschera&quot; ed è combinato con gli altri parametri &quot;Maschera&quot; nel gruppo &quot;Colore&quot;. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine che rappresenta i pattern distribuiti lungo la spline di input sullo sfondo dell&#39;input. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Input spline</b> <i>Numero intero</i> | Metodo di selezione delle spline da utilizzare per i motivi di dispersione:<br><br>- <i>Tutte le spline</i>: utilizzare tutte le spline nell&#39;elenco di input;<br>- <i>Spline singola</i>: utilizzare solo la spline specificata dall&#39;elenco di input;<br>- <i>Intervallo spline</i>: utilizzare solo le spline dell&#39;intervallo specificato dall&#39;elenco di input. |
| <b>Indice spline</b> <i>Intero</i> (disponibile quando &#39;Input spline&#39; è impostato su &#39;Single Spline&#39;) | Indice di elenco della spline da utilizzare per i pattern di dispersione. |
| <b>Intervallo spline</b> <i>Intero2</i> (disponibile quando &#39;Input spline&#39; è impostato su &#39;Intervallo spline&#39;) | Intervallo di indici di elenco, incluse le spline, che devono essere utilizzate per i pattern di dispersione. |
| <b>Modalità Dispersione</b> <i>Numero intero</i> | Metodo di dispersione dei pattern lungo le spline, che influisce sulla quantità di pattern su ogni spline: <br><br>- Quantità forma: la quantità specificata di pattern uniformemente distanziati è dispersa;<br>- Spaziatura forma: il numero di pattern viene regolato automaticamente per adattarsi alla spaziatura uniforme specificata.<br><br>In entrambi i casi, il primo e l&#39;ultimo motivo si trovano esattamente all&#39;inizio e alla fine di ogni spline. |
| <b>Quantità forma</b> <i>Numero intero</i> (disponibile quando &#39;Modalità Dispersione&#39; è impostato su &#39;Quantità forma&#39;) | Quantità di pattern uniformemente distribuiti lungo ciascuna spline. |
| <b>Distribuzione della forma lungo la spline</b> <i>Numero intero</i> (disponibile quando &#39;Modalità Dispersione&#39; è impostato su &#39;Quantità forma&#39;) | Metodo di distribuzione dei pattern lungo una spline:<br><br>- <i>Dall&#39;origine</i>: la spaziatura dei pattern è influenzata dalle tangenti del punto della spline, in cui le forme sono più distanti vicino a punti con tangenti lunghe;<br>- <i>Uniforme</i>: i pattern sono distribuiti uniformemente lungo la spline indipendentemente dalle tangenti e dalla traiettoria. |
| <b>Spaziatura tra forme</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità Dispersione&#39; è impostato su &#39;Spaziatura forme&#39;) | Distanza minima lungo una spline in base alla quale i pattern devono essere distanziati, mentre il primo e l&#39;ultimo pattern devono ancora atterrare rispettivamente all&#39;inizio e alla fine di ogni spline. |
| <b>Inizio</b> <i>Mobile</i> | <span id="_Hlk135680521"></span>Sposta il punto dall&#39;inizio di una spline nel punto in cui inizia la dispersione. Il valore è la lunghezza normalizzata di ogni spline. |
| <b>Fine</b> <i>Mobile</i> | Sposta il punto dall&#39;inizio di una spline nel punto in cui termina la dispersione. Il valore è la lunghezza normalizzata di ogni spline. |
| <b>Pivot forma</b> <i>Float2</i> | Sposta il perno della serie X e Y nello spazio tangente della spline.<br>Considerando che il perno è ciò che viene posizionato sulla spline, questo sposta efficacemente i pattern lungo o perpendicolarmente alla spline.<br>Nota: le posizioni dei perni influiscono sull&#39;effetto dei parametri &#39;Scala&#39; e &#39;Rotazione (pivot)&#39;. |
| <b>Pattern</b> |  |
| <b>Pattern</b> <i>Numero intero</i> | Motivo che deve essere sparso lungo le spline:<br><br>- <i>Input motivo</i>: utilizzare i motivi forniti agli input &#39;N. di input motivo&#39;;<br>- Quadrato;<br>- Disco;<br>- Paraboloide;<br>- Campana;<br>- Gaussiano;<br>- Spina;<br>- Piramide;<br>- Mattone;<br>- Gradazione;<br>- Onde;<br>- Mezza campana;<br>- Campana dorata;<br>- Crescente;<br>- Capsula;<br>- Cono;<br>- Gradazione w. offset;<br>- Emisfero. |
| <b>Numero di input del modello</b> <i>Intero</i> (disponibile quando &#39;Pattern&#39; è impostato su &#39;Input pattern&#39;) | Seleziona l&#39;indice del pattern di input che deve essere distribuito. |
| <b>Distribuzione input pattern</b> <i>Intero</i> (disponibile quando &#39;Pattern&#39; è impostato su &#39;Input pattern&#39;) | Metodo utilizzato per selezionare i pattern di input da diffondere su una spline specifica:<br><br>- <i>Casuale</i>: un pattern viene selezionato in modo casuale;<br>- <i>Lungo la spline</i>: l&#39;indice del pattern aumenta gradualmente lungo la spline;<br>- <i>Indice del pattern</i>: esegue un ciclo sull&#39;indice dei pattern di input lungo ogni spline;<br>- <i>Indice spline</i>: esegue un ciclo sull&#39;indice dei pattern di input da una spline al successivo nell&#39;elenco delle spline di input. |
| <b>Variazione distribuzione</b> <i>Virgola mobile</i> (disponibile quando &#39;Distribuzione input pattern&#39; è impostato su &#39;Lungo spline&#39;) | Aumenta o diminuisce in modo casuale l&#39;indice selezionato dei pattern sulla spline. |
| <b>Sostituisci primo modello</b> <i>Booleano</i> | Selezionate manualmente l&#39;indice del pattern da posizionare all&#39;inizio di ogni spline. |
| <b>Indice di input primo modello</b> <i>Numero intero</i> (disponibile quando &#39;Sostituisci primo criterio&#39; è impostato su &#39;True&#39;) | Indice del pattern da posizionare all&#39;inizio di ogni spline. |
| <b>Sostituisci ultimo modello</b> <i>Booleano</i> | Selezionate manualmente l&#39;indice del pattern da posizionare alla fine di ogni spline. |
| <b>Indice di input ultimo modello</b> <i>Numero intero</i> (disponibile quando &#39;Ignora ultimo modello&#39; è impostato su &#39;True&#39;) | Indice del pattern da posizionare alla fine di ogni spline. |
| <b>Duplicati</b> |  |
| <b>Modalità di distribuzione</b> <i>Numero intero</i> | Metodo utilizzato per posizionare i pattern duplicati:<br><br>- <i>Lineare</i>: i duplicati sono equidistanti lungo la normale della spline dalla posizione originale del pattern;<br>- <i>Circolare</i>: i duplicati sono disposti lungo un cerchio virtuale centrato sulla spline nella posizione originale del pattern. |
| <b>Quantità duplicata</b> <i>Numero intero</i> | Numero di pattern duplicati. |
| <b>Scostamento</b> <i>Virgola mobile 2</i> (disponibile quando &#39;Modalità distribuzione&#39; è impostato su &#39;Lineare&#39;) | Applica uno scostamento alle posizioni dei duplicati lungo la tangente (parallela) e la normale (perpendicolare) della spline.<br>I duplicati sui lati opposti della spline vengono spostati in direzioni opposte. |
| <b>Centro offset</b> <i>Virgola mobile 2</i> (disponibile quando &#39;Modalità distribuzione&#39; è impostato su &#39;Lineare&#39;) | Applica uno scostamento ai duplicati lungo la spline su X (parallelo) e Y (perpendicolare). |
| <b>Angolo di diffusione</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità distribuzione&#39; è impostato su &#39;Circolare&#39;) | L&#39;arco del cerchio virtuale lungo il quale vengono distribuiti i duplicati, come l&#39;angolo dell&#39;arco in cui 1 è il cerchio completo. |
| <b>Distanza di offset</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità distribuzione&#39; è impostato su &#39;Circolare&#39;) | Raggio del cerchio virtuale lungo il quale vengono distribuiti i duplicati. |
| <b>Rotazione</b> <i>Mobile</i> | Ruota il cerchio virtuale lungo il quale vengono distribuiti i duplicati. |
| <b>Attenuazione inizio/fine offset</b> <i>Float2</i> | Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine, quando si applicano offset ai duplicati.<br>Ciò significa che gli scostamenti vengono ridotti per i duplicati più vicini alle estremità di una spline. |
| <b>Offset attenuazione per Thickness</b> <i>Mobile</i> | Fattori nel thickness della spline quando si applicano gli offset ai duplicati.<br>Ciò significa che gli scostamenti vengono ridotti per i duplicati su una porzione di una spline con un thickness inferiore. |
| <b>Dimensioni</b> |  |
| <b>Modalità dimensioni</b> <i>Numero intero</i> | Il metodo di impostazione della dimensione dei pattern sparsi:<br><br>- <i>Normale</i>: la dimensione viene controllata in modo uniforme utilizzando un parametro &#39;Scala&#39; globale;<br>- <i>Usa Thickness da spline</i>: la dimensione dipende dal thickness della spline. |
| <b>Il Thickness ha effetto</b> <i>Intero</i> (disponibile quando &#39;Modalità dimensioni&#39; è impostato su &#39;Usa Thickness da spline&#39;) | Specifica quale asse della scala di un pattern deve essere guidato dal thickness della spline:<br><br>- X &amp; Y: il Thickness viene moltiplicato per la dimensione in entrambi gli assi X e Y;<br>- <span id="_Hlk135741125"></span>X: il Thickness viene moltiplicato per la dimensione solo sull&#39;asse X;<br>- Y: il Thickness viene moltiplicato per la dimensione solo sull&#39;asse Y.<br><br>Se non viene moltiplicato, la scala originale del pattern corrisponde all&#39;intera estensione dell&#39;immagine.<br>In questo modo, in modalità &#39;X&#39;, la dimensione sull&#39;asse Y corrisponde all&#39;intera estensione dell&#39;immagine e deve essere modificata utilizzando il parametro Size. Lo stesso vale per le dimensioni sull’asse X quando si utilizza la modalità &quot;Y&quot;. |
| <b>Dimensioni</b> <i>Float2</i> | Dimensioni originali dei pattern in X e Y prima che vengano apportate altre regolazioni in base ad altri parametri. |
| <b>Dimensioni casuali</b> <i>Float2</i> | Applica un moltiplicatore casuale fino al valore specificato per ridurre le dimensioni dei pattern in X e Y. |
| <b>Scala Thickness</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità dimensioni&#39; è impostato su &#39;Usa Thickness da spline&#39;) | Un ulteriore moltiplicatore per la scala dei pattern quando vengono guidati dal thickness della spline. |
| <b>Scala</b> <i>Virgola mobile</i> (disponibile quando &#39;Modalità dimensioni&#39; è impostato su &#39;Normale&#39;) | Un controllo globale per le dimensioni di tutti i pattern, dove 1 rappresenta l’intera estensione dell’immagine.<br>Il ridimensionamento viene applicato relativamente al perno di un pattern. La posizione dei punti cardini può essere spostata mediante il parametro &#39;Shape Pivot&#39;. |
| <b>Scala casuale</b> <i>Mobile</i> | Applica un moltiplicatore casuale fino al valore specificato per ridurre le dimensioni dei pattern. |
| <b>Moltiplicatore input mappa scala</b> <i>Mobile</i> | Controlla l’intensità dell’input Mappa scala. Questa mappa funge da moltiplicatore per le dimensioni correnti dei pattern.<br>L&#39;effetto di questa mappa è combinato con gli altri parametri nel gruppo &#39;Dimensioni&#39;. |
| <b>Modalità campionamento input scala</b> <i>Spazio Texture</i> | Metodo di mappatura dei valori nella mappa scala alle spline:<br><br>- <i>spazio Texture</i>: i valori vengono applicati alle spline in cui si troverebbero se inseriti in una texture utilizzando le coordinate UV della texture. In questo modo il valore viene applicato alle spline &#39;in posizione&#39;;<br>- <i>Orizzontale lungo la spline</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;<br>- <i>Ora. lungo spline (rand. offset X)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento orizzontale casuale nella mappa Scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);<br>- <i>Hor. lungo spline (rand. offset Y)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero ogni riga nelle coordinate spline). |
| <b>Attenuazione inizio/fine</b> <i>Float2</i> | Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine durante il ridimensionamento dei pattern.<br>Ciò significa che le dimensioni vengono ridotte per i motivi più vicini alle estremità di una spline. |
| <b>Posizione</b> |  |
| <b>Offset locale</b> <i>Float2</i> | Applica uno scostamento alle posizioni delle serie lungo la tangente (parallela) e la normale (perpendicolare) della spline. |
| <b>Scostamento locale casuale</b> <i>Float2</i> | Applica un ulteriore scostamento casuale alle posizioni delle serie lungo la tangente (parallela) e la normale (perpendicolare) della spline. |
| <b>Centro casuale scostamento locale</b> <i>Float2</i> | Sposta il centro dello scostamento casuale applicato dal parametro Scostamento casuale locale (Local Offset Random) lungo la tangente (parallela) e la normale (perpendicolare) della spline. |
| <b>Attenuazione inizio/fine scostamento locale</b> <i>Float2</i> | Fattori nella distanza dal punto medio della spline al suo inizio e alla sua fine quando si applicano scostamenti di posizione ai pattern.<br>Ciò significa che gli scostamenti vengono diminuiti per i pattern più vicini alle estremità di una spline. |
| <b>Attenuazione offset locale per Thickness</b> <i>Mobile</i> | Fattori nel thickness della spline quando si applica uno scostamento ai pattern.<br>Ciò significa che gli scostamenti vengono ridotti per i duplicati su una porzione di una spline con un thickness inferiore. |
| <b>Scostamento sulla spline</b> <i>Mobile</i> | Applica uno scostamento di posizione ai pattern lungo le spline. |
| <b>Scostamento casuale sulla spline</b> <i>Mobile</i> | Applica uno scostamento di posizione aggiuntivo ai pattern lungo le spline. |
| <b>Rotazione</b> |  |
| <b>Allinea con tangente</b> <i>Booleano</i> | Ruota i pattern in modo che corrispondano alla direzione della spline nella loro posizione. |
| <b>Rotazione (pivot)</b> <i>Mobile</i> | Ruota i pattern attorno ai loro perni.<br>È possibile spostare la posizione dei punti cardini utilizzando il parametro &#39;Shape Pivot&#39;. |
| <b>Rotazione casuale (pivot)</b> <i>Mobile</i> | Applica una rotazione casuale aggiuntiva ai pattern attorno ai loro perni.<br>È possibile spostare la posizione dei punti cardini utilizzando il parametro &#39;Shape Pivot&#39;. |
| <b>Rotazione al centro casuale (pivot)</b> <i>Mobile</i> | Ruota attorno ai perni del pattern al centro delle rotazioni casuali applicate dal parametro Rotazione casuale. |
| <b>Rotazione (al centro)</b> <i>Mobile</i> | Ruota i pattern attorno al loro centro. |
| <b>Rotazione casuale (al centro)</b> <i>Mobile</i> | Applica una rotazione casuale aggiuntiva ai pattern attorno al loro centro. |
| <b>Rotazione al centro casuale (al centro)</b> <i>Mobile</i> | Ruota attorno al centro del pattern al centro delle rotazioni casuali applicate dal parametro Rotazione casuale. |
| <b>Colore</b> |  |
| <b>Metodo fusione</b> <i>Numero intero</i> | Metodo di fusione dei colori dei pattern con lo sfondo e altri pattern sovrapposti:<br><br>- <i>Max</i>: usate il colore più chiaro;<br>- <i>Aggiungi</i>: aggiungete i colori. |
| <b>Colore base forma</b> <i>Mobile</i> | Colore di base dei pattern. |
| <b>Moltiplicatore colore di base forma</b> <i>Mobile</i> | Intensità del Colore di base di forme dei pattern.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Moltiplicatore Thickness spline</b> <i>Mobile</i> | Intensità di moltiplicazione del colore di ogni motivo rispetto al thickness della spline nella relativa posizione.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Moltiplicatore Indice Forma</b> <i>Mobile</i> | Intensità di moltiplicazione del colore di ogni pattern rispetto al relativo indice normalizzato.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Modalità Height emisfero</b> <i>Intero</i> (disponibile quando &#39;Pattern&#39; è impostato su &#39;Emisfero&#39;) | Effetto del height della spline su un pattern emisfero diffuso su di essa:<br><br>- <i>Scostamento</i>: il height della spline viene aggiunto al height dell&#39;emisfero;<br>- <i>Scala</i>: il height della spline viene moltiplicato per il height dell&#39;emisfero. |
| <b>Moltiplicatore Height spline</b> <i>Mobile</i> | Intensità di moltiplicazione del colore di ogni motivo rispetto al height della spline nella relativa posizione.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Moltiplicatore scala forme</b> <i>Mobile</i> | Intensità per la quale il colore di ogni pattern viene moltiplicato rispetto alla scala.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Luminanza casuale</b> <i>Mobile</i> | Applica un moltiplicatore casuale fino al valore specificato per diminuire la luminanza dei pattern.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Moltiplicatore di input Height</b> <i>Mobile</i> | Controlla l’intensità dell’input Mappa altezza. Questa mappa funge da moltiplicatore per la luminanza corrente dei pattern.<br>L&#39;effetto di questa mappa è combinato con gli altri parametri nel gruppo &#39;Colore&#39;.<br>Nota: il colore di output è il risultato ponderato di tutti i moltiplicatori di colore. |
| <b>Modalità campionamento input mappa Height</b> <i>Numero intero</i> | Metodo di mappatura dei valori nella mappa altezza alle spline:<br><br>- <i>spazio Texture</i>: i valori vengono applicati alle spline in cui si troverebbero se inseriti in una texture utilizzando le coordinate UV della texture. In questo modo il valore viene applicato alle spline &#39;in posizione&#39;;<br>- <i>Orizzontale lungo la spline</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;<br>- <i>Ora. lungo spline (rand. offset X)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento orizzontale casuale nella mappa Scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);<br>- <i>Hor. lungo spline (rand. offset Y)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero ogni riga nelle coordinate spline). |
| <b>Maschera casuale</b> <i>Mobile</i> | Regola l’intervallo della mascheratura casuale dei pattern, dove 0 significa che non viene mascherato alcun pattern e 1 significa che sono tutti i pattern. |
| <b>Soglia mappa maschera</b> <i>Mobile</i> | I valori della Mappa maschera al di sotto di questo valore di soglia vengono elaborati come nero, mentre i valori al di sopra della soglia vengono elaborati come bianco.<br>Ciò significa che tutti i pattern nelle aree della Mappa maschera al di sotto di questo valore verranno mascherati. |
| <b>Modalità campionamento input mappa maschera</b> <i>Numero intero</i> | Metodo di mappatura dei valori nella mappa maschera alle spline:<br><br>- <i>spazio Texture</i>: i valori vengono applicati alle spline in cui si troverebbero se fossero posizionati in una texture utilizzando le coordinate UV della texture. In questo modo il valore viene applicato alle spline &#39;in posizione&#39;;<br>- <i>Orizzontale lungo la spline</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), in cui ogni riga viene applicata a una spline diversa dall&#39;alto verso il basso;<br>- <i>Ora. lungo spline (rand. offset X)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento orizzontale casuale nella mappa Scala per ogni spline (ad esempio, ogni riga nelle coordinate spline);<br>- <i>Hor. lungo spline (rand. offset Y)</i>: i valori vengono applicati direttamente alle coordinate delle spline codificate (vedere l&#39;input Coord spline), con uno scostamento verticale casuale nella mappa Scala per ogni spline (ovvero ogni riga nelle coordinate spline). |
| <b>Inverti mappa maschera</b> <i>Booleano</i> | Inverte i valori della Mappa maschera con un’operazione &quot;Uno meno&quot; (1 - x). |
| <b>Inversione maschera</b> <i>Booleano</i> | Inverte la mascheratura dei pattern. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni dei punti per mantenere la forma della spline con risoluzioni non quadrate. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-02.jpg" alt="ScatterOnSplineGreyscale-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-03.jpg" alt="ScatterOnSplineGreyscale-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-04.jpg" alt="ScatterOnSplineGreyscale-Variant2-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-05.jpg" alt="ScatterOnSplineGreyscale-Variant2-After">
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

![Esempio di nodo 2](scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-06.gif "Esempio di nodo 2")

</td>
<td style="border: 0;" valign="top">

![Demo nodo 2](scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-07.gif "Demo nodo 2")

</td>
</tr>
</table>
