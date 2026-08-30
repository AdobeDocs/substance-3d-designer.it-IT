---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi.resources/voronoi.png){width="200px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Voronoi** genera un disturbo 3D di Voronoi mappato a un&#39;immagine 2D utilizzando una *proiezione ortogonale Z-down*.

Questo nodo può essere testato con [Cubo GBuffer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con *il motore GPU* (ad esempio **Direct** o **OpenGL**). Vai a **Strumenti > Cambia motore...** oppure premi il tasto **F9** per selezionare il motore desiderato.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti</b> <i>Booleano</i> | Inverte l’immagine di output. |
| <b>Scala</b> <i>Mobile</i> | Controlla la scala del rumore di Voronoi.<br><br>*Nota*: quando **Affiancamento** è attivato su *qualsiasi asse*, la regolazione della scala è *graduale*. Questo è previsto. |
| <b>Dimensioni</b> <i>Float3</i> | Controlla la dimensione del disturbo di Voronoi sugli assi **X**, **Y** e **Z**. I valori non uniformi producono un effetto *allungamento o schiacciante*.<br><br>*Nota*: quando l&#39;opzione **Affiancamento** è abilitata su *qualsiasi asse*, la regolazione della dimensione è *graduale*. Questo è previsto. |
| <b>Scostamento</b> <i>Float3</i> | Applica uno scostamento alla *posizione* del rumore di Voronoi sugli assi **X**, **Y** e **Z**. |
| <b>Disturbo</b> <i>Float3</i> | Intensità dello *scostamento casuale* applicato a ciascun punto del disturbo sugli assi **X**, **Y** e **Z**. |
| <b>Intensità Distorsione</b> <i>Mobile</i> | Controlla l&#39;intensità di un *effetto di alterazione* applicato al disturbo di Voronoi. |
| <b>Moltiplicatore scala Distorsione</b> <i>Mobile</i> | Controlla la scala del *pattern di deformazione* utilizzato nell&#39;effetto di alterazione controllato dall&#39;**intensità della Distorsione**. |
| <b>Curva arrotondata</b> <i>Mobile</i> | Arrotonda la *pendenza* attorno a ciascun punto del disturbo per renderlo *convesso*.<br><br>*Nota*: questo parametro non è disponibile quando il parametro **Stile** è impostato su *Bordo*. |
| <b>Scala distanza</b> <i>Mobile</i> | Regola la *distanza della sfumatura* attorno a ciascun punto del disturbo. |
| <b>Modalità distanza</b> <i>Numero intero</i> | Imposta il metodo su *calcolare la sfumatura della distanza* attorno a ciascun punto del disturbo:<br><br>- *euclideo*<br>- *Manhattan*<br>- *Chebyshev*<br>- *Minkowski* |
| <b>Numero di Minkowski</b> <i>Mobile</i> | L&#39;ordine *p* della distanza di Minkowski. Se dividiamo la sfumatura della distanza in quadranti, questo numero influisce su questi quadranti come segue:<br><br>- p è *esattamente* 1: retto<br>- p è *inferiore* a 1: concavo<br>- p è *maggiore* di 1: convesso<br><br>Valori interessanti:<br><br>- *1,0*: distanza di Manhattan<br>- *2,0*: distanza euclidea<br>- *Infinito*: distanza Chebyshev <br><br>*Nota*: questo parametro è disponibile solo quando il parametro **Modalità distanza** è impostato su *Minkowski*. |
| <b>Stile</b> <i>Numero intero</i> | Imposta il metodo *rendering dei dati* del disturbo di Voronoi, considerando che il disturbo si basa su un insieme di punti nello spazio:<br><br>- *F1*: la distanza dal *punto più vicino* nello spazio<br>- *F2*: la distanza dal *secondo punto più vicino* nello spazio<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-* Bordo *: il* bordo tra ogni cella *del disturbo nello spazio<br>-* Colore casuale *: assegna un* colore piatto casuale* a ogni cella del disturbo nello spazio |
| <b>Thickness Edge</b> <i>Mobile</i> | Regola il thickness dei bordi rilevati tra le celle del disturbo di Voronoi. Gli spigoli vengono rilevati negli assi X, Y e Z, pertanto alcuni spessori possono aumentare più rapidamente di altri a seconda della *profondità* delle celle.<br><br>*Nota*: questo parametro è disponibile solo quando il parametro **Stile** è impostato su *Spigolo*. |
| <b>Modalità colore casuale</b> <i>Numero intero</i> | Imposta il metodo di *acquisizione* del valore di inizializzazione casuale per la selezione colore per cella:<br><br>- *Numero casuale globale*: utilizzare il valore di inizializzazione *ereditato* dal nodo<br>- *Numero manuale*: utilizzare un valore di inizializzazione *discreto*<br><br>*Nota*: questo parametro è disponibile solo quando il parametro **Stile** è impostato su *Colore casuale*. |
| <b>Numero di colori casuale</b> <i>Numero intero</i> | Valore di inizializzazione casuale discreto da utilizzare per la selezione del colore per cella.<br><br>*Nota*: questo parametro è disponibile solo quando il parametro **Style** è impostato su *Colore casuale* e il parametro **Modalità di inizializzazione colore casuale** è impostato su ***Numero manuale***. |
| <b>Non square expansion</b> <i>Booleano</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant6.jpg" />
        </td>
    </tr>
</table>
