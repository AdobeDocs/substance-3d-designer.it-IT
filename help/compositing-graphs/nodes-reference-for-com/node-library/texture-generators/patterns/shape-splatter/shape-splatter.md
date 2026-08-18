---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: Utilizzate il nodo Splatter forme per dispersione forme su texture per la creazione di pattern procedurali e dettagli.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spruzzo forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---


# Spruzzo forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter.png){width="128px"}

## Spruzzo forma

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo molto complesso, progettato per essere utilizzato insieme ai nodi [Shape Splatter Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md), [Shape Splatter to Mask](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md) e [Shape Splatter Data Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md). Utilizzato per splattare le forme in modo simile a [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), ma con un processo dinamico e non distruttivo che consente il controllo su ogni passaggio, attraverso un sistema a più livelli simile a [Flood Fill.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) Mentre Flood Fill prende una mappa di input di base da un&#39;origine esterna, Shape Splatter genera la mappa e i dati che ne derivano in un unico passaggio, come una sorta di versione più avanzata di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

Lo scopo principale è quello di consentire il posizionamento di forme su e guidato da una mappa del height e quindi generare varie mappe dai dati di splatter. Ad esempio, posizionare rocce, ramoscelli e foglie su un paesaggio, orientati e guidati da varie mappe. È quindi possibile utilizzare mappe diverse per height, normal, basecolor, rugosità e qualsiasi altro canale, mentre tutte sono ancora basate sugli stessi dati di splatter condivisi.

## Parametri

### Input

* **Height in background**: *Input in scala di grigi* height in background per posizionare le porzioni e attivare vari effetti.
* **Pattern 1-8**: *Input scala di grigi**Pattern facoltativo*
* **Distribuzione pattern**: *Input scala di grigi* Mappa scala di grigi a
* **Scala forme**: *Input scala di grigi* Mappa scala di grigi per il ridimensionamento delle porzioni.
* **Rotazione forma**: *Input scala di grigi* Mappa scala di grigi per guidare la rotazione delle porzioni.
* **Scostamento Height**: *Input scala di grigi* Mappa scala di grigi da utilizzare come scostamento per il height di porzioni.
* **Scala Height**: *Input scala di grigi* Mappa scala di grigi da utilizzare come offset per il height di porzioni.
* **Maschera casuale**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Mappa vettoriale**: *Input colore* Mappa vettoriale colore per guidare il posizionamento e la rotazione del riquadro.

### Parametri

* **Importo X**: *1 - 64*\
  Quantità di X ripetizioni del pattern.
* **Importo Y**: *1 - 64*\
  Quantità di ripetizioni Y del pattern.
* **Pattern**
  * **Numero di input pattern**: *1 - 8* Impostare la quantità di pattern diversi da utilizzare. Sblocca i nuovi slot di input pattern.
  * **Modalità di distribuzione pattern**: *Casuale, Indice pattern, Indice linea, Indice colonna* Impostare come determinare il pattern da utilizzare. In modo casuale o per pattern, linea o colonna.
  * **Moltiplicatore mappa distribuzione pattern**: *0.0 - 1.0* Impostare l&#39;influenza della mappa di distribuzione opzionale per il posizionamento dei pattern.
  * **Rotazione motivo**: *0, 90, 180, 270* Impostazione del predefinito, rotazione a 90 gradi dei motivi.
  * **Rotazione pattern casuale**: *0,0 - 1,0* Impostare la quantità di rotazione a gradino casuale di 90 gradi per i pattern.
* **Dimensioni**
  * **Scala**: *0,0 - 5,0*\
    Impostate la scala uniforme per ogni porzione.
  * **Scala casuale**: *0,0 - 1,0* Scala casuale uniforme per ogni porzione.
  * **Scala senza sovrapposizione**: *0.0 - 1.0* Ridimensiona in modo casuale in modo uniforme, ma solo verso il basso, per evitare la sovrapposizione delle porzioni. Non deve essere usato insieme ai due parametri precedenti.
  * **Moltiplicatore mappa scala**: *0.0 - 1.0* Impostare l&#39;influenza della mappa scala.
  * **Dimensioni**: *0.0 - 1.0* Consente il ridimensionamento non uniforme delle porzioni.
  * **Rapporto dimensioni da Pendenza sfondo**: *0.0 - 1.0* Utilizza la pendenza della mappa di sfondo (Normale calcolato) per le porzioni con scala non uniforme. Simula l’alterazione prospettica.
  * **Rapporto tra dimensioni X/Y**: *0,0 - 1,0* Ridimensionamento non uniforme per compensare un rapporto diverso negli importi X e Y.
