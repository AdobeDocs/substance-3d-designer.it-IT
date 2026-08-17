---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Utilizzate il nodo Mappatura Flood Fill per mappare i valori tra aree connesse utilizzando algoritmi di riempimento del flusso per l’elaborazione delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---


# Mappatura Flood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

## Mappatura Flood Fill (Scala di grigi)

**Ingresso:** *Filtri/Effetti*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Mappatura Flood Fill consente di rimappare un motivo o una texture esistente su ogni singola cella da un [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). A differenza di altre conversioni di Flood Fill, ad esempio [Scala di grigi casuale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) o [Sfumatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), non genera colori o valori in tinta unita, ma consente di utilizzare mappe di input personalizzate. Può essere visto come una sorta di combinazione di [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) e [Affianca Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) o [Mappatura forme](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), in quanto fornisce alcuni controlli e interfacce simili.

La versione a colori dispone di controlli aggiuntivi per l&#39;utilizzo delle mappe normali, in cui può [compensare le rotazioni delle mappe di norma nello spazio tangente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

## Parametri

### Input

* **Casella di testo Flood Fill**: *Input colore* Input Flood Fill standard, obbligatorio.
* **Input motivo 1-8**: *Input colore/scala di grigi*\
  Inserimento di immagini con pattern personalizzato.
* **Mappa di distribuzione pattern**: *Input in scala di grigi* Mappa ID per determinare il pattern a cui passare la cella. Può derivare da un&#39;altra mappa del Flood Fill, ad esempio da Flood Fill a indice.
* **Mappa scala**: *Input scala di grigi* Mappa per determinare la scala per cella.
* **Mappa di rotazione**: *Input in scala di grigi* Mappa per determinare la rotazione per cella.
* **Mappa scostamento luminanza**: *Input scala di grigi* Mappa per impostare la luminanza per cella

### Parametri

* **Modalità Porzione**: *Nessuna porzione, H+V* Impostare se utilizzare o meno la porzione. Visibile solo se Dimensione o Scala sono impostate su un valore inferiore a 1.
* **Pattern**
  * **Numero di input pattern**: *1 - 8* Impostare la quantità di input pattern personalizzati da utilizzare.
  * **Modalità distribuzione pattern**: *Casuale, dimensioni forma, input mappa distribuzione* Impostare il metodo per determinare il pattern visualizzato in una cella.
  * **Variazione della distribuzione del pattern**: *0.0 - 1.0* Consente una lieve variazione o uno scostamento nella distribuzione del pattern senza modificare tutto attraverso il valore di Numero casuale.
* **Dimensioni**
  * **Modalità dimensioni**: *Rispetto alla texture, Rispetto alla sfera della forma, Rispetto alla forma più grande, Rispetto alla forma più piccola, Adatta casella forma* Impostare la modalità di determinazione della dimensione del pattern in ogni cella.
  * **Dimensioni**: *0.0 - 1.0* Consente il ridimensionamento non uniforme del pattern.
  * **Scala**: *0,0 - 1,0*\
    Impostate la scala globale (uniforme) per l’effetto.
  * **Moltiplicatore mappa scala**: *0.0 - 1.0* Imposta l&#39;influenza della mappa scala facoltativa.
  * **Scala casuale**: *-1,0 - 1,0* Impostate la quantità di variazione casuale all&#39;interno della scala del pattern.
* **Rotazione**
  * **Rotazione**: *0.0 - 1.0* Impostare una rotazione globale e uniforme per ogni cella.
  * **Moltiplicatore Mappa di rotazione**: *0.0 - 1.0* Impostare l&#39;influenza della Mappa di rotazione facoltativa.
  * **Rotazione casuale**: *0,0 - 1,0* Impostare la quantità di rotazione casuale per ogni cella.
  * **Scala automatica rotazione**: *False/True* Impostare se un pattern deve adattarsi a una cella quando viene ruotato.
* **Posizione**
  * **Scostamento posizione**: *0.0 - 1.0* Impostare uno scostamento posizione globale per ogni cella.
  * **Allineamento scostamento posizione**: *Texture, Pattern* Imposta per allineare lo scostamento di 0 punti alla cella Pattern o alla texture.
  * **Scostamento posizione casuale**: *0,0 - 1,0* Impostare la quantità di randomizzazione dello scostamento posizione per cella.
* **Colore** (solo per la versione in scala di grigio)
  * **Intervallo luminanza**: *0.0 - 1.0* Imposta il contrasto globale sulla texture, dove 0 diventa grigio medio.
  * **Intervallo luminanza casuale**: *0.0 - 1.0* Imposta la quantità di randomizzazione per l&#39;Intervallo luminanza.
  * **Scostamento luminanza**: *-1.0 - 1.0* Imposta lo scostamento per la luminanza, fungendo da controllo della luminosità.
  * **Scostamento luminanza casuale**: *0,0 - 1,0* Imposta la quantità di randomizzazione per lo Scostamento luminanza.
  * **Moltiplicatore mappa scostamento luminanza**: *0.0 - 1.0* Imposta l&#39;influenza della mappa opzionale di scostamento luminanza.
  * **Colore sfondo**: *(valore scala di grigio)*Imposta il colore di sfondo su cui vengono fuse le texture.
* **Colore** (solo per la versione a colori)
  * **Mappa normale**: *False/True* Imposta per interpretare l&#39;input del pattern come mappa normale. Compenserà e correggerà la rotazione normale dello spazio tangente.
  * **Formato normale**: *DirectX, OpenGL*\
    Consente di passare da un Formato mappa normale all’altro (inverte il canale verde). Attivo solo quando Is Normal Map è True.
  * **Regolazione HSL**: *-1.0 - 1.0* Regolare HSL a livello globale.
  * **HSL casuale**: *-1.0 - 1.0* Imposta la randomizzazione HSL per cella.
  * **Regolazione dell&#39;Alpha**: *-1.0 - 1.0* Impostate la regolazione dell&#39;Alpha globale, riducendo il contrasto dell&#39;Alpha.
  * **Alpha casuale**: *-1.0 - 1.0* Impostare la randomizzazione della regolazione Alpha per cella.
  * **Colore di sfondo**: *(Valore colore)*Imposta il colore di sfondo su cui vengono fuse le texture.

.

## Immagini di esempio

![](../../../../../../assets/floodfill-mapper-ex01.png)

![](../../../../../../assets/floodfill-mapper-ex02.jpg)

</td>
</tr>
</table>
