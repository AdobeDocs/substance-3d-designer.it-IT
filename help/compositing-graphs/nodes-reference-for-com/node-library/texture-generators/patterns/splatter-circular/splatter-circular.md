---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Usa il nodo Circolare di splatter per dispersione forme circolari tra texture per creare pattern organici e casuali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Circolare a dispersione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 8%

---


# Circolare a dispersione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter-circular.resources/splatter-circular.png){width="128px"}

![](splatter-circular.resources/splatter-circular-color.png){width="128px"}

<b>Ingresso:</b> Generatori texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Splatter Circular genera un pattern ad anello con vari controlli. Può utilizzare forme predefinite o input personalizzati. È simile a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), ma con un posizionamento circolare invece di una griglia.

Questo risulta utile quando si desidera posizionare le forme in modo circolare con varie opzioni di randomizzazione.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

Entrambi gli ingressi sono opzionali.

|  |  |
|:---|:---|
| <b>Input immagine pattern 1-6</b> <i>Input scala di grigi (input colore)</i> | Solo circolare splatter: immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Input immagine&quot;. |
| <b>Sfondo</b> <i>Input scala di grigi (input colore)</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Quantità motivo</b> <i>1 - 64</i> | Quantità di porzioni di pattern da posizionare su un anello. |
| <b>Quantità motivo casuale</b> <i>0.0 - 1.0</i> | Randomizzazione della quantità di pattern da posizionare. Consigliato per un valore Anello maggiore di 1. |
| <b>Quantità motivo casuale min</b> <i>1 - 10</i> | Imposta la quantità minima di pattern per la randomizzazione. |
| <b>Quantità squillo</b> <i>1 - 10</i> | Imposta il numero di anelli da riempire. Gli anelli sono sempre posizionati all&#39;interno di quello esterno, e lo spazio uniformemente. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |
| <b>Pattern</b> |  |
| <b>Pattern</b> <i>Input immagine, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Mezzaluna, Capsula, Cono</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Numero di input del modello</b> <i>1 - 6</i> | Consente di impostare il numero di diversi input dell’immagine da utilizzare. Disponibile solo quando <i>Input immagine</i> è selezionato in precedenza. |
| <b>Distribuzione input pattern</b> <i>Casuale, Per Numero Di Serie, Per Numero Di Serie</i> | Consente di impostare la modalità di selezione di più input pattern. Casuale significa che ne è stato scelto uno casuale, Numero pattern significa che sono semplicemente inseriti in una sequenza ciclica, Con numeri di anello significa che ogni anello ha un altro in sequenza. |
| <b>Filtro input immagine</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> |  |
| <b>Specifico per pattern</b> <i>0.0 - 1.0</i> | Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato. |
| <b>Simmetria casuale</b> <i>0.0 - 1.0</i> | Imposta il numero di porzioni che devono essere capovolte/riflesse casualmente in base al comportamento riportato di seguito. |
| <b>Simmetria modalità casuale</b> <i>Orizzontale + Verticale, Orizzontale, Verticale</i> | Determina il comportamento di mirroring della simmetria. |
| <b>Posizione</b> |  |
| <b>Raggio</b> <i>0.0 - 1.0</i> | Imposta il raggio dal centro in cui vengono posizionati i pattern. |
| <b>Raggio casuale</b> <i>0.0 - 1.0</i> | Rende casuale il raggio per ogni porzione del pattern. |
| <b>Moltiplicatore del raggio dell&#39;anello</b> <i>0.0 - 1.0</i> | Modifica la spaziatura di più anelli. |
| <b>Angolo casuale</b> <i>0.0 - 1.0</i> | Rende casuale l’angolo di ogni pattern. Più alti sono i valori, maggiore sarà la rotazione. |
| <b>Fattore Spirale</b> <i>0.0 - 1.0</i> | Trasforma gli anelli in spirali, dove ogni piastrella è posizionata con un raggio leggermente crescente. |
| <b>Pagine affiancate</b> <i>0.0 - 2.0</i> | Consente di impostare la quantità di giri eseguiti da un anello. Questo valore può essere aumentato oltre i limiti. |
| <b>Scostamento lungo la direzione</b> <i>0.0 - 1.0</i> | Sposta ogni pattern fuori dal centro lungo il suo angolo. L’effetto dipende molto da Angolo casuale o ha l’aspetto di un moltiplicatore per il Raggio. |
| <b>Scostamento globale</b> <i>0.0 - 1.0</i> | Traduce l&#39;intera forma. |
| <b>Dimensioni</b> |  |
| <b>Collega pattern</b> <i>Falso/Vero</i> | Rende la lunghezza delle porzioni del pattern dipendente dal raggio, il che significa che ogni forma dovrebbe toccare quella precedente e quella successiva. |
| <b>Dimensioni (Connesso)</b> <i>0.0 - 1.0</i> | Modifica le dimensioni di ogni pattern a livello globale. Una volta connesso, è relativo al raggio totale. |
| <b>Dimensioni casuali</b> <i>0.0 - 1.0</i> | Rende casuale la dimensione di ogni pattern singolarmente. |
| <b>Scala</b> <i>0.0 - 2.0</i> | Ridimensiona in modo uniforme ogni pattern. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Rende casuale il ridimensionamento uniforme. |
| <b>Scala in base al numero di serie</b> <i>0.0 - 1.0</i> | Rende la scala della serie dipendente dalla posizione lungo l&#39;anello. |
| <b>Inverti numero pattern</b> <i>Falso/Vero</i> | Usata con l’opzione precedente, questa opzione consente di invertire il ridimensionamento da piccolo a grande e viceversa. |
| <b>Scala in base al numero di squillo</b> <i>0.0 - 1.0</i> | Rende la scala dipendente dal numero dell&#39;anello. |
| <b>Inverti numero squillo</b> <i>Falso/Vero</i> | Usata con l’opzione precedente, può invertire il ridimensionamento da piccolo a grande e viceversa. |
| <b>Rotazione</b> |  |
| <b>Rotazione motivo</b> <i>0.0 - 1.0</i> | Ruota ogni pattern in modo uniforme. |
| <b>Rotazione motivo casuale</b> <i>0.0 - 1.0</i> | Rende casuale la rotazione della serie. |
| <b>Pivot rotazione pattern</b> <i>Centro, Min X, Max X, Min Y, Max Y</i> | Imposta la posizione del punto fulcro attorno al quale ruotare ogni pattern singolarmente. |
| <b>Orientamento al centro</b> <i>Falso/Vero</i> | Ruota ogni pattern in modo che sia rivolto verso il centro dell&#39;anello. La loro rotazione dà loro lo stesso orientamento - questo può produrre effetti indesiderati con Scostamento lungo la direzione. |
| <b>Rotazione anello</b> <i>0.0 - 1.0</i> | Ruota l&#39;intero anello attorno al centro. |
| <b>Rotazione dell&#39;anello casuale</b> <i>0.0 - 1.0</i> | Rende casuale la rotazione per anello. |
| <b>Scostamento rotazione anello</b> <i>0.0 - 1.0</i> | Sposta la rotazione per anello. |
| <b>Colore</b> |  |
| <b>Colore</b> <i>(valore scala di grigi)</i> | Colore da moltiplicare per il pattern selezionato. |
| <b>Luminanza casuale</b> <i>0.0 - 1.0</i> | Rende casuali il colore o la luminanza per ogni porzione del pattern. |
| <b>Luminanza per scala</b> <i>0.0 - 1.0</i> | Rende la luminanza dipendente dalla scala del singolo pattern. |
| <b>Luminanza per numero di serie</b> <i>0.0 - 1.0</i> | Rende la luminanza dipendente dalla sequenza del pattern. Può essere utilizzato, ad esempio, con spirali. |
| <b>Inverti numero pattern</b> <i>Falso/Vero</i> | Inverte l’opzione precedente. |
| <b>Luminanza per numero di squillo</b> <i>0.0 - 1.0</i> | Rende la luminanza dipendente dalla sequenza dell&#39;anello. |
| <b>Inverti numero squillo</b> <i>Falso/Vero</i> | Inverte l’opzione precedente. |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | Nasconde casualmente i pattern. |
| <b>Colore di sfondo</b> <i>(valore scala di grigi)</i> | Modifica il colore di sfondo in tinta unita. |
| <b>Metodo fusione</b> <i>Aggiungi, Max, Aggiungi Sub</i> | Imposta come fondere i pattern sovrapposti. |
| <b>Opacità globale</b> <i>0.0 - 1.0</i> | Imposta l&#39;opacità globale dell&#39;intero risultato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter-circular.resources/circularsplatter-ex.png" />
        </td>
    </tr>
</table>
