---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: Utilizzate il nodo Tile Random 2 per creare pattern di riquadri casuali con controlli di variazione avanzati in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Affianca casuale 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---


# Affianca casuale 2

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2.jpg){width="200px"}

**Ingresso:** *Generatori Di Texture* */Pattern*

**Complesso**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Tile Random 2** genera porzioni adiacenti di dimensioni casuali e rapporti height-larghezza.

La griglia può essere modificata *inclinando* casualmente i lati delle forme per suddividere gli angoli.

Le forme possono essere regolate con opzioni per *ridimensionamento*, *smussatura*, *arrotondamento degli angoli* e *rotazione disordinata*.

Queste regolazioni possono essere controllate da *mappe di input*.

Un output dedicato consente di immettere i **UV** della forma in **Flood Fill a (...)** nodi per l&#39;applicazione di variazioni aggiuntive.

</td>
</tr>
</table>

## Parametri

### Input

* **Mappa Dimensione Casuale** *Scala Di Grigi*\
  Immagine di input in scala di grigio che controlla la scala casuale delle forme.\
  Il suo impatto è controllato dal parametro **Moltiplicatore mappa input dimensione casuale**.
* **Mappa inclinata casuale** *Scala di grigio* Immagine di input in scala di grigio che controlla l&#39;inclinazione casuale delle forme.\
  Il suo impatto è controllato dal parametro **Random Slant Input Map Multiplier**.
* **Mappa Raggio Angoli Arrotondati** *Scala Di Grigi*\
  Immagine di input in scala di grigio che controlla il raggio degli angoli arrotondati delle forme.\
  Il suo impatto è controllato dal **mult mappa input raggio angoli arrotondati.** parametro.
* **Mappa di distanza smussata** *Scala di grigi*\
  Immagine di input in scala di grigio che controlla la smussatura delle forme.\
  Il suo impatto è controllato dal **mult mappa input distanza smussata** parametro.
* **Mappa maschera** *Scala di grigi*\
  Immagine di input in scala di grigio che controlla la maschera delle forme.\
  Il suo impatto è controllato dai parametri **Inizio input mappa maschera** e **Fine input mappa maschera**.

### Parametri

* **Importo X** *Intero*\
  Numero di celle sull&#39;asse **X**.
* **Importo Y** *Intero*\
  Numero di celle sull&#39;asse **Y**.
* Dimensioni
  * **Moltiplicatore dimensione casuale** *Mobile*\
    Applica una regolazione *globale* all&#39;intensità del ridimensionamento casuale.
  * **Moltiplicatore mappa di input dimensione casuale** *Mobile*\
    Regola l’intensità del ridimensionamento casuale utilizzando i valori *campionati* dall’input **Mappa dimensioni casuale**.
  * **Dimensione Casuale X** *Mobile*\
    Regola l&#39;intensità del ridimensionamento casuale sull&#39;asse **X** *only*.
  * **Dimensione Casuale Y** *Mobile*\
    Regola l&#39;intensità del ridimensionamento casuale sull&#39;asse **Y** *only*.
  * **Distribuzione casuale delle dimensioni** *Numero intero*\
    Controlla il metodo di distribuzione dei valori di ridimensionamento casuale:
    * *Uniforme*: la scala casuale viene applicata *allo stesso modo* su tutte le celle
    * *Disturbo blu*: la scala casuale è *regolata* utilizzando un pattern di disturbo blu
* Aspetto forma - Trasformazione
  * **Thickness interstizio** *Mobile* Regola il thickness dello spazio tra le forme. È *uguale per tutte* le forme.
  * **Moltiplicatore Di Posizione Casuale** *Mobile*\
    Applica uno scostamento di posizione casuale alla forma fino a *soddisfare il bordo della cella*.
  * **Raggio angoli arrotondati** *Mobile* Regola il *raggio* degli angoli arrotondati delle forme. Un valore di **0** indica che non viene applicato alcun arrotondamento.\
    *Nota*: questo effetto non può essere applicato quando il parametro **Abilita controllo smusso per asse** è impostato su *Vero*.
  * **Mult mappa input raggio angoli arrotondati** *Mobile* Regola l&#39;intensità in base alla quale la mappa di input **Raggio angoli arrotondati** influisce sul raggio degli angoli arrotondati.\
    La mappa funge da moltiplicatore *per pixel* per il parametro **Raggio angoli arrotondati**.\
    *Nota*: questo effetto non può essere applicato quando il parametro **Abilita controllo smusso per asse** è impostato su *Vero*.
  * **Moltiplicatore di scala** *Mobile*\
    Regola le dimensioni di ogni forma in proporzione all&#39;*area della relativa cella*.
  * **Scala casuale** *Mobile* Regola l&#39;intensità in base alla quale viene applicata una scala casuale a *ogni* forma.
  * **Rotazione** *Mobile* Ruota le forme nelle celle spostando ogni *angolo* nel relativo *adiacente* lungo il bordo della cella.\
    Questo metodo determina l&#39;applicazione di *distorsione* e *ridimensionamento* alla forma in corrispondenza della rotazione.
  * **Rotazione casuale** *Mobile* Regola l&#39;intensità in base alla quale viene applicata una quantità casuale di rotazione a ogni forma.\
    Il metodo di rotazione è descritto nel parametro **Rotazione**.
  * **Posizione angoli casuale** *Mobile* Distorce le forme applicando una quantità casuale di *scostamento* a ciascuno dei loro *angoli* lungo il bordo della cella.
