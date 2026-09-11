---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Usa il nodo Splatter forme per dispersione le forme tra le texture per creare pattern e dettagli procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spruzzo forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# Spruzzo forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo molto complesso, progettato per essere utilizzato insieme ai nodi [Shape Splatter Fusione](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) e [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Utilizzato per splattare le forme in modo simile a [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), ma con un processo dinamico e non distruttivo che consente il controllo su ogni passaggio, attraverso un sistema a più livelli simile a [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Mentre Flood Fill prende una mappa di input di base da un&#39;origine esterna, Shape Splatter genera la mappa e i dati che ne derivano in un unico passaggio, come una sorta di versione più avanzata di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Il suo scopo principale è quello di consentire il posizionamento di forme su e guidate da una mappa di altezza e quindi generare varie mappe dai dati di splatter. Ad esempio, posizionare rocce, ramoscelli e foglie su un paesaggio, orientati e guidati da varie mappe. È quindi possibile utilizzare mappe diverse per height, normal, basecolor, rugosità e qualsiasi altro canale, mentre tutte sono ancora basate sugli stessi dati di splatter condivisi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Height in background</b> <i>Input scala di grigi</i> | Height di sfondo per posizionare le porzioni e attivare vari effetti. |
| <b>Pattern 1-8</b> <i>Input scala di grigi</i> | Pattern facoltativo |
| <b>Distribuzione pattern</b> <i>Input scala di grigi</i> | Mappa scala di grigi a |
| <b>Scala forme</b> <i>Input scala di grigi</i> | Mappa in scala di grigi per applicare la scala ai riquadri. |
| <b>Rotazione forma</b> <i>Input scala di grigi</i> | Mappa in scala di grigi per guidare la rotazione delle porzioni. |
| <b>Scostamento Height</b> <i>Input scala di grigi</i> | Mappa in scala di grigi da utilizzare come scostamento per il height di porzioni. |
| <b>Scala Height</b> <i>Input scala di grigi</i> | Mappa in scala di grigi da utilizzare come scostamento per il height di porzioni. |
| <b>Maschera casuale</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Mappa vettoriale</b> <i>Input colore</i> | Mappa vettoriale colori per guidare il posizionamento e la rotazione delle porzioni. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>X importo</b> <i>1 - 64</i> | Quantità di X ripetizioni del pattern. |
| <b>Importo Y</b> <i>1 - 64</i> | Quantità di ripetizioni Y del pattern. |
| <b>Pattern</b> |  |
| <b>Numero di input del modello</b> <i>1 - 8</i> | Impostate la quantità di pattern diversi da utilizzare. Sblocca i nuovi slot di input pattern. |
| <b>Modalità distribuzione pattern</b> <i>Casuale, Indice motivo, Indice riga, Indice colonna</i> | Impostare come determinare il motivo da utilizzare. In modo casuale o per pattern, linea o colonna. |
| <b>Moltiplicatore mappa distribuzione pattern</b> <i>0.0 - 1.0</i> | Impostate l&#39;influenza della mappa di distribuzione facoltativa per il posizionamento dei pattern. |
| <b>Rotazione motivo</b> <i>0, 90, 180, 270</i> | Imposta il predefinito, rotazione di 90 gradi dei pattern. |
| <b>Rotazione motivo casuale</b> <i>0.0 - 1.0</i> | Impostate la quantità di rotazione casuale a gradino di 90 gradi per i pattern. |
| <b>Dimensioni</b> |  |
| <b>Scala</b> <i>0.0 - 5.0</i> | Impostate la scala uniforme per ogni porzione. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Rendete casuale la scala uniforme per ogni porzione. |
| <b>Scala senza sovrapposizione</b> <i>0.0 - 1.0</i> | Ridimensiona in modo uniforme, ma solo verso il basso, per evitare la sovrapposizione di porzioni. Non deve essere usato insieme ai due parametri precedenti. |
| <b>Moltiplicatore mappa scala</b> <i>0.0 - 1.0</i> | Impostate l&#39;influenza della mappa scala. |
| <b>Dimensioni</b> <i>0.0 - 1.0</i> | Consente il ridimensionamento non uniforme delle porzioni. |
| <b>Rapporto dimensioni da Bg Pendenza</b> <i>0.0 - 1.0</i> | Usa la pendenza della mappa di sfondo (Normale calcolato) per ridimensionare le porzioni in modo non uniforme. Simula l’alterazione della Prospettiva. |
| <b>Dimensioni in base al rapporto di fattore X/Y</b> <i>0.0 - 1.0</i> | Ridimensionamento non uniforme per compensare un rapporto diverso negli importi X e Y. |
| <b>Posizione</b> |  |
| <b>Posizione casuale</b> <i>0.0 - 2.0</i> | Scostamento casuale della posizione per ogni porzione. |
| <b>Distribuzione casuale</b> <i>Gaussiano, Uniforme</i> | Imposta il calcolo da utilizzare per il parametro precedente. Non fa una differenza enorme, più evidente con numeri alti. Il gaussiano tende a dare una diffusione più uniforme. |
| <b>Moltiplicatore mappa vettoriale</b> <i>0.0 - 1.0</i> | Influenza della mappa di input vettoriale sugli offset. |
| <b>Scostamento orizzontale</b> <i>-2.0 - 2.0</i> | Offset orizzontale globale. |
| <b>Scostamento verticale</b> <i>-2.0 - 2.0</i> | Offset verticale globale. |
| <b>Opzione Oltre I Limiti</b> <i>Ridimensiona forma, Vincola posizione</i> | Azione da eseguire quando una porzione appare fuori limite. |
| <b>Rotazione</b> |  |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota tutte le porzioni. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Ruota in modo casuale per porzione. |
| <b>Rotazione da Bg Pendenza</b> <i>0.0 - 1.0</i> | Usa la pendenza della mappa di sfondo (Normale calcolato) per ruotare le porzioni. Può essere utilizzato per posizionare le forme in alto o in basso sulle pendenze. |
| <b>Moltiplicatore Mappa di rotazione</b> <i>0.0 - 1.0</i> | Fusioni dell&#39;effetto della Mappa di rotazione sulla rotazione per porzione. |
| <b>Moltiplicatore mappa vettoriale</b> <i>0.0 - 1.0</i> | Fusioni dell&#39;effetto della Mappa di rotazione sulla rotazione per porzione. |
| <b>Height</b> |  |
| <b>Regolazione automatica scala Height</b> <i>Falso/Vero</i> | Regola automaticamente l’intervallo di height in relazione allo sfondo, invece di definire un intervallo assoluto. Consente un controllo minore o maggiore. |
| <b>Scostamento Height</b> <i>-1.0 - 1.0</i> | Modificatore per scostare/spostare tutte le porzioni in modo uniforme nell’intervallo di height. |
| <b>Scostamento Height casuale</b> <i>0.0 - 1.0</i> | Cambia casualmente lo scostamento del height in base alle porzioni. |
| <b>Moltiplicatore mappa offset Height</b> <i>0.0 - 1.0</i> | Modificatore per impostare l’influenza della mappa di offset. |
| <b>Scala Height</b> <i>0.0 - 1.0</i> | Modificatore per ridimensionare/espandere tutte le porzioni in modo uniforme nell’intervallo di height. A differenza dello scostamento, questo sposta ulteriormente i valori, come il contrasto. |
| <b>Scala Height casuale</b> <i>0.0 - 1.0</i> | Cambia casualmente la scala dei height in base alle porzioni. |
| <b>Moltiplicatore mappa scala Height</b> <i>0.0 - 1.0</i> | Modificatore per impostare l’influenza della Mappa scala. |
| <b>Conformità allo sfondo</b> <i>0.0 - 1.0</i> | Influisce sulla fusione delle porzioni con lo sfondo. Nessuna conformazione significa che le mappe di altezza rimangono rigide, conformazione significa che la forma di sfondo segue. Ideale, ad esempio, per foglie e bastoni. |
| <b>Sfondo uniforme</b> <i>0.0 - 2.0</i> | Valore di arrotondamento per l’effetto precedente, per evitare variazioni errate o estreme. |
| <b>Inclina da Bg Pendenza</b> <i>0.0 - 1.0</i> | Height di riquadri Regola/pendenza guidato da pendenza di sfondo (normale calcolato). |
| <b>Smoothness Pendenza in background</b> <i>0.0 - 2.0</i> | Valore di arrotondamento per l’effetto precedente, per evitare variazioni errate o estreme. |
| <b>Ritaglia pixel neri</b> <i>Falso/Vero</i> | Attivate/disattivate per ignorare i pixel neri (0) interi dalle forme base del riquadro. |
| <b>Base motivo unico</b> <i>Falso/Vero</i> | Regola il comportamento di fusione delle porzioni con lo sfondo: le porzioni si intersecano con lo sfondo (False) o lo sostituiscono quando sono in basso. |
| <b>Mascheratura</b> |  |
| <b>Maschera casuale</b> <i>0.0 - 1.0</i> | Nasconde casualmente le porzioni. Più alto è questo valore, più porzioni scompariranno. |
| <b>Moltiplicatore mappa casuale maschera</b> <i>0.0 - 1.0</i> | Soglia per la mappa maschera quando iniziare a nascondere le porzioni. |
| <b>Maschera da Bg Pendenza</b> <i>-1.0 - 1.0</i> | Usa la pendenza della mappa di sfondo (Normale calcolato) per nascondere le porzioni. |
