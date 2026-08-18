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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Circolare a dispersione

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter-circular.png){width="128px"}

![](../../../../../../assets/splatter-circular-color.png){width="128px"}

## Circolare a dispersione (colore)

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Splatter Circular genera un pattern ad anello con vari controlli. Può utilizzare forme predefinite o input personalizzati. È simile a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), ma con un posizionamento circolare invece di una griglia.

Questo risulta utile quando si desidera posizionare le forme in modo circolare con varie opzioni di randomizzazione.

## Parametri

### Input

Entrambi gli ingressi sono opzionali.

* **Input immagine pattern 1-6**: *Input scala di grigi (input colore)*\
  Solo circolare splatter: immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Input immagine&quot;.
* **Sfondo**: *Input scala di grigi (input colore)*

### Parametri

* **Entità motivo**: *1 - 64*\
  Quantità di porzioni di pattern da posizionare su un anello.
* **Quantità motivo casuale**: *0,0 - 1,0*\
  Randomizzazione della quantità di pattern da posizionare. Consigliato per un valore Anello maggiore di 1.
* **Quantità pattern casuale min**: *1 - 10* Imposta la quantità minima di pattern per la randomizzazione.
* **Fattore squillo**: *1 - 10*\
  Imposta il numero di anelli da riempire. Gli anelli sono sempre posizionati all&#39;interno di quello esterno, e lo spazio uniformemente.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Pattern**
  * **Pattern**: *Input immagine, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Crescente, Capsula, Cono*\
    Seleziona la forma del motivo da utilizzare.
  * **Numero di input pattern**: *1 - 6* Imposta il numero di input di immagini diversi da utilizzare. Disponibile solo quando *Input immagine* è selezionato in precedenza.
  * **Distribuzione Input Pattern**: *Casuale, Per Numero Pattern, Per Numero Anello* Imposta La Modalità Di Selezione Di Più Input Pattern. Casuale significa che ne è stato scelto uno casuale, Numero pattern significa che sono semplicemente inseriti in una sequenza ciclica, Con numeri di anello significa che ogni anello ha un altro in sequenza.
  * **Filtro input immagine**: *Bilineare + Mipmap, Bilineare, Più vicino*
  * **Specifico per pattern**: *0,0 - 1,0*\
    Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato.
  * **Simmetria casuale**: *0,0 - 1,0*\
    Imposta il numero di porzioni che devono essere capovolte/riflesse casualmente in base al comportamento riportato di seguito.
  * **Modalità casuale simmetria**: *Orizzontale + Verticale, Orizzontale, Verticale* Determina il comportamento di mirroring della simmetria.
* **Posizione**
  * **Raggio**: *0,0 - 1,0*\
    Imposta il raggio dal centro in cui vengono posizionati i pattern.
  * **Raggio casuale**: *0.0 - 1.0* Rende casuale il raggio per ogni porzione del pattern.
  * **Moltiplicatore del raggio dell&#39;anello**: *0,0 - 1,0*\
    Modifica la spaziatura di più anelli.
  * **Angolo casuale**: *0.0 - 1.0* Rende casuale l&#39;angolo di ogni pattern. Più alti sono i valori, maggiore sarà la rotazione.
  * **Fattore Spirale**: *0,0 - 1,0*\
    Trasforma gli anelli in spirali, dove ogni piastrella è posizionata con un raggio leggermente crescente.
  * **Pagine affiancate**: *0.0 - 2.0* Imposta la quantità di giri consentiti da un anello. Questo valore può essere aumentato oltre i limiti.
  * **Scostamento lungo la direzione**: *0.0 - 1.0*\
    Sposta ogni pattern fuori dal centro lungo il suo angolo. L’effetto dipende molto da Angolo casuale o ha l’aspetto di un moltiplicatore per il Raggio.
  * **Scostamento globale**: *0,0 - 1,0*\
    Traduce l&#39;intera forma.
