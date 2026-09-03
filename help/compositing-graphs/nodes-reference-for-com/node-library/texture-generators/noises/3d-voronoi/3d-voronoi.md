---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: Utilizza il nodo Voronoi 3D per generare pattern Voronoi in base alla posizione del mondo 3D per creare texture cellulari volumetriche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# Voronoi 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3d-voronoi-01.png){width="200px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo <b>3D Voronoi</b> genera un rumore Voronoi nello spazio 3D in base all&#39;input <b>Mappa posizione</b>.

Questo nodo può essere testato con [Cubo 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

</td>
</tr>
</table>

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con <i>motore GPU</i> (ad esempio <b>Direct3D</b> o <b>OpenGL</b>). Vai a <b>Strumenti > Cambia motore...</b> oppure premi il tasto <b>F9</b> per selezionare il motore desiderato.

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti</b> <i>Booleano</i> | Inverte l’immagine di output. |
| <b>Scala</b> <i>Mobile</i> | Controlla la scala del disturbo 3D di Voronoi.<br><br><i>Nota</i>: quando <b>Affiancamento</b> è attivato su <i>qualsiasi asse</i>, la regolazione della scala è <i>incrementata</i>. Questo è previsto. |
| <b>Dimensioni</b> <i>Float3</i> | Controlla la dimensione del disturbo 3D di Voronoi sugli assi <b>X</b>, <b>Y</b> e <b>Z</b>. I valori non uniformi producono un effetto <i>allungamento o schiacciante</i>.<br><br><i>Nota</i>: quando l&#39;opzione <b>Affiancamento</b> è abilitata su <i>qualsiasi asse</i>, la regolazione della dimensione è <i>graduale</i>. Questo è previsto. |
| <b>Scostamento</b> <i>Float3</i> | Applica uno scostamento alla <i>posizione</i> del disturbo 3D di Voronoi sugli assi <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Disturbo</b> <i>Float3</i> | Intensità dello <i>scostamento casuale</i> applicato a ciascun punto del disturbo sugli assi <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensità Distorsione</b> <i>Mobile</i> | Controlla l’intensità di un <i>effetto di alterazione</i> applicato al disturbo 3D di Voronoi. |
| <b>Moltiplicatore scala Distorsione</b> <i>Mobile</i> | Controlla la scala del <i>pattern di deformazione</i> utilizzato nell&#39;effetto di alterazione controllato dall&#39;<b>intensità della Distorsione</b>. |
| <b>Curva arrotondata</b> <i>Mobile</i> | Arrotonda la <i>pendenza</i> attorno a ciascun punto del disturbo per renderlo <i>convesso</i>.<br><br><i>Nota</i>: questo parametro non è disponibile quando il parametro <b>Stile</b> è impostato su <i>Bordo</i>. |
| <b>Scala distanza</b> <i>Mobile</i> | Regola la <i>distanza della sfumatura</i> attorno a ciascun punto del disturbo. |
| <b>Modalità distanza</b> <i>Numero intero</i> | Imposta il metodo su <i>calcolare la sfumatura della distanza</i> attorno a ciascun punto del disturbo:<br><br>- <i>euclideo</i><br>- <i>Manhattan</i><br>- <i>Chebyshev</i><br>- <i>Minkowski</i> |
| <b>Numero di Minkowski</b> <i>Mobile</i> | L&#39;ordine <i>p</i> della distanza di Minkowski. Se dividiamo la sfumatura della distanza in quadranti, questo numero influisce su questi quadranti come segue:<br><br>- p è <i>esattamente</i> 1: retto<br>- p è <i>inferiore</i> a 1: concavo<br>- p è <i>maggiore</i> di 1: convesso<br><br>Valori interessanti:<br>- <i>1,0</i>: distanza di Manhattan<br>- <i>2,0</i>: distanza euclidea<br>- <i>Infinito</i>: distanza Chebyshev<br><br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Modalità distanza</b> è impostato su <i>Minkowski</i>. |
| <b>Stile</b> <i>Numero intero</i> | Imposta il metodo <i>rendering dei dati</i> del disturbo 3D di Voronoi, considerando che il disturbo si basa su un insieme di punti nello spazio 3D:<br><br>- <i>F1</i>: la distanza dal <i>punto più vicino</i> nello spazio 3D<br>- <i>F2</i>: la distanza dal <i>secondo punto più vicino</i> nello spazio 3D<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Bordo</i>: il <i>bordo tra ogni cella</i> del disturbo nello spazio 3D<br>- <i>Colore casuale</i>: assegnate un <i>colore piatto casuale</i> a ogni cella del disturbo nello spazio 3D |
| <b>Thickness Edge</b> <i>Mobile</i> | Regola il thickness dei bordi rilevati tra le celle del disturbo 3D di Voronoi. Gli spigoli vengono rilevati negli assi X, Y e Z, pertanto alcuni spessori possono aumentare più rapidamente di altri a seconda della <i>profondità</i> delle celle.<br><br><i>Nota</i>: questo parametro è disponibile solo quando il parametro <b>Stile</b> è impostato su <i>Spigolo</i>. |
| <b>Abilita Affiancamento</b> <i>Booleano</i> | Regola il disturbo 3D di Voronoi in modo che il relativo pattern <i>si ripeta</i> sugli assi X, Y e Z. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-07.jpg" />
        </td>
    </tr>
</table>
