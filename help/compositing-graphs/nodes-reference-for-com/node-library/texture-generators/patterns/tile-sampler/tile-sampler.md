---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Usate il nodo Tile Sampler per campionare e disporre le porzioni dalle texture di input per creare pattern affiancati in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Affianca Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# Affianca Sampler

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-sampler.resources/tile-sampler.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Affianca Sampler è il nodo più avanzato per la generazione di pattern di riquadri. È una versione evoluta e più complessa di [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partire da 2017 2.1, le differenze sono molto più piccole tra Tile Sampler e [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Le differenze principali si riscontrano ora solo nei sette slot di mappa disponibili per le funzioni Scala, Posizione, Rotazione, Dimensione, Colore e Mascheratura. Il loro effetto può essere fuso in separatamente.

Tile Sampler è utile per la creazione di pattern di procedurali artificiali, con un controllo aggiuntivo su determinati parametri guidati da mappe di input esterne.

Assicurati di conoscere [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) prima di passare al Tile Sampler. Nella maggior parte dei casi, troverai [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) sufficiente e non avrai bisogno della complessità aggiuntiva di Tile Sampler.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input pattern 1-6</b> <i>Input scala di grigi / Input colore</i> | Immagine pattern personalizzata, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Input immagine&quot;.<br><br>La quantità di input disponibili è determinata dal parametro <b>Numero input pattern</b>. |
| <b>Input mappa scala</b> <i>Input scala di grigi</i> | Mappa in scala di grigi per applicare la scala ai riquadri. |
| <b>Input mappa Spostamento</b> <i>Input scala di grigi</i> | Mappa in scala di grigi per gestire lo spostamento dei riquadri. |
| <b>Input Mappa di rotazione</b> <i>Input scala di grigi</i> | Mappa in scala di grigi per guidare la rotazione delle porzioni. |
| <b>Input mappa vettoriale</b> <i>Input colore</i> | Mappa vettoriale colori per applicare il ridimensionamento non uniforme. |
| <b>Input mappa colori</b> <i>Input scala di grigi / Input colore</i> | Mapping per la colorazione per porzione. |
| <b>Input mappa maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per nascondere determinate porzioni. |
| <b>Input mappa distribuzione pattern</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per gestire più input di pattern personalizzati. |
| <b>Input in background</b> <i>Input scala di grigi / Input colore</i> | Immagine di sfondo facoltativa. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>X importo</b> <i>0 - 64</i> | Quantità di ripetizioni X del pattern. |
| <b>Importo Y</b> <i>0 - 64</i> | Quantità di ripetizioni Y del pattern. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di squash e allungamento con rapporti non quadrati. |
| <b>Pattern</b> |  |
| <b>Pattern</b> <i>Input pattern, Quadrato, Disco, Paraboloide, Campana, Gaussiano, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana ridotta, Mezzaluna, Capsula, Cono</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Numero di input del modello</b> <i>1 - 6</i> | Quantità di pattern personalizzati tra cui scegliere in modo casuale. |
| <b>Distribuzione input pattern</b> <i>Casuale, Numero Motivo, Mappa Di Distribuzione</i> | Consente di impostare la modalità di selezione di più input pattern. Casuale significa che è stato scelto un numero casuale. Numero pattern significa che sono semplicemente inseriti in una sequenza a ciclo continuo. La mappa di distribuzione utilizza un input mappa in scala di grigio per il posizionamento dell&#39;unità. |
| <b>Filtro input pattern (motore > v4)</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> |  |
| <b>Specifico per pattern</b> <i>0.0 - 1.0</i> | Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato. |
| <b>Casuale specifico per pattern</b> <i>0.0 - 1.0</i> | L’effetto di randomizzazione dipende dal pattern selezionato. |
| <b>Rotazione</b> <i>0, 90, 180, 270</i> | Rotazione graduale (90 gradi). |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Rotazione libera casuale su base per porzione. |
| <b>Simmetria casuale</b> <i>0.0 - 1.0</i> | Imposta il numero di porzioni che devono essere capovolte/riflesse casualmente in base al comportamento riportato di seguito. |
| <b>Simmetria modalità casuale</b> <i>Orizzontale + Verticale, Orizzontale, Verticale</i> | Determina il comportamento di mirroring della simmetria. |
| <b>Dimensioni</b> |  |
| <b>Modalità dimensioni</b> <i>Normale, Mantieni proporzioni, Assoluto, Pixel</i> | Imposta il comportamento generale della dimensione del pattern.<br><br>Normale consente di definire la dimensione degli elementi del pattern. È influenzata dall&#39;entità X e Y.<br><br>Mantieni proporzioni consente di impostare una dimensione influenzata dalla quantità X e Y, ma le proporzioni X e Y tra i due elementi rimangono invariate.<br><br>Assoluto consente di impostare una dimensione assoluta non influenzata dalla quantità X e Y.<br><br>Pixel consente di impostare una dimensione assoluta in pixel, non influenzata dalla quantità X e Y. La modifica della risoluzione influirà sulle dimensioni degli elementi. |
| <b>Dimensioni (Assoluto/Pixel)</b> <i>0.0 - 1.0</i> | Modifica le proporzioni non uniformi delle porzioni. Il comportamento esatto dipende dalla modalità Dimensione. |
| <b>Dimensioni casuali</b> <i>0.0 - 1.0</i> | Rende casuali le proporzioni per porzione. |
| <b>Scala</b> <i>0.0 - 10.0</i> | Imposta la scala globale dei riquadri. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Rende casuale la scala per porzione. |
| <b>Moltiplicatore mappa scala</b> <i>0.0 - 1.0</i> | Fusioni nell&#39;effetto della mappa scala. |
| <b>Moltiplicatore mappa vettoriale scala</b> <i>0.0 - 1.0</i> | Fusione l&#39;effetto della mappa vettoriale di scala per determinare il ridimensionamento non uniforme. |
| <b>Effetto sulla parametrizzazione della scala</b> <i>X e Y, X, Y</i> | Imposta gli assi interessati dalla parametrizzazione della scala. Può essere utilizzato per fare in modo che la mappa scala influisca solo su X o Y di elementi. |
| <b>Posizione</b> |  |
| <b>Posizione casuale</b> <i>0.0 - 10.0</i> | Rende casuale la posizione delle porzioni su entrambi gli assi. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta le porzioni in base al tipo di scostamento. |
| <b>Tipo offset</b> <i>quincux orizzontale, quincux verticale, globale orizzontale, globale verticale</i> | Cambia la direzione in cui opera l&#39;offset. |
| <b>Scostamento globale</b> <i>0.0 - 1.0</i> | Scostamento globale di tutte le porzioni sull&#39;asse X o Y. |
| <b>Intensità mappa Spostamento</b> <i>0.0 - 1.0</i> | Fusione l&#39;intensità della mappa di Spostamento sullo scostamento. |
| <b>Angolo di Spostamento</b> <i>0.0 - 1.0</i> | Consente di impostare l’angolo di spostamento. |
| <b>Spostamento mappa vettoriale</b> <i>0.0 - 1.0</i> | Usa la mappa vettoriale per determinare spostamento e angolo. |
| <b>Rotazione</b> |  |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota tutte le porzioni. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Ruota in modo casuale per porzione. |
| <b>Moltiplicatore Mappa di rotazione</b> <i>0.0 - 1.0</i> | Fusioni dell&#39;effetto della Mappa di rotazione sulla rotazione per porzione. |
| <b>Moltiplicatore mappa vettoriale</b> <i>0.0 - 1.0</i> | Utilizza la mappa vettoriale per guidare la rotazione per porzione. |
| <b>Colore</b> |  |
| <b>Soglia mappa maschera</b> <i>0.0 - 1.0</i> | Soglia per la mappa maschera quando iniziare a nascondere le porzioni. |
| <b>Inversione mappa maschera</b> <i>Falso/Vero</i> | Inverte l’effetto mappa maschera. |
| <b>Tecnica Di Campionamento Della Mappa Maschera</b> <i>Centro pattern, rettangolo di selezione pattern (più lento)</i> | Indica se nascondere deve essere determinato da un singolo punto o da un rettangolo di selezione. Evita che i pixel isolati causino effetti strani. |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | La mascheratura casuale funziona parallelamente alla mappa della maschera. |
| <b>Inverti maschera</b> <i>Falso/Vero</i> | Inverte la maschera casuale. |
| <b>Metodo fusione</b> <i>Aggiungi/Sotto, Max (Tile Sampler) / Aggiungi/Sotto, Fusione Alpha (Tile Sampler Color)</i> | Modalità Fusione per le porzioni sullo sfondo e viceversa. |
| <b>Colore</b> <i>(valore scala di grigi) / (valore colore)</i> | Tinta piastrella solida, globale. |
| <b>Colore/Luminanza casuale</b> <i>0.0 - 1.0</i> | Randomizzazione del colore, per porzione. |
| <b>Modalità Parametrizzazione Colore</b> <i>Input colore, Scala, Indice linea, Indice riga, Indice pattern (Tile Sampler) / Mappa colori, Scala, Indice linea, Indice riga, Indice pattern, Posizione centro pattern, Posizione centro pattern (RG) Dimensione sfera (B) (Colore Sampler Tile)</i> | Consente di impostare l’esatto livello di casualità del colore da parametrizzare. |
| <b>Moltiplicatore di parametrizzazione colore</b> <i>0.0 - 1.0</i> | Fusioni nell&#39;effetto di parametrizzazione sopra riportato. |
| <b>Effetto della parametrizzazione del colore (solo colore)</b> <i>RGB+Alpha, solo RGB, solo Alpha</i> | Imposta l’effetto della parametrizzazione sul colore. |
| <b>Opacità globale (solo scala di grigi)</b> <i>0.0 - 1.0</i> | Imposta l’opacità globale della porzione. |
| <b>Colore di sfondo</b> <i>(valore scala di grigi) / (valore colore)</i> | Imposta il colore di sfondo in tinta unita. |
| <b>Ordine di rendering inverso</b> <i>Falso/Vero</i> | Inverte l’ordine di rendering per passare dal primo all’ultimo. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-sampler.resources/tilesampler-ex2.png" /><br><i>Nell'esempio viene illustrato come i parametri sono guidati dalle mappe di input (Distribuzione pattern, Scala, Rotazione).</i>
        </td>
    </tr>
</table>
