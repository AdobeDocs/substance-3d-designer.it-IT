---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Usa il nodo di Atlas scatter per creare texture su un atlas per creare pattern a piastrelle da materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter.png){width="200px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Estrai gli elementi da un Atlas e dispersione sullo sfondo. Gli input di Atlas sono materiali completi, costituiti da singoli elementi disposti e imballati su un singolo foglio di texture. Questo nodo li suddivide (utilizzando un processo [Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md) interno) e li dispersione, in modo simile a [Shape Splatter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). L&#39;Atlas scatter richiede almeno un input mappa opacità e un input mappa altezza affinché l&#39;Atlas funzioni.

</td>
</tr>
</table>

>[!NOTE]
>
> Centinaia di [Atlanti](https://source.substance3d.com/allassets?assetType=substanceAtlas), pronti per essere utilizzati nel nodo Atlas scatter, sono disponibili in [Substance Source](https://source.substance3d.com/).

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Risoluzione input Atlas</b> <i>Risoluzione, da 1 a 12</i> | Impostare manualmente la risoluzione dell&#39;atlas di input completo per garantire un buon rapporto prestazioni/qualità. |
| <b>X importo</b> <i>1 - 64</i> | Quantità di X ripetizioni del pattern. |
| <b>Importo Y</b> <i>1 - 64</i> | Quantità di ripetizioni Y del pattern. |
| <b>Pattern</b> |  |
| <b>Intervallo pattern</b> <i>0 - 10</i> | Definisce l’intervallo di pattern da diffondere. Se impostato su 0, verranno utilizzati tutti i pattern. |
| <b>Modalità distribuzione pattern</b> <i>Casuale, Indice motivo, Indice riga, Indice colonna</i> | Definisce l&#39;ordine in cui vengono utilizzati gli elementi atlas. |
| <b>Moltiplicatore mappa distribuzione pattern</b> <i>0.0 - 1.0</i> | Seleziona il motivo forma in funzione del valore di scala di grigi dell’immagine di input. |
| <b>Rotazione motivo</b> <i>0, 90, 180, 270</i> | Applica una rotazione fissa a ciascun elemento atlante, in base alla quantità di gradi selezionata. |
| <b>Rotazione motivo casuale</b> <i>0.0 - 1.0</i> | Applica una rotazione casuale alla porzione impostata degli elementi atlas. |
| <b>Precisione rilevamento forme atlante</b> <i>Forme semplici o piccole, forme complesse o grandi, nessuna modalità di errore</i> | Imposta la precisione con cui vengono rilevate le forme. Maggiore è la precisione, maggiore sarà l&#39;impatto sulle prestazioni. |
| <b>Riduci opacità atlante (rilevamento più rapido)</b> <i>-4 - 0</i> | Consente di controllare il rapporto di ridimensionamento della mappa di opacità dell&#39;atlante di input, utilizzata per il rilevamento delle forme. Una risoluzione più bassa migliora le prestazioni a costo di precisione. |
| <b>Ignora forma più piccola di</b> <i>0.0 - 1.0</i> | Imposta le dimensioni minime di una forma da rilevare, espresse come rapporto dell&#39;immagine complessiva |
| <b>Dimensioni</b> |  |
| <b>Scala</b> <i>0.0 - 5.0</i> | Imposta la scala relativa delle forme a dispersione. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Definisce il moltiplicatore per l’applicazione del ridimensionamento casuale a ciascuna forma distribuita. |
| <b>Scala senza sovrapposizione</b> <i>0.0 - 1.0</i> | Riduce la scala della forma in modo che non si sovrappongano. |
| <b>Moltiplicatore mappa scala</b> <i>0.0 - 1.0</i> | Moltiplica la scala della forma in funzione del valore di scala di grigi dell’immagine di input. |
| <b>Dimensioni</b> <i>0.0 - 1.0</i> | Imposta la scala relativa delle forme distribuite in base alla lunghezza (X) e alla larghezza (Y). |
| <b>Rapporto dimensioni da Bg Pendenza</b> <i>0.0 - 1.0</i> | Modifica le proporzioni della forma in funzione della pendenza del height di sfondo. |
| <b>Mantieni proporzioni</b> <i>0.0 - 1.0</i> | Determina l’entità di mantenimento delle proporzioni originali delle forme disperse, anziché utilizzare le relative proporzioni delle celle della griglia, ovvero il rapporto tra i valori Quantità X e Quantità Y. |
| <b>Posizione</b> |  |
| <b>Posizione casuale</b> <i>0.0 - 2.0</i> | Moltiplicatore per spostare ogni forma in direzione casuale dal punto iniziale della griglia. |
| <b>Distribuzione casuale</b> <i>Gaussiano, Uniforme</i> | Passa da una distribuzione gaussiana a una distribuzione uniforme per la posizione casuale. La distribuzione gaussiana produrrà un risultato più organico rispetto alla distribuzione uniforme. |
| <b>Moltiplicatore mappa vettoriale</b> <i>0.0 - 1.0</i> | Controlla l&#39;influenza dell&#39;input della mappa vettoriale per spostare le forme nella direzione del vettore specificata dai canali rosso (X) e verde (Y) della mappa. |
| <b>Scostamento orizzontale</b> <i>-2.0 - 2.0</i> | Moltiplicatore per lo scostamento della posizione lungo l&#39;asse X. |
| <b>Scostamento verticale</b> <i>-2.0 - 2.0</i> | Moltiplicatore per lo scostamento della posizione lungo l&#39;asse Y. |
| <b>Opzione Oltre I Limiti</b> <i>Ridimensiona forma, Vincola posizione</i> | A causa della natura tecnica dello splatter, le forme non possono essere disegnate a più di 2 celle di distanza dalla loro posizione originale. Se una forma diventa troppo grande o viene spostata troppo, sono disponibili due opzioni: - Scala forma riduce la dimensione della forma quando raggiunge un limite - Vincola posizione riporta la forma alla posizione originale |
| <b>Rotazione</b> |  |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Consente di controllare la rotazione locale per tutte le forme. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Un moltiplicatore per una quantità casuale di rotazione applicata per forma. |
| <b>Rotazione da Bg Pendenza</b> <i>0.0 - 1.0</i> | Modifica la rotazione della forma in funzione della pendenza del height di sfondo. Generalmente utilizzato in combinazione con il parametro &quot;Rapporto dimensioni da Pendenza di sfondo&quot; |
| <b>Moltiplicatore Mappa di rotazione</b> <i>0.0 - 1.0</i> | Moltiplica la rotazione della forma in funzione del valore di scala di grigi dell’immagine di input. |
| <b>Moltiplicatore mappa vettoriale</b> <i>0.0 - 1.0</i> | Imposta la rotazione della forma in funzione dell&#39;input dell&#39;immagine vettoriale. |
| <b>Height</b> |  |
| <b>Regolazione automatica scala Height</b> <i>Falso/Vero</i> | Regola automaticamente il height in funzione della scala del pattern per mantenere il height di forme proporzionale al height di sfondo. |
| <b>Metodo fusione</b> <i>Fusione Height, test Alpha</i> | Imposta il metodo per risolvere le sovrapposizioni di forme. |
| <b>Scostamento Height</b> <i>-1.0 - 1.0</i> | Applica uno scostamento globale al height di forme |
| <b>Scostamento Height casuale</b> <i>0.0 - 1.0</i> | Un moltiplicatore per uno scostamento casuale del height applicato per forma |
| <b>Moltiplicatore mappa offset Height</b> <i>0.0 - 1.0</i> | Moltiplica lo scostamento del height di forme in funzione del valore in scala di grigio dell’immagine di input. |
| <b>Scala Height</b> <i>0.0 - 1.0</i> | Consente di controllare la scala del height globale per le forme distribuite |
| <b>Scala Height casuale</b> <i>0.0 - 1.0</i> | Un moltiplicatore per una scala casuale del height applicata per forma |
| <b>Moltiplicatore mappa scala Height</b> <i>0.0 - 1.0</i> | Moltiplica la scala del height di forme in funzione del valore di scala di grigi dell’immagine di input. |
| <b>Conformità allo sfondo</b> <i>0.0 - 1.0</i> | A 0, il height di forme rimane intatto, a 1 il height di forme verrà deformato dallo sfondo del height sottostante. |
| <b>Sfondo uniforme</b> <i>0.0 - 2.0</i> | Consente di controllare la quantità di arrotondamento applicato alla deformazione del height della forma quando è conforme allo sfondo. |
| <b>Inclina da Bg Pendenza</b> <i>0.0 - 1.0</i> | Deforma il height di forme in funzione della pendenza del height di sfondo locale: al height di forme viene aggiunta una sfumatura lineare corrispondente alla pendenza di sfondo. |
| <b>Smoothness Pendenza in background</b> <i>0.0 - 2.0</i> | Controlla l’arrotondamento applicato alla pendenza di sfondo quando la forma viene inclinata in base a tale pendenza. |
| <b>Ritaglia pixel neri</b> <i>Falso/Vero</i> | Ignora il valore del nero dagli input del pattern. |
| <b>Base motivo unico</b> <i>Falso/Vero</i> | Consente di appiattire il height di sfondo sotto una forma corrispondente al height iniziale. |
| <b>Mascheratura</b> |  |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | Maschera una quantità casuale di forme, espressa come rapporto della quantità totale. |
| <b>Moltiplicatore mappa casuale maschera</b> <i>0.0 - 1.0</i> | Imposta la maschera di forma casuale in funzione dell’input dell’immagine in scala di grigio. |
| <b>Maschera da Bg Pendenza</b> <i>-1.0 - 1.0</i> | Controlla la mascheratura delle forme in base alla pendenza dello sfondo nella loro posizione. |
| <b>Colore</b> |  |
| <b>Regolazione colore</b> <i>-1.0 - 1.0</i> | Consente di regolare globalmente i colori degli elementi sparsi. |
| <b>Colore casuale</b> <i>0.0 - 1.0</i> | Moltiplicatore per lo spostamento dei valori di colore di una quantità casuale per forma. |
| <b>Colore dallo sfondo</b> <i>0.0 - 1.0</i> | Modifica i colori della forma in base al colore dello sfondo nella posizione desiderata. |
| <b>Normale</b> |  |
| <b>Inclina da Bg Pendenza</b> <i>0.0 - 1.0</i> | Inclina la forma normale in base alla normale dello sfondo. |
| <b>Normale casuale</b> <i>0.0 - 1.0</i> | Moltiplicatore per inclinare la forma normale di una quantità casuale per forma. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passare da un Formato mappa normale a un altro (inverte il canale verde) |
| <b>Rugosità</b> |  |
| <b>Regolazione rugosità</b> <i>-1.0 - 1.0</i> | Consente di scostare la rugosità della forma globale. |
| <b>Rugosità dallo sfondo</b> <i>0.0 - 1.0</i> | Modifica la rugosità delle forme in base alla ruvidità dello sfondo nella loro posizione. |
| <b>Rugosità casuale</b> <i>0.0 - 1.0</i> | Moltiplicatore per lo scostamento della rugosità di una quantità casuale per forma. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-11.png" />
        </td>
    </tr>
</table>
