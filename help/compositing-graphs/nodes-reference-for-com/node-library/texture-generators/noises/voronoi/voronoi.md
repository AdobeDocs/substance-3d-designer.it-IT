---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Utilizza il nodo Voronoi per generare pattern Voronoi per creare trame cellulari ed effetti di materiale organico.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**Ingresso:** *Generatori Di Texture* */Rumori*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Voronoi** genera un disturbo 3D di Voronoi mappato a un&#39;immagine 2D utilizzando una *proiezione ortogonale Z-down*.

Questo nodo può essere testato con [Cubo GBuffer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con *il motore GPU* (ad esempio **Direct** o **OpenGL**). Vai a **Strumenti > Cambia motore...** oppure premi il tasto **F9** per selezionare il motore desiderato.

</td>
</tr>
</table>

## Parametri

* **Inverti** *Booleano*\
  Inverte l’immagine di output.
* **Scala** *Mobile*\
  Controlla la scala del disturbo di Voronoi.\
  *Nota*: quando l&#39;opzione **Affiancatura** è abilitata su *qualsiasi asse*, la regolazione della scala è *graduale*. Questo è previsto.
* **Dimensioni** *Float3*\
  Controlla la dimensione del disturbo di Voronoi sugli assi **X**, **Y** e **Z**. I valori non uniformi producono un effetto *allungamento o schiacciamento*.\
  *Nota*: quando l&#39;opzione **Divisione in porzioni** è abilitata su *qualsiasi asse*, la regolazione della dimensione è *incrementata*. Questo è previsto.
* **Scostamento** *Float3*\
  Applica uno scostamento alla *posizione* del rumore di Voronoi sugli assi **X**, **Y** e **Z**.
* **Disordine** *Float3*\
  Intensità dello *scostamento casuale* applicato a ciascun punto del disturbo sugli assi **X**, **Y** e **Z**.
* **Intensità Distorsione** *Mobile*\
  Controlla l&#39;intensità di un *effetto di alterazione* applicato al disturbo di Voronoi.
* **Moltiplicatore scala Distorsione** *Mobile*\
  Controlla la scala del *pattern di deformazione* utilizzato nell&#39;effetto di alterazione controllato dall&#39;**intensità della Distorsione**.
* **Curva arrotondata** *Mobile*\
  Arrotonda la *pendenza* attorno a ogni punto del disturbo per renderlo *convesso*.\
  *Nota*: questo parametro non è disponibile quando il parametro **Style** è impostato su *Edge*.
* **Scala distanza** *Mobile*\
  Regola la *distanza della sfumatura* attorno a ciascun punto del disturbo.
* **Modalità distanza** *Numero intero*\
  Imposta il metodo su *calcolare la sfumatura della distanza* attorno a ciascun punto del disturbo:
  * *Euclideo*
  * *Manhattan*
  * *Chebyshev*
  * *Minkowski*
* **Numero di Minkowski** *Mobile*\
  L&#39;ordine *p* della distanza di Minkowski. Se dividiamo la sfumatura di distanza in quadranti, questo numero influisce sui quadranti nel modo seguente:
  * p è *esattamente* 1: diritto
  * p è *inferiore* a 1: concavo
  * p è *maggiore* di 1: convesso\
    Valori interessanti:\
    *- 1.0*: distanza Manhattan\
    *- 2.0*: distanza euclidea\
    *- Infinito*: distanza di Chebyshev\
    *Nota*: questo parametro è disponibile solo quando **Modalità distanza** è impostato su *Minkowski*.
* **Style** *Integer* Imposta il metodo *rendering dei dati* del rumore di Voronoi, considerando che il rumore si basa su un insieme di punti nello spazio:
  * *F1*: distanza dal *punto più vicino* nello spazio
  * *F2*: distanza dallo spazio *secondo punto più vicino*
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: il* bordo tra ogni cella* del rumore nello spazio
  * *Colore casuale*: assegna un *colore casuale piatto* a ogni cella del disturbo nello spazio
* **Thickness bordi** *Mobile* Regola il thickness dei bordi rilevati tra le celle del disturbo di Voronoi. I bordi vengono rilevati negli assi X, Y e Z, pertanto alcuni spessori possono aumentare più rapidamente di altri a seconda della *profondità* delle celle.\
  *Nota*: questo parametro è disponibile solo quando il parametro **Style** è impostato su *Edge*.
* **Modalità colore casuale** *Numero intero*\
  Imposta il metodo di *acquisizione* del valore di inizializzazione casuale per la selezione del colore per cella:
  * *Numero casuale globale*: utilizza il valore di inizializzazione *ereditato* dal nodo
  * *Numero di inizializzazione manuale*: utilizzare un valore di inizializzazione *discreto*\
    *Nota*: questo parametro è disponibile solo se **Stile** è impostato su *Colore casuale*.
* **Numero colore casuale** *Numero intero*\
  Seme casuale discreto da utilizzare per la selezione del colore per cella.\
  *Nota*: questo parametro è disponibile solo se il parametro **Style** è impostato su *Colore casuale* e il parametro **Modalità colore casuale** è impostato su ***Numero manuale***.
* **Non square expansion** *Booleano*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