* Inclinazione
  * **Moltiplicatore Inclinazione Casuale** *Mobile*\
    Applica una regolazione *globale* all&#39;intensità dell&#39;inclinazione casuale.
  * **Moltiplicatore mappa di input inclinata casuale** *Mobile*\
    Regola l’intensità dell’inclinazione casuale utilizzando i valori *campionati* dall’input **Mappa inclinazione casuale**.
  * **Inclinazione Casuale X** *Mobile*\
    Regola l’intensità dell’inclinazione casuale\
    sull&#39;asse **X** *only*.
  * **Inclinazione Casuale Y** *Mobile*\
    Regola l’intensità dell’inclinazione casuale\
    sull&#39;asse **Y** *only*.
  * **Distribuzione Inclinata Casuale** *Numero Intero*\
    Controlla il metodo di distribuzione dei valori di inclinazione casuale:
    * *Uniforme*: l&#39;inclinazione casuale viene applicata *nello stesso modo* su tutte le celle
    * *Disturbo blu*: l’inclinazione casuale è *regolata* utilizzando un pattern di disturbo blu
* Smusso
  * **Modalità Distanza Smussata** *Numero Intero*\
    Imposta il metodo di *acquisizione della distanza* in base alla quale le forme devono essere smussate:
    * *Rispetto alle dimensioni della griglia*: le forme sono smussate in base alla *proporzione delle dimensioni della griglia* specificata- *Rispetto alle dimensioni della forma*: le forme sono smussate in base alla *proporzione delle dimensioni* specificata
    * *Rispetto alle dimensioni dell&#39;immagine*: le forme sono smussate in base alla *proporzione dell&#39;immagine specificata*
  * **Moltiplicatore Distanza Smussata** *Mobile*\
    Applica una regolazione *globale* alla distanza di smussatura.
  * **Mult mappa input distanza smussata** *Mobile*\
    Regola la distanza di smussatura utilizzando la mappa di input **Mappa di distanza smussata** come moltiplicatore *per pixel*.
  * **Curva arrotondata smussata** *Mobile*\
    Regola l&#39;intensità dell&#39;arrotondamento applicato all&#39;angolo di smussatura per renderla più *convessa*.
  * **Abilita controllo smusso per asse** *Booleano*\
    Se *è True*, è possibile applicare la smussatura e regolarla *separatamente* sugli assi **X** e **Y**.\
    *Nota*: questa operazione *annulla* l&#39;effetto **Angoli arrotondati**.
  * **Distanza Smussata X** *Mobile*\
    Regola la distanza di smussatura sull&#39;asse **X** *only*. Questa distanza dipende dal valore del parametro **Modalità distanza rilievo**.\
    *Nota*: questo parametro è disponibile solo quando il parametro **Abilita controllo smusso per asse** è impostato su *Vero*.
  * **Distanza smussata Y** *Mobile*\
    Regola la distanza di smussatura sull&#39;asse **Y** *only*. Questa distanza dipende dal valore del parametro **Modalità distanza rilievo**.\
    *Nota*: questo parametro è disponibile solo quando il parametro **Abilita controllo smusso per asse** è impostato su *Vero*.
* Maschera
  * **Inversione casuale maschera** *Booleano*\
    Inverte la maschera casuale delle forme.
  * **Inizio casuale maschera** *Mobile*\
    Per un dato **Numero casuale**, la mascheratura pseudo-casuale viene applicata seguendo un *ordine specifico* da una forma iniziale a una forma finale. Questo parametro consente di *spostare l&#39;indice* della forma *start*.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore può quindi essere *maggiore* del valore **Fine casuale maschera**.
  * **Fine casuale maschera** *Mobile* Per un dato **Numero casuale**, la mascheratura pseudo-casuale viene applicata seguendo un *ordine specifico* da una forma iniziale a una forma finale. Questo parametro consente di *scostare l&#39;indice* della forma *end*.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore potrebbe quindi essere *maggiore* del valore **Inizio casuale maschera**.
  * **Maschera per inversione area cella** *Booleano*\
    Inverte la mascheratura delle forme in base all&#39;area delle celle.
  * **Inizio maschera per area cella** *Mobile*\
    Regola la soglia dell&#39;area della cella *minima* per la mascheratura delle forme.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore può quindi essere *maggiore* del valore **Maschera per fine area cella**.
  * **Maschera in base alla fine dell&#39;area della cella** *Mobile* Regola la soglia dell&#39;area della cella *massima* per la mascheratura delle forme.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore potrebbe pertanto essere *inferiore* al valore **Inizio maschera per area cella**.
  * **Inversione input mappa maschera** *Booleano*\
    Inverte la maschera delle forme in base alla mappa di input **Mappa maschera**.
  * **Inizio input mappa maschera** *Mobile*\
    Regola il valore *minimo della scala di grigi* nella mappa di input **Mappa maschera** per le forme di mascheramento.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore può quindi essere *maggiore* del valore **Fine input mappa maschera**.
  * **Fine input mappa maschera** *Mobile* Regola il *valore massimo in scala di grigi* nella mappa di input **Mappa maschera** per la mascheratura delle forme.\
    *Nota*: determina un limite di un *intervallo di valori* per la mascheratura. Il valore potrebbe quindi essere *inferiore* al valore **Inizio input mappa maschera**.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-inputs.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-demo.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-demo2.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/tilerandom2-node.png){width="340px"}

</td>
</tr>
</table>
