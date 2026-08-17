---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: Usa il nodo del 3D voronoi fractal per generare pattern di Voronoi frattali in base alla posizione 3D per le texture volumetriche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D voronoi fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 0%

---


# 3D voronoi fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal.png){width="200px"}

**Ingresso:** *Generatori Di Texture* */Rumori*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **3D voronoi fractal** genera un disturbo *frattale* di Voronoi nello spazio 3D in base all&#39;input **Mappa posizione**.

Questo nodo può essere testato con [Cubo 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con *motore GPU* (ad esempio **Direct3D** o **OpenGL**). Vai a **Strumenti > Cambia motore...** oppure premi il tasto **F9** per selezionare il motore desiderato.

</td>
</tr>
</table>

## Parametri

* **Inverti** *Booleano*\
  Inverte l’immagine di output.
* **Scala** *Mobile*\
  Controlla la scala del disturbo frattale di Voronoi 3D.\
  *Nota*: quando l&#39;opzione **Affiancatura** è abilitata su *qualsiasi asse*, la regolazione della scala è *graduale*. Questo è previsto.
* **Dimensioni** *Float3*\
  Controlla la dimensione del disturbo frattale di Voronoi 3D negli assi **X**, **Y** e **Z**. I valori non uniformi producono un effetto *allungamento o schiacciamento*.\
  *Nota*: quando l&#39;opzione **Divisione in porzioni** è abilitata su *qualsiasi asse*, la regolazione della dimensione è *incrementata*. Questo è previsto.
* **Scostamento** *Float3*\
  Applica uno scostamento alla *posizione* del disturbo frattale 3D di Voronoi sugli assi **X**, **Y** e **Z**.
* **Disordine** *Float3*\
  Intensità dello *scostamento casuale* applicato a ciascun punto del disturbo sugli assi **X**, **Y** e **Z**.
* **Intensità Distorsione** *Mobile*\
  Controlla l&#39;intensità di un *effetto di alterazione* applicato al disturbo frattale 3D di Voronoi.
* **Moltiplicatore scala Distorsione** *Mobile*\
  Controlla la scala del *pattern di deformazione* utilizzato nell&#39;effetto di alterazione controllato dall&#39;**intensità della Distorsione**.
* **Livello Min** *Intero*\
  Il *livello minimo di ripetizione* utilizzato nel pattern frattale. Un intervallo minimo/massimo più ampio genera un *modello più ricco* con variazione su più intervalli di frequenza.
* **Livello Massimo** *Numero Intero*\
  Il *livello massimo di ripetizione* utilizzato nel pattern frattale. Un intervallo minimo/massimo più ampio genera un *modello più ricco* con variazione su più intervalli di frequenza.
* **Rugosità** *Mobile*\
  Controlla l&#39;*equilibrio* tra *livelli di ripetizione* bassi e alti nel pattern frattale.\
  *Nota*: un valore di **0** genera un output *non in linea* seguito da altri valori bassi. Questo è previsto.\
  *Nota 2*: questo parametro è disponibile solo quando **Metodo fusione** è impostato su *Aggiungi*.
* **Lacunarità** *Galleggiante*\
  Controlla la modalità di riempimento dello spazio del pattern frattale applicato **. Un valore *maggiore* genera *meno spazi vuoti* nel pattern e un disturbo *più denso*.
* **Opacità globale** *Mobile*\
  Controlla l&#39;*intervallo* dei valori di disturbo frattale di Perlin 3D da 0.
* **Curva arrotondata** *Mobile*\
  Arrotonda la *pendenza* attorno a ogni punto del disturbo per renderlo *convesso*.\
  *Nota*: questo parametro non è disponibile quando **Stile** è impostato su *Bordo*.
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
* **Metodo fusione** *Numero intero*\
  Imposta il metodo di fusione dei valori di *celle sovrapposte* nello spazio 3D:
  * *Aggiungi*: aggiungi i valori
  * *Max*: mantieni il valore *più alto*
  * *Min*: mantieni il valore *più basso*
* **Style** *Integer* Imposta il metodo *rendering dei dati* del disturbo frattale di Voronoi 3D, considerando che il disturbo si basa su un insieme di punti nello spazio 3D:
  * *F1*: distanza dal *punto più vicino* nello spazio 3D
  * *F2*: distanza dal *secondo punto più vicino* nello spazio 3D
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Edge *: il* bordo tra ogni cella* del rumore nello spazio 3D
  * *Colore casuale*: assegnate un *colore piatto casuale* a ogni cella del disturbo nello spazio 3D
* **Thickness bordi** *Mobile* Regola il thickness dei bordi rilevati tra le celle del disturbo frattale di Voronoi 3D. I bordi vengono rilevati negli assi X, Y e Z, pertanto alcuni spessori possono aumentare più rapidamente di altri a seconda della *profondità* delle celle.\
  *Nota*: questo parametro è disponibile solo quando il parametro **Style** è impostato su *Edge*.
* **Abilita Porzione** *Booleano*\
  Regola il disturbo frattale di Voronoi 3D in modo che il relativo pattern *si ripeta* sugli assi X, Y e Z.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoifractal-variant3.jpg){width="256px"}

</td>
</tr>
</table>
