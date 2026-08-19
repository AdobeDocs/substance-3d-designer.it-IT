---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Usa il nodo di Atlas scatter per dispersione le texture su un atlas per creare pattern a piastrelle da materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 0%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/atlas-scatter.png){width="200px"}

## Atlas scatter

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Estrai gli elementi da un Atlas e dispersione sullo sfondo. Gli input Atlas sono materiali completi, costituiti da singoli elementi disposti e imballati su un singolo foglio di texture. Questo nodo li suddivide (utilizzando un processo [Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md) interno) e li dispersione, in modo simile a [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). Per funzionare, l’Atlas scatter richiede almeno un input mappa opacità e un input mappa Height per l’Atlas.

>[!NOTE]
>
> Centinaia di [Atlanti](https://source.substance3d.com/allassets?assetType=substanceAtlas), pronti per essere utilizzati nel nodo Atlas scatter, sono disponibili in [Substance Source](https://source.substance3d.com/).

## Input e parametri

### Parametri

* **Risoluzione input Atlas**: *Risoluzione, da 1 a 12*\
  Impostare manualmente la risoluzione dell&#39;atlas di input completo per garantire un buon rapporto prestazioni/qualità.
* **Importo X**: *1 - 64*\
  Quantità di X ripetizioni del pattern.
* **Importo Y**: *1 - 64*\
  Quantità di ripetizioni Y del pattern.
* **Pattern**
  * **Intervallo pattern**: *0 - 10*\
    Definisce l’intervallo di pattern da diffondere. Se impostato su 0, verranno utilizzati tutti i pattern.
  * **Modalità distribuzione pattern**: *Casuale, Indice pattern, Indice linea, Indice colonna* Definisce l&#39;ordine in cui vengono utilizzati gli elementi atlas.
  * **Moltiplicatore mappa distribuzione pattern**: *0.0 - 1.0*\
    Seleziona il motivo forma in funzione del valore di scala di grigi dell’immagine di input.
  * **Rotazione motivo**: *0, 90, 180, 270*\
    Applica una rotazione fissa a ciascun elemento atlante, in base alla quantità di gradi selezionata.
  * **Rotazione motivo casuale**: *0,0 - 1,0*\
    Applica una rotazione casuale alla porzione impostata degli elementi atlas.
  * **Precisione rilevamento forme atlante**: *forme semplici o piccole, forme complesse o grandi, nessuna modalità di errore*\
    Imposta la precisione con cui vengono rilevate le forme. Maggiore è la precisione, maggiore sarà l&#39;impatto sulle prestazioni.
  * **Riduci opacità atlante (rilevamento più rapido)**: *-4 - 0*\
    Consente di controllare il rapporto di ridimensionamento della mappa di opacità dell&#39;atlante di input, utilizzata per il rilevamento delle forme. Una risoluzione più bassa migliora le prestazioni a costo di precisione.
  * **Ignora forma più piccola di**: *0.0 - 1.0* Imposta le dimensioni minime di una forma da rilevare, espresse come rapporto dell&#39;immagine complessiva
* **Dimensioni**
  * **Scala**: *0,0 - 5,0*\
    Imposta la scala relativa delle forme a dispersione.
  * **Scala casuale**: *0,0 - 1,0*\
    Definisce il moltiplicatore per l’applicazione del ridimensionamento casuale a ciascuna forma distribuita.
  * **Scala senza sovrapposizione**: *0,0 - 1,0*\
    Riduce la scala della forma in modo che non si sovrappongano.
  * **Moltiplicatore mappa scala**: *0,0 - 1,0*\
    Moltiplica la scala della forma in funzione del valore di scala di grigi dell’immagine di input.
  * **Dimensioni**: *0,0 - 1,0*\
    Imposta la scala relativa delle forme distribuite in base alla lunghezza (X) e alla larghezza (Y).
  * **Rapporto dimensioni da Bg Pendenza**: *0,0 - 1,0*\
    Modifica le proporzioni della forma in funzione della pendenza del height di sfondo.
  * **Mantieni proporzioni**: *0.0 - 1.0*\
    Determina l’entità di mantenimento delle proporzioni originali delle forme disperse, anziché utilizzare le relative proporzioni delle celle della griglia, ovvero il rapporto tra i valori Quantità X e Quantità Y.
* **Posizione**
  * **Posizione casuale**: *0,0 - 2,0*\
    Moltiplicatore per spostare ogni forma in direzione casuale dal punto iniziale della griglia.
  * **Distribuzione casuale**: *Gaussiana, Uniforme*\
    Passa da una distribuzione gaussiana a una distribuzione uniforme per la posizione casuale. La distribuzione gaussiana produrrà un risultato più organico rispetto alla distribuzione uniforme.
  * **Moltiplicatore mappa vettoriale**: *0,0 - 1,0*\
    Controlla l&#39;influenza dell&#39;input della mappa vettoriale per spostare le forme nella direzione del vettore specificata dai canali rosso (X) e verde (Y) della mappa.
  * **Scostamento orizzontale**: *-2,0 - 2,0*\
    Moltiplicatore per lo scostamento della posizione lungo l&#39;asse X.
  * **Scostamento Verticale**: *-2.0 - 2.0*\
    Moltiplicatore per lo scostamento della posizione lungo l&#39;asse Y.
  * **Opzione Oltre I Limiti**: *Ridimensiona Forma, Vincola Posizione*\
    A causa della natura tecnica dello splatter, le forme non possono essere disegnate a più di 2 celle di distanza dalla loro posizione originale. Se una forma diventa troppo grande o viene spostata troppo, sono disponibili due opzioni: - Scala forma riduce la dimensione della forma quando raggiunge un limite - Vincola posizione riporta la forma alla posizione originale
* **Rotazione**
  * **Rotazione**: *0,0 - 1,0*\
    Consente di controllare la rotazione locale per tutte le forme.
  * **Rotazione casuale**: *0,0 - 1,0*\
    Un moltiplicatore per una quantità casuale di rotazione applicata per forma.
  * **Rotazione da Bg Pendenza**: *0,0 - 1,0*\
    Modifica la rotazione della forma in funzione della pendenza del height di sfondo. Generalmente utilizzato in combinazione con il parametro &quot;Rapporto dimensioni da Pendenza di sfondo&quot;
  * **Moltiplicatore Mappa di rotazione**: *0,0 - 1,0*\
    Moltiplica la rotazione della forma in funzione del valore di scala di grigi dell’immagine di input.
  * **Moltiplicatore mappa vettoriale**: *0,0 - 1,0*\
    Imposta la rotazione della forma in funzione dell&#39;input dell&#39;immagine vettoriale.
* **Height**
  * **Regolazione automatica scala Height**: *False/True*\
    Regola automaticamente il height in funzione della scala del pattern per mantenere il height di forme proporzionale al height di sfondo.
  * **Metodo fusione**: *Fusione Height, Test Alpha*\
    Imposta il metodo per risolvere le sovrapposizioni di forme.
  * **Scostamento Height**: *-1,0 - 1,0*\
    Applica uno scostamento globale al height di forme
  * **Scostamento Height casuale**: *0,0 - 1,0*\
    Un moltiplicatore per uno scostamento casuale del height applicato per forma
  * **Moltiplicatore mappa offset Height**: *0.0 - 1.0*\
    Moltiplica lo scostamento del height di forme in funzione del valore in scala di grigio dell’immagine di input.
  * **Scala Height**: *0,0 - 1,0*\
    Consente di controllare la scala del height globale per le forme distribuite
  * **Scala Height casuale**: *0,0 - 1,0*\
    Un moltiplicatore per una scala casuale del height applicata per forma
  * **Moltiplicatore mappa scala Height**: *0,0 - 1,0*\
    Moltiplica la scala del height di forme in funzione del valore di scala di grigi dell’immagine di input.
  * **Conformità allo sfondo**: *0.0 - 1.0*\
    A 0, il height di forme rimane intatto, a 1 il height di forme verrà deformato dallo sfondo del height sottostante.
  * **Sfondo uniforme**: *0.0 - 2.0*\
    Consente di controllare la quantità di arrotondamento applicato alla deformazione del height della forma quando è conforme allo sfondo.
  * **Inclina da Bg Pendenza**: *0.0 - 1.0*\
    Deforma il height di forme in funzione della pendenza del height di sfondo locale: al height di forme viene aggiunta una sfumatura lineare corrispondente alla pendenza di sfondo.
  * **Smoothness Pendenza in background**: *0.0 - 2.0*\
    Controlla l’arrotondamento applicato alla pendenza di sfondo quando la forma viene inclinata in base a tale pendenza.
  * **Ritaglia pixel neri**: *False/True*\
    Ignora il valore del nero dagli input del pattern.
  * **Base motivo unico**: *False/True*\
    Consente di appiattire il height di sfondo sotto una forma corrispondente al height iniziale.
* **Mascheratura**
  * **Maschera casuale**: *0,0 - 1,0*\
    Maschera una quantità casuale di forme, espressa come rapporto della quantità totale.
  * **Moltiplicatore mappa casuale maschera**: *0,0 - 1,0*\
    Imposta la maschera di forma casuale in funzione dell’input dell’immagine in scala di grigio.
  * **Maschera da Bg Pendenza**: *-1.0 - 1.0*\
    Controlla la mascheratura delle forme in base alla pendenza dello sfondo nella loro posizione.
* **Colore**
  * **Regolazione colore**: *-1,0 - 1,0*\
    Consente di regolare globalmente i colori degli elementi sparsi.
  * **Colore casuale**: *0,0 - 1,0*\
    Moltiplicatore per lo spostamento dei valori di colore di una quantità casuale per forma.
  * **Colore di sfondo**: *0.0 - 1.0*\
    Modifica i colori della forma in base al colore dello sfondo nella posizione desiderata.
* **Normale**
  * **Inclina da Bg Pendenza**: *0.0 - 1.0*\
    Inclina la forma normale in base alla normale dello sfondo.
  * **Normale casuale**: *0,0 - 1,0*\
    Moltiplicatore per inclinare la forma normale di una quantità casuale per forma.
  * **Formato normale**: *DirectX, OpenGL*\
    Passare da un Formato mappa normale a un altro (inverte il canale verde)
* **Rugosità**
  * **Regolazione rugosità**: *-1,0 - 1,0*\
    Consente di scostare la rugosità della forma globale.
  * **Rugosità da sfondo**: *0.0 - 1.0*\
    Modifica la rugosità delle forme in base alla ruvidità dello sfondo nella loro posizione.
  * **Rugosità casuale**: *0,0 - 1,0* Un moltiplicatore per lo scostamento della rugosità di una quantità casuale per forma.

## Immagini di esempio

![](../../../../../../assets/atlas-scatter-11.png){width="512px"}

</td>
</tr>
</table>