* **Posizione**
  * **Posizione casuale**: *0,0 - 2,0* Posizione scostata casualmente per ogni porzione.
  * **Distribuzione casuale**: *Gaussiana, uniforme* Imposta il calcolo da utilizzare per il parametro precedente. Non fa una differenza enorme, più evidente con numeri alti. Il gaussiano tende a dare una diffusione più uniforme.
  * **Moltiplicatore mappa vettoriale**: *0.0 - 1.0* Influenza della mappa di input vettoriale sugli offset.
  * **Scostamento orizzontale**: *-2.0 - 2.0* Scostamento orizzontale globale.
  * **Scostamento verticale**: *-2.0 - 2.0* Scostamento verticale globale.
  * **Opzione Oltre I Limiti**: *Ridimensionare La Forma, Vincolare La Posizione* Azione Da Eseguire Quando Una Sezione Appare Fuori Dai Limiti.
* **Rotazione**
  * **Rotazione**: *0.0 - 1.0* Ruota globalmente tutte le porzioni.
  * **Rotazione casuale**: *0,0 - 1,0* Ruota in modo casuale per porzione.
  * **Rotazione dalla Pendenza Bg**: *0.0 - 1.0* Utilizza la pendenza della mappa di sfondo (Normale calcolato) per ruotare le porzioni. Può essere utilizzato per posizionare le forme in alto o in basso sulle pendenze.
  * **Moltiplicatore Mappa di rotazione**: *0.0 - 1.0* Fusioni nell&#39;effetto della Mappa di rotazione sulla rotazione per porzione.
  * **Moltiplicatore mappa vettoriale**: *0.0 - 1.0* Fusioni nell&#39;effetto della Mappa di rotazione sulla rotazione per porzione.
* **Height**
  * **Regolazione automatica scala Height**: *False/True* Regola automaticamente l&#39;intervallo di height rispetto allo sfondo, anziché definire un intervallo assoluto. Consente un controllo minore o maggiore.
  * **Scostamento Height**: *-1.0 - 1.0* Modificatore per scostare/spostare tutte le porzioni in modo uniforme nell&#39;intervallo del height.
  * **Scostamento Height casuale**: *0,0 - 1,0* Cambia casualmente lo scostamento del height in base ai singoli riquadri.
  * **Moltiplicatore mappa offset Height**: *0.0 - 1.0* Modificatore per impostare l&#39;influenza della mappa di offset.
  * **Scala Height**: *0.0 - 1.0* Modificatore per ridimensionare/espandere tutti i riquadri in modo uniforme nell&#39;intervallo del height. A differenza dello scostamento, questo sposta ulteriormente i valori, come il contrasto.
  * **Scala Height casuale**: *0,0 - 1,0* Modifica casualmente la scala dei height in base ai singoli riquadri.
  * **Moltiplicatore mappa scala Height**: *0.0 - 1.0* Modificatore per impostare l&#39;influenza della mappa scala.
  * **Conformità allo sfondo**: *0.0 - 1.0* Influisce sulla fusione delle porzioni con lo sfondo. Nessuna conformazione significa che le mappe di altezza rimangono rigide, conformazione significa che la forma di sfondo segue. Ideale, ad esempio, per foglie e bastoni.
  * **Sfondo uniforme**: *0.0 - 2.0* Valore di arrotondamento per l&#39;effetto precedente, per evitare variazioni errate o estreme.
  * **Inclina dalla Pendenza Bg**: *0.0 - 1.0* height di sezioni Regola/pendenza guidato dalla pendenza di sfondo (normale calcolato).
  * **Smoothness della Pendenza di sfondo**: *0.0 - 2.0* Valore di arrotondamento per l&#39;effetto precedente, per evitare variazioni errate o estreme.
  * **Ritaglia pixel neri**: *False/True* Attiva/disattiva per ignorare i pixel neri (0) piastrellati dalle forme base dei riquadri.
  * **Base pattern appiattita**: *False/True* Regola il comportamento di fusione delle porzioni con lo sfondo: le porzioni si intersecano con lo sfondo (False) o lo sostituiscono quando sono più basse.
* **Mascheratura**
  * **Maschera casuale**: *0.0 - 1.0* Nasconde casualmente le porzioni. Più alto è questo valore, più porzioni scompariranno.
  * **Moltiplicatore mappa casuale maschera**: *0.0 - 1.0* Soglia per la mappa maschera quando iniziare a nascondere le porzioni.
  * **Maschera da Pendenza sfondo**: *-1.0 - 1.0* Utilizza la pendenza della mappa di sfondo (Normale calcolato) per nascondere le porzioni.

## Immagini di esempio

</td>
</tr>
</table>
