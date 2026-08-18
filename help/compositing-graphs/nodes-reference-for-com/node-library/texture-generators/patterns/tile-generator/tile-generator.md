---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Utilizzare il nodo Tile Generator per creare pattern di sezioni procedurali con controlli personalizzabili per dimensioni, scostamento e variazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore di riquadri
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---


# Generatore di riquadri

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

## Tile Generator (a colori)

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Tile Generator è uno dei nodi più avanzati della libreria. Se imparate a padroneggiarlo, potete creare qualsiasi tipo di pattern (entro alcune limitazioni). A partire dalla versione 2017 2.1 sono stati apportati alcuni aggiornamenti importanti, che allineano questo nodo alle funzionalità di [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md).

Questo nodo è molto utile per una varietà di scenari, ma tieni presente che la semplice lettura dei parametri non ti insegnerà completamente come utilizzarli. Ti consigliamo di sperimentare anche tu!

Per il 99% di tutti i casi, la versione a colori NON è necessaria!

Alcuni suggerimenti generali sull&#39;utilizzo:

* Potete iniziare con una forma di base, ma se disponete di un input personalizzato (impostate **Tipo di pattern** su *Input immagine*), dovete prima crearlo! Determina gran parte dell&#39;aspetto.
* Iniziate impostando correttamente le quantità X e Y.
* Trovate la modalità giusta per **dimensioni**: le modalità relative come **Interstizio** si comportano in modo molto diverso dalle modalità **Assoluto**.
* Successivamente, regolate **Scala** globale e **Dimensione** non uniforme.
* Infine, modifica qualsiasi parametro **&quot;Variation&quot;** finché non soddisfa le tue esigenze. La sottigliezza è la chiave della variazione!

## Parametri

### Input

* **Input pattern 1-6**: *Input scala di grigi*\
  Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;.
* **Sfondo**:*Input scala di grigi* Sfondo da utilizzare al posto del colore a tinta unita.

### Parametri

* **Importo X**: *1 - 64*\
  Quantità di ripetizioni X del pattern.
* **Importo Y**: *1 - 64*\
  Quantità di ripetizioni Y del pattern.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Pattern**
  * **Pattern**: *Input immagine, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Crescente, Capsula, Cono*\
    Seleziona la forma del motivo da utilizzare.
  * **Numero di input pattern**: *1 - 6* Numero di input immagine diversi da utilizzare. Disponibile solo quando *Input immagine* è selezionato in precedenza.
  * **Distribuzione input pattern**: *Casuale, Per numero di pattern* Come scegliere tra i diversi input di immagine, se è selezionato più di 1.
  * **Specifico per pattern**: *0,0 - 1,0*\
    Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato.
  * **Filtro input immagine (solo motore >v4)**: *Bilineare + Mipmap, Bilineare, Più vicino*
  * **Rotazione**: *0, 90, 180, 270* Ruota tutte le porzioni globalmente di un angolo impostato in intervalli di 90 gradi.
  * **Rotazione casuale**: *0,0 - 1,0* La rotazione casuale di una porzione determina uno dei quattro passi di 90 gradi.
  * **Rifletti in quincunx**: *False/True* Ruota di 90 gradi tutte le altre porzioni.
  * **Simmetria casuale**: *0.0 - 1.0* Riflette casualmente alcuni pattern in base alla modalità simmetria casuale selezionata. Più alto è questo valore, maggiore sarà il mirroring dei pattern.
  * **Modalità casuale simmetria**: *Orizzontale + Verticale, Orizzontale, Verticale* Determina il comportamento di mirroring quando Simmetria casuale è maggiore di 0.