* **Dimensioni**
  * **Connetti pattern**: *False/True* Rende la lunghezza delle porzioni del pattern dipendente dal raggio, ovvero ogni forma deve toccare quella precedente e quella successiva.
  * **Dimensioni (Connesso)**: *0,0 - 1,0*\
    Modifica le dimensioni di ogni pattern a livello globale. Una volta connesso, è relativo al raggio totale.
  * **Dimensioni casuali**: *0,0 - 1,0*\
    Rende casuale la dimensione di ogni pattern singolarmente.
  * **Scala**: *0,0 - 2,0*\
    Ridimensiona in modo uniforme ogni pattern.
  * **Scala casuale**: *0,0 - 1,0*\
    Rende casuale il ridimensionamento uniforme.
  * **Scala in base al numero di serie**: *0.0 - 1.0* La scala del pattern dipende dalla posizione lungo l&#39;anello.
  * **Inverti numero modello**: *False/True*\
    Usata con l’opzione precedente, questa opzione consente di invertire il ridimensionamento da piccolo a grande e viceversa.
  * **Scala in base al numero dell&#39;anello**: *0.0 - 1.0* Rende la scala dipendente dal numero dell&#39;anello.
  * **Inverti numero anello**: *False/True* Se utilizzato con l&#39;opzione precedente, può invertire il ridimensionamento da piccolo a grande e viceversa.
* **Rotazione**
  * **Rotazione motivo**: *0.0 - 1.0* Ruota ogni motivo in modo uniforme.
  * **Rotazione motivo casuale**: *0,0 - 1,0*\
    Rende casuale la rotazione della serie.
  * **Rotazione Motivo Pivot**: *Centro, Min X, Max X, Min Y, Max Y*\
    Imposta la posizione del punto fulcro attorno al quale ruotare ogni pattern singolarmente.
  * **Orientamento Al Centro**: *Falso/Vero*\
    Ruota ogni pattern in modo che sia rivolto verso il centro dell&#39;anello. La loro rotazione dà loro lo stesso orientamento - questo può produrre effetti indesiderati con Scostamento lungo la direzione.
  * **Rotazione anello**: *0.0 - 1.0* Ruota l&#39;intero anello attorno al centro.
  * **Rotazione anello casuale**: *0,0 - 1,0* Rende casuale la rotazione per anello.
  * **Scostamento rotazione anello**: *0,0 - 1,0*\
    Sposta la rotazione per anello.
* **Colore**
  * **Colore**: *(valore scala di grigio)*Colore da moltiplicare con il pattern selezionato.
  * **Luminanza casuale**: *0.0 - 1.0* Rende casuale il colore o la luminanza per ogni porzione del pattern.
  * **Luminanza in base alla scala**: *0.0 - 1.0* Rende la luminanza dipendente dalla scala del singolo pattern.
  * **Luminanza in base al numero di serie**: *0.0 - 1.0* La luminanza dipende dalla sequenza di serie. Può essere utilizzato, ad esempio, con spirali.
  * **Inverti numero pattern**: *False/True* Inverte l&#39;opzione precedente.
  * **Luminanza in base al numero dell&#39;anello**: *0.0 - 1.0* La luminanza dipende dalla sequenza dell&#39;anello.
  * **Inverti numero anello**: *False/True* Inverte l&#39;opzione precedente.
  * **Maschera casuale**: *0.0 - 1.0* Nasconde casualmente i pattern.
  * **Colore sfondo**: *(valore scala di grigio)*Modifica il colore di sfondo in tinta unita.
  * **Metodo fusione**: *Aggiungi, Max, Aggiungi secondario* Imposta come fondere i pattern sovrapposti.
  * **Opacità globale**: *0.0 - 1.0* Imposta l&#39;opacità globale dell&#39;intero risultato.

## Immagini di esempio

![](../../../../../../assets/circularsplatter-ex.png)

</td>
</tr>
</table>
