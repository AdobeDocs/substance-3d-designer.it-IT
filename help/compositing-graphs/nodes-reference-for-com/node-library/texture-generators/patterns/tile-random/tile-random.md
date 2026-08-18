---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Utilizzate il nodo Affianca casuale per creare pattern di riquadri casuali con variazioni procedurali per effetti di texture organica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Affianca casuale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---


# Affianca casuale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

## Affianca casuale (a colori)

**Ingresso:** *Generatori/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Porzione Casuale genera un motivo di porzione procedurale che presenta un po&#39; più di caos nelle forme delle porzioni rispetto alla sua controparte, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Lo fa dividendo casualmente alcune porzioni in porzioni più piccole. Ti consigliamo di trovare prima il modo di aggirare il Tile Generator prima di affrontare Tile Random, come molti concetti sono simili.

Affianca casuale viene utilizzato al posto di [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) quando l&#39;obiettivo è un modello meno organizzato e dall&#39;aspetto più vecchio. Tuttavia, presenta dei limiti, quindi [Affianca Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) per qualsiasi altra esigenza avanzata.

## Parametri

### Input

* **Input pattern**: *Input scala di grigi (input colore)*\
  Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;.
* **Input in background**: *Input in scala di grigi (input a colori)*

### Parametri

* **Importo X**: *1 - 64*\
  Quantità di ripetizioni X del pattern.
* **Importo Y**: *1 - 64*\
  Quantità di ripetizioni Y del pattern.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Pattern**
  * **Pattern**: *Input motivo, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana dorata, Crescente, Capsula, Cono*\
    Seleziona la forma del motivo da utilizzare.
  * **Filtro input immagine (motore > v4)**: *Bilineare + Mipmap, Bilineare, Più vicino*
  * **Specifico per pattern**: *0,0 - 1,0*\
    Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato.
  * **Casuale specifico per pattern**: *0,0 - 1,0* L&#39;effetto di casualizzazione dipende dal pattern selezionato.
  * **Rotazione**: *0, 90, 180, 270, orizzontale casuale, verticale casuale* Imposta la rotazione a intervalli di 90 gradi, con randomizzazione facoltativa.
  * **Rotazione casuale**: *0.0 - 1.0* Aggiunge una rotazione libera casuale.
  * **Simmetria casuale**: **0.0 - 1.0** riflette casualmente alcuni pattern in base alla modalità simmetria casuale selezionata. Più alto è questo valore, maggiore sarà il mirroring dei pattern.
  * **Modalità casuale simmetria**: *Orizzontale + Verticale, Orizzontale, Verticale* Determina il comportamento di mirroring quando Simmetria casuale è maggiore di 0.
* **Dividere**
  * **Modalità**: *nessuna, automatica, orizzontale automatica, verticale automatica, h+v* Imposta la regola su come dividere le porzioni.
  * **Soglia**: *0.0 - 1.0* Soglia di dimensione per specificare quando dividere una porzione.
  * **Moltiplicatore**: *0 - 10* Moltiplicatore di divisione. Più alto è questo valore, maggiori saranno le divisioni.
* **Dimensioni**
  * **X casuale**: *0.0 - 1.0* Rende casuale il ridimensionamento non uniforme sull&#39;asse X.
  * **A caso Y**: *0.0 - 1.0* Rende casuale il ridimensionamento non uniforme sull&#39;asse Y.
* **Interstizio**
  * **Modalità**: *Rispetto al brick più piccolo, Rispetto al brick più grande* Imposta l&#39;interstizio delle dimensioni del brick rispetto a.
  * **Quantità**: *0,0 - 1,0* Imposta le dimensioni dello spazio tra i mattoni.
* **Forma**
  * **Scala**: *0.0 - 1.0* Ridimensiona globalmente ogni porzione.
  * **Ridimensionamento casuale**: *0,0 - 1,0* Ridimensionamento casuale in base ai singoli riquadri.
  * **Rotazione**: *0.0 - 1.0* Rotazione globale per ogni riquadro.
  * **Rotazione casuale**: *0,0 - 1,0* Ruota in modo casuale in base ai singoli riquadri.
  * **Vincolo di rotazione**: *False/True* Vincola la scala in modo che le porzioni ruotate non si sovrappongano mai.
* **Posizione**
  * **Scostamento**: *0,0 - 1,0*\
    Sposta o converte le porzioni a livello globale, scorre solo sull’asse X
  * **Scostamento casuale**: *0,0 - 1,0* Scostamento casuale per porzione, scivola solo sull&#39;asse X
  * **Casuale**: *0.0 - 1.0* Rende casuale la posizione; le porzioni si spostano sia sull&#39;asse X che sull&#39;asse Y.
  * **Vincoli casuali**: *False/True* I vincoli vengono ridimensionati in modo che le porzioni si tocchino, ma non si sovrappongano. Attenua significativamente l’effetto Posizione casuale.
* **Colore**
  * **Colore**: *(valore scala di grigio) / (valore colore)*Imposta il colore in tinta unita per tutte le porzioni.
  * **Colore casuale**: *0.0 - 1.0* Rende casuale il colore per porzione.
  * **Parametrizzazione colore**: *nessuna, area, dimensione x, dimensione y* Rende la variazione del colore dipendente da una di queste impostazioni.
  * **Intensità parametrizzazione colore**: *0.0 - 1.0* Moltiplicatore per l&#39;effetto di parametrizzazione sopra riportato.
  * **Effetto di parametrizzazione del colore (solo per il colore):** **RGB+Alpha, solo RGB, solo Alpha** Determina l&#39;effetto di parametrizzazione per il solo colore.
  * **Colore di sfondo**: *(valore scala di grigio) / (valore colore)*Imposta il colore di sfondo in tinta unita.
  * **Metodo fusione**: *Aggiungi/Sotto, Max /* Aggiungi/Sotto, Fusione Alpha (Colore)**Imposta il metodo fusione per le porzioni sullo sfondo.
* **Maschera**
  * **Casuale**: *0.0 - 1.0* Inizia casualmente la mascheratura delle porzioni. Più alto è il valore, più porzioni scompaiono.
  * **Inverti**: *Falso/Vero*\
    Inverte il risultato della maschera.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/tile-random-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