* **Dimensioni**
  * **&#x200B;**&#x200B;Modalità dimensioni **:***Normale - Interstizio, Normale - Dimensioni, Mantieni proporzioni, Assoluto, Pixel*Imposta il comportamento generale della dimensione del pattern.\
    Normale (Normal) - Interstizio (Interstice) consente di definire lo spazio tra gli elementi della serie. È influenzata dall&#39;entità X e Y.\
    Normale (Normal) - Dimensione (Size) consente di definire la dimensione degli elementi della serie, indipendentemente dallo spazio. È influenzata dall&#39;entità X e Y.\
    Mantieni rapporto consente di impostare una dimensione influenzata dalla quantità X e Y, ma il rapporto X e Y tra i due viene lasciato intatto.\
    Assoluto consente di impostare una dimensione assoluta non influenzata dalla quantità X e Y.\
    Pixel consente di impostare una dimensione assoluta in pixel, non influenzata dalla quantità X e Y. La modifica della risoluzione influirà sulle dimensioni degli elementi.
  * **Dimensioni medie**: *0.0 - 1.0* Modifica le dimensioni alternando colonna e riga.
  * **Interstizio X/Y**: *0.0 - 1.0* Disponibile solo in modalità Normale - Dimensione interstizio. Modifica lo spazio interstizio. Influisce sulla giuntura tra le forme e consente un controllo non uniforme, a differenza di **Scala**.
  * **Dimensioni (Assoluto/Pixel)**: *0,0 - 1,0*\
    Disponibile solo al di fuori della modalità Normale - Dimensione interstizio. Imposta dimensioni non uniformi, a differenza di **Scala**.
  * **Scala**: *0.0 - 2.0* Imposta Scala Globale.
  * **Scala casuale**: *0.0 - 1.0* Imposta la variazione di scala globale per porzione.
  * **Scala valore di inizializzazione casuale**: *0 - 1000* Offset del valore di inizializzazione della variazione della scala.
* **Posizione**
  * **Scostamento**: *0.0 - 1.0* Sposta l&#39;intero pattern in modo incrementale su ogni riga o colonna consecutiva (il comportamento dipende dal parametro Scostamento verticale).
  * **Scostamento casuale**: *0,0 - 1,0* Rende casuale lo scostamento della linea.
  * **Offset numero casuale**: *0 - 1000* Modifica il valore di inizializzazione relativo per l&#39;effetto di offset casuale.
  * **Scostamento verticale**: *False/True* Imposta se l&#39;effetto Scostamento si verifica su righe o linee; Orizzontale o verticale.
  * **Posizione casuale**: *0,0 - 1,0* Rende casuale la posizione in modo non uniforme, con controllo separato per X e Y.
  * **Scostamento globale**: *0.0 - 1.0* Sposta l&#39;intero risultato sugli assi X e Y.
* **Rotazione**
  * **Rotazione**: *0.0 - 1.0* Esegue una Rotazione libera uniforme di tutte le porzioni del pattern.
  * **Rotazione casuale**: *0.0 - 1.0* Rende casuale la rotazione libera di tutte le porzioni. Più alto è questo valore, più porzioni possono essere ruotate.
* **Colore**
  * **Colore**: *(valore scala di grigio)*Imposta il colore tinta unita della porzione.
  * **Luminanza/Colore casuale**: *0.0 - 1.0* Introduce la variazione del colore per porzione o della luminanza.
  * **Luminanza in base al numero**: *False/True* Applica una dissolvenza alla luminanza sull&#39;intero pattern.
  * **Luminanza In Base Alla Scala**: *False/True* Rende La Variazione Della Luminanza Dipendente Dalla Scala Dei Riquadri.
  * **Maschera controllo**: *False/True* Nasconde ogni altra porzione.
  * **Maschera orizzontale**: *False/True* Nasconde ogni altra colonna.
  * **Maschera verticale**: *False/True* Nasconde ogni altra riga.
  * **Maschera casuale**: *0.0 - 1.0* Nasconde casualmente le porzioni. Più alto è questo valore, più porzioni scompariranno.
  * **Inverti maschera**: *False/True* Inverte il risultato di eventuali effetti di mascheratura da questa sezione.
  * **Metodo fusione**: *Aggiungi, Max, Aggiungi secondario* Imposta il metodo di fusione da utilizzare.
  * **Colore sfondo**: *(valore scala di grigio)*Imposta il colore di sfondo in tinta unita.
  * **Opacità globale**: *0.0 - 1.0* Imposta l&#39;opacità delle porzioni globali.
  * **Ordine di rendering inverso**: *False/True* Esegue il rendering dei riquadri in primo piano o viceversa.

## Immagini di esempio

![](../../../../../../assets/tilesampler-ex.png)

![](../../../../../../assets/image2020-9-17-14-50-18.png)

![](../../../../../../assets/image2020-9-17-14-52-4.png)

![](../../../../../../assets/image2020-9-17-14-53-47.png)

</td>
</tr>
</table>
