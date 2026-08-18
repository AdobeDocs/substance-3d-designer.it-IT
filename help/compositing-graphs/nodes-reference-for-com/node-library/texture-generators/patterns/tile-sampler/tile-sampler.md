---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# Affianca Sampler

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-sampler.png){width="128px"}

## Affianca Sampler (a colori)

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Affianca Sampler è il nodo più avanzato per la generazione di pattern di riquadri. È una versione evoluta e più complessa di [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partire da 2017 2.1, le differenze sono molto più piccole tra Tile Sampler e [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Le differenze principali si riscontrano ora solo nei sette slot di mappa disponibili per le funzioni Scala, Posizione, Rotazione, Dimensione, Colore e Mascheratura. Il loro effetto può essere fuso in separatamente.

Tile Sampler è utile per la creazione di pattern procedurali artificiali, con un controllo aggiuntivo su alcuni parametri guidati da mappe di input esterne.

Assicurati di conoscere [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) prima di passare al Tile Sampler. Nella maggior parte dei casi, troverai [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) sufficiente e non avrai bisogno della complessità aggiuntiva di Tile Sampler.

## Parametri

### Input

* **Input pattern 1-6**: *Input scala di grigi / Input colore*\
  Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;.\
  La quantità di input disponibili è determinata dal parametro **Numero di input pattern**.
* **Input mappa scala**: *Input scala di grigi* Mappa scala di grigi per il ridimensionamento delle porzioni di unità.
* **Input mappa Spostamento**: *Input scala di grigi* Mappa scala di grigi per gestire lo spostamento dei riquadri.
* **Input Mappa di rotazione**: *Input scala di grigi*\
  Mappa in scala di grigi per guidare la rotazione delle porzioni.
* **Input mappa vettoriale**: *Input colore*\
  Mappa vettoriale colori per applicare il ridimensionamento non uniforme.
* **Input mappa colori**: *Input scala di grigi/Input colore* Map to drive per-tile tinting.
* **Input mappa maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per nascondere determinate porzioni.
* **Input mappa distribuzione pattern**: *Input scala di grigi*\
  Slot maschera utilizzato per gestire più input di pattern personalizzati.
* **Input sfondo**: *Input in scala di grigio/Input colore* Immagine di sfondo facoltativa.

### Parametri

* **Importo X**: *0 - 64*\
  Quantità di ripetizioni X del pattern.
* **Importo Y**: *0 - 64*\
  Quantità di ripetizioni Y del pattern.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Pattern**
  * **Pattern**: *Input motivo, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana dorata, Crescente, Capsula, Cono*\
    Seleziona la forma del motivo da utilizzare.
  * **Numero di input pattern**: *1 - 6* Quantità di pattern personalizzati tra cui scegliere in modo casuale.
  * **Distribuzione input pattern**: *Casuale, Numero pattern, Mappa distribuzione* Imposta la modalità di scelta di più input pattern. Casuale significa che è stato scelto un numero casuale. Numero pattern significa che sono semplicemente inseriti in una sequenza a ciclo continuo. La mappa di distribuzione utilizza un input mappa in scala di grigio per il posizionamento dell&#39;unità.
  * **Filtro input pattern (motore > v4)**: *Bilineare + Mipmap, Bilineare, Più vicino*
  * **Specifico per pattern**: *0,0 - 1,0*\
    Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato.
  * **Casuale specifico per pattern**: *0.0 - 1.0* L&#39;effetto di randomizzazione dipende dal pattern selezionato.
  * **Rotazione**: *0, 90, 180, 270* Rotazione graduale (90 gradi).
  * **Rotazione casuale**: *0,0 - 1,0* Rotazione libera casuale per porzione.
  * **Simmetria casuale**: *0.0 - 1.0* Imposta il numero di porzioni da capovolgere/riflettere in modo casuale in base al comportamento riportato di seguito.
  * **Modalità casuale simmetria**: *Orizzontale + Verticale, Orizzontale, Verticale* Determina il comportamento di mirroring della simmetria.
* **Dimensioni**
  * **Modalità dimensioni**: *Normale, Mantieni proporzioni, Assoluto, Pixel* Imposta il comportamento generale delle dimensioni del pattern.\
    Normale consente di definire la dimensione degli elementi della serie. È influenzata dall&#39;entità X e Y.\
    Mantieni rapporto consente di impostare una dimensione influenzata dalla quantità X e Y, ma il rapporto X e Y tra i due viene lasciato intatto.\
    Assoluto consente di impostare una dimensione assoluta non influenzata dalla quantità X e Y.\
    Pixel consente di impostare una dimensione assoluta in pixel, non influenzata dalla quantità X e Y. La modifica della risoluzione influirà sulle dimensioni degli elementi.
  * **Dimensioni (Assoluto/Pixel)**: *0.0 - 1.0* Modifica le proporzioni non uniformi per le porzioni. Il comportamento esatto dipende dalla modalità Dimensione.
  * **Dimensioni casuali**: *0,0 - 1,0* Rende casuali le proporzioni per porzione.
  * **Scala**: *0.0 - 10.0* Imposta la scala dei riquadri globale.
  * **Scala casuale**: *0,0 - 1,0* Rende casuale la scala per porzione
  * **Moltiplicatore mappa scala**: *0.0 - 1.0* Fusioni nell&#39;effetto della mappa scala.
  * **Moltiplicatore mappa vettoriale scala**: *0.0 - 1.0* Fusioni nell&#39;effetto della mappa vettoriale scala per determinare un ridimensionamento non uniforme.
  * **La parametrizzazione della scala ha effetto**: *X e Y, X, Y* Imposta gli assi interessati dalla parametrizzazione della scala. Può essere utilizzato per fare in modo che la mappa scala influisca solo su X o Y di elementi.
* **Posizione**
  * **Posizione casuale**: *0.0 - 10.0* Rende casuale la posizione della porzione su entrambi gli assi.
  * **Scostamento**: *0,0 - 1,0*\
    Sposta le porzioni in base al tipo di scostamento.
  * **Tipo di offset**: *quincux orizzontale, quincux verticale, globale orizzontale, globale verticale* Modifica la direzione in cui opera l&#39;offset.
  * **Scostamento globale**: *0.0 - 1.0* Scostamento globale di tutte le porzioni sull&#39;asse X o Y.
  * **Intensità mappa di Spostamento**: *0.0 - 1.0* Fusioni nell&#39;intensità della mappa di Spostamento sullo scostamento.
  * **Angolo di Spostamento**: *0.0 - 1.0* Imposta l&#39;angolo di spostamento.
  * **Spostamento mappa vettoriale**: *0.0 - 1.0* Utilizza la mappa vettoriale per determinare lo spostamento e l&#39;angolo.
* **Rotazione**
  * **Rotazione**: *0.0 - 1.0* Ruota globalmente tutte le porzioni.
  * **Rotazione casuale**: *0,0 - 1,0* Ruota in modo casuale per porzione.
  * **Moltiplicatore Mappa di rotazione**: *0.0 - 1.0* Fusioni nell&#39;effetto della Mappa di rotazione sulla rotazione per porzione.
  * **Moltiplicatore mappa vettoriale**: *0.0 - 1.0* Utilizza la mappa vettoriale per attivare la rotazione per porzione.
* **Colore**
  * **Soglia mappa maschera**: *0.0 - 1.0* Soglia per la mappa maschera quando iniziare a nascondere i riquadri.
  * **Inversione mappa maschera**: *False/True* Inverte l&#39;effetto mappa maschera.
  * **Tecnica di campionamento mappa maschera**: *Centro pattern, rettangolo di selezione pattern (più lento)*Se il nascondiglio deve essere determinato da un singolo punto o da un rettangolo di selezione. Evita che i pixel isolati causino effetti strani.
  * **Maschera casuale**: *0.0 - 1.0* La mascheratura casuale funziona parallelamente alla mappa della maschera.
  * **Inverti maschera**: *False/True* Inverte la maschera casuale.
  * **Metodo di fusione**: *Aggiungi/Sub, Max (Tile Sampler) /* Aggiungi/Sub, Fusione Alpha* (Colore Tile Sampler)*Metodo di fusione per le porzioni sullo sfondo e l&#39;una sull&#39;altra.
  * **Colore**: *(valore scala di grigio) / (valore colore)*Tinta unita, colore porzione globale.
  * **Colore/Luminanza casuale**: *0.0 - 1.0* Randomizzazione del colore, per porzione.
  * **Modalità Di Parametrizzazione Del Colore**: *Input Colore, Scala, Indice Linea, Indice Riga, Indice Pattern (Tile Sampler)*\
    */ *Mappa colore, Scala, Indice linea, Indice riga, Indice pattern, Posizione centro pattern, Posizione centro pattern (RG), Dimensione sfera (B) (Colore porzione Sampler)**Imposta esattamente la casualità del colore cui sono associati i parametri.
  * **Moltiplicatore di parametrizzazione colore**: *0.0 - 1.0* Fusioni nell&#39;effetto di parametrizzazione sopra riportato.
  * **Effetto della parametrizzazione del colore (solo colore):** **RGB+Alpha, solo RGB, solo Alpha** Imposta l&#39;effetto della parametrizzazione sul colore.
  * **Opacità globale (solo scala di grigi)**: *0.0 - 1.0* Imposta l&#39;opacità globale delle porzioni.
  * **Colore di sfondo**: *(valore scala di grigio) / (valore colore)*Imposta il colore di sfondo in tinta unita.
  * **Ordine di rendering inverso**: *False/True* Inverte l&#39;ordine di rendering per passare dal primo all&#39;ultimo.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tilesampler-ex2.png" width="256px"/></div> |
| --- |
|  |

*Nell&#39;esempio viene illustrato come i parametri sono guidati dalle mappe di input (Distribuzione pattern, Scala, Rotazione).*

</td>
</tr>
</table>
