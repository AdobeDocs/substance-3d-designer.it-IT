---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Utilizzare il nodo Tile Generator per creare pattern di riquadri procedurali con controlli personalizzabili per dimensioni, scostamento e variazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore di riquadri
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 6%

---


# Generatore di riquadri

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-generator.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

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

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input pattern 1-6</b> <i>Input scala di grigi</i> | Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;. |
| <b>Sfondo</b> <i>Input scala di grigi</i> | Sfondo da utilizzare al posto del colore in tinta unita. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>X importo</b> <i>1 - 64</i> | Quantità di ripetizioni X del pattern. |
| <b>Importo Y</b> <i>1 - 64</i> | Quantità di ripetizioni Y del pattern. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |
| <b>Pattern</b> |  |
| <b>Pattern</b> <i>Input immagine, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Mezzaluna, Capsula, Cono</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Numero di input del modello</b> <i>1 - 6</i> | Numero di diversi input di immagine da utilizzare. Disponibile solo quando <i>Input immagine</i> è selezionato in precedenza. |
| <b>Distribuzione input pattern</b> <i>Casuale, Per Numero Di Modello</i> | Come scegliere tra diversi input dell&#39;immagine, se è selezionato più di 1. |
| <b>Specifico per pattern</b> <i>0.0 - 1.0</i> | Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato. |
| <b>Filtro input immagine (solo motore >v4)</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> |  |
| <b>Rotazione</b> <i>0, 90, 180, 270</i> | Ruota tutte le porzioni globalmente di un angolo impostato in intervalli di 90 gradi. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Casuale ruota una porzione di uno dei quattro gradini di 90 gradi. |
| <b>Capovolgi Quincunx</b> <i>Falso/Vero</i> | Ruota di 90 gradi ogni due porzioni. |
| <b>Simmetria casuale</b> <i>0.0 - 1.0</i> | Riflette casualmente alcuni pattern in base alla modalità Simmetria casuale selezionata. Più alto è questo valore, maggiore sarà il mirroring dei pattern. |
| <b>Simmetria modalità casuale</b> <i>Orizzontale + Verticale, Orizzontale, Verticale</i> | Determina il comportamento di mirroring quando Simmetria casuale è maggiore di 0. |
| <b>Dimensioni</b> |  |
| <b>Modalità dimensioni</b> <i>Normale - Interstizio, Normale - Dimensioni, Mantieni rapporto, Assoluto, Pixel</i> | Imposta il comportamento generale della dimensione del pattern.<br><br>Normale: l&#39;interstizio consente di definire lo spazio tra gli elementi della serie. È influenzata dall&#39;entità X e Y.<br><br>Normale: la dimensione consente di definire la dimensione degli elementi del pattern, indipendentemente dallo spazio. È influenzata dall&#39;entità X e Y.<br><br>Mantieni proporzioni consente di impostare una dimensione influenzata dalla quantità X e Y, ma le proporzioni X e Y tra i due elementi rimangono invariate.<br><br>Assoluto consente di impostare una dimensione assoluta non influenzata dalla quantità X e Y.<br><br>Pixel consente di impostare una dimensione assoluta in pixel, non influenzata dalla quantità X e Y. La modifica della risoluzione influirà sulle dimensioni degli elementi. |
| <b>Dimensioni Medie</b> <i>0.0 - 1.0</i> | Modifica le dimensioni alternando colonna e riga. |
| <b>Interstizio X/Y</b> <i>0.0 - 1.0</i> | Disponibile solo in modalità Normale - Dimensione interstizio. Modifica lo spazio interstizio. Influisce sulla giuntura tra le forme e consente un controllo non uniforme, a differenza di <b>Scala</b>. |
| <b>Dimensioni (Assoluto/Pixel)</b> <i>0.0 - 1.0</i> | Disponibile solo al di fuori della modalità Normale - Dimensione interstizio. Imposta dimensioni non uniformi, a differenza di <b>Scala</b>. |
| <b>Scala</b> <i>0.0 - 2.0</i> | Imposta Scala globale. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Imposta la variazione di scala globale per porzione. |
| <b>Scala Numero Casuale</b> <i>0 - 1000</i> | Offset valore di inizializzazione variazione scala. |
| <b>Posizione</b> |  |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta l&#39;intero pattern in modo incrementale su ogni riga o colonna consecutiva (il comportamento dipende dal parametro Scostamento verticale). |
| <b>Scostamento casuale</b> <i>0.0 - 1.0</i> | Rende casuale lo scostamento della linea. |
| <b>Offset Numero Casuale</b> <i>0 - 1000</i> | Modifica il valore di inizializzazione relativo per l’effetto di offset casuale. |
| <b>Scostamento verticale</b> <i>Falso/Vero</i> | Consente di specificare se l’effetto Scostamento deve avvenire su righe o linee, Orizzontale o Verticale. |
| <b>Posizione casuale</b> <i>0.0 - 1.0</i> | Rende casuale la posizione in modo non uniforme, con controllo separato per X e Y. |
| <b>Scostamento globale</b> <i>0.0 - 1.0</i> | Sposta l’intero risultato sugli assi X e Y. |
| <b>Rotazione</b> |  |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Esegue una Rotazione libera uniforme di tutte le porzioni del pattern. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Rende casuale la rotazione libera di tutte le porzioni. Più alto è questo valore, più porzioni possono essere ruotate. |
| <b>Colore</b> |  |
| <b>Colore</b> <i>(valore scala di grigi)</i> | Imposta il colore tinta unita della porzione. |
| <b>Luminanza/Colore casuale</b> <i>0.0 - 1.0</i> | Introduce la variazione di colore o luminanza per porzione. |
| <b>Luminanza in base al numero</b> <i>Falso/Vero</i> | Applica una dissolvenza alla luminanza sull’intero pattern. |
| <b>Luminanza per scala</b> <i>Falso/Vero</i> | Rende la variazione della luminanza dipendente dalla scala dei riquadri. |
| <b>Maschera controllo</b> <i>Falso/Vero</i> | Nasconde tutte le altre porzioni. |
| <b>Maschera orizzontale</b> <i>Falso/Vero</i> | Nasconde tutte le altre colonne. |
| <b>Maschera verticale</b> <i>Falso/Vero</i> | Nasconde ogni altra riga. |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | Nasconde casualmente le porzioni. Più alto è questo valore, più porzioni scompariranno. |
| <b>Inverti maschera</b> <i>Falso/Vero</i> | Inverte il risultato di eventuali effetti di mascheratura da questa sezione. |
| <b>Metodo fusione</b> <i>Aggiungi, Max, Aggiungi Sub</i> | Consente di impostare il metodo di fusione da utilizzare. |
| <b>Colore di sfondo</b> <i>(valore scala di grigi)</i> | Imposta il colore di sfondo in tinta unita. |
| <b>Opacità globale</b> <i>0.0 - 1.0</i> | Imposta l’opacità delle porzioni globali. |
| <b>Ordine di rendering inverso</b> <i>Falso/Vero</i> | Renderizza le porzioni in avanti o viceversa. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tilesampler-ex.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-50-18.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-52-4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2020-9-17-14-53-47.png" />
        </td>
    </tr>
</table>
