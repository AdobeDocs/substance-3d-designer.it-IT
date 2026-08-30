---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/triangle-grid.html"
breadcrumb-title: ''
description: Utilizzate il nodo Triangle Grid per generare pattern a griglia triangolare per la creazione di texture geometriche in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Triangle Grid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangle Grid
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---


# Triangle Grid

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](triangle-grid.resources/trianglegridgrayscale.jpg){width="200px"}

![](triangle-grid.resources/trianglegridcolor.jpg){width="200px"}

<b>Ingresso:</b> Generatori texture > Pattern

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Triangle Grid** genera una rappresentazione in scala di grigi di una *superficie triangolata* su *vertici* nello spazio 3D, utilizzando una proiezione ortogonale Z-down.

Il parametro **Output colore** consente di selezionare i dati utilizzati per la rappresentazione, creando vari stili visivi.\
È possibile regolare le *posizioni* dei vertici, che influiscono sulla trama generata.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Height</b> <i>Scala di grigi</i> PRIMARIO | L&#39;input dell&#39;immagine in scala di grigio utilizzato per mappare il *height*, ovvero la posizione Z, dei vertici.    L&#39;influenza di questo input è controllata dal parametro &#39;Moltiplicatore input Height&#39;. |
| <b>Mappa vettoriale</b> <i>Colore</i> | Input dell&#39;immagine a colori utilizzato per mappare lo *spostamento* dei vertici sugli assi X e Y.    Gli scostamenti X/Y vengono mappati rispettivamente ai canali R/G dell’immagine.    L’influenza di questo input è controllata dal parametro &quot;Spostamento mappa vettoriale&quot;. |
| <b>Input colore</b> <i>Colore</i> | L&#39;input dell&#39;immagine a colori utilizzato per mappare il *colore* dei vertici, segmenti o triangoli.    Questo input viene utilizzato quando il parametro &#39;Origine colore&#39; è impostato su &#39;Input colore&#39;. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Immagine di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Output colore</b> *Numero intero* | Metodo di rappresentazione della superficie triangolata:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Per vertice:</b> a ciascun vertice viene assegnato un colore che viene interpolato sulla superficie del triangolo</li> <li data-preserve-html="true"><b>Per triangolo:</b> a ogni triangolo viene assegnato un colore piatto</li> <li data-preserve-html="true"><b>Linea sottile</b><b>:</b> applica un contorno ai segmenti tra vertici</li> <li data-preserve-html="true"><b>Distanza dal bordo</b><b>:</b> esegue il rendering della distanza dal segmento più vicino su ogni triangolo</li> <li data-preserve-html="true"><b>Centro</b><b>:</b> esegue il rendering della distanza normalizzata dal baricentro di ogni triangolo</li> </ul> |
| <b>Triangolazione</b> *Numero intero* | Imposta il metodo di triangolazione per la superficie, ovvero quale *coppia di vertici opposti* in un quadruplo deve essere connessa:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Automatico:</b> seleziona automaticamente la coppia di vertici risultante in triangoli <i>rivolti verso il lato meno distante</i> dalla fotocamera<br/> <b>45°:</b> connettono vertici opposti creando una linea <i>ruotata di 45 gradi</i> rispetto all&#39;asse X-destro</li> <li data-preserve-html="true"><b>-45°:</b> connettono vertici opposti creando una linea <i>ruotata di -45 gradi</i> rispetto all&#39;asse X-destro</li> <li data-preserve-html="true"><b>Quincux orizzontale:</b> alterna l&#39;orientamento della triangolazione <i>ogni altra riga</i> dei vertici</li> <li data-preserve-html="true"><b>Verticale Quincux:</b> alterna l&#39;orientamento della triangolazione <i>ogni altra colonna</i> dei vertici<br/> </li> </ul> |
| <b>X importo</b> *Numero intero* | Quantità di vertici generati sull’asse X. |
| <b>Importo Y</b> *Numero intero* | Quantità di vertici generati sull&#39;asse Y. |
| <b>Moltiplicatore di posizione casuale</b> *Mobile* | Regola l’intensità dell’effetto di alterazione principale. |
| <b>Posizione casuale</b> *Float2* | Regola l&#39;intensità dello scostamento casuale applicato alle posizioni X e Y di ciascun vertice, relativamente alle *dimensioni della rispettiva cella* nella griglia.   Questo offset *si accumula* con <b>Scostamento Quincux</b> e <b>Spostamento mappa vettoriale</b>. |
| <b>Spostamento mappa vettoriale</b> *Mobile* | Regola lo spostamento *globale* applicato a ciascun vertice utilizzando i valori *campionati* dall&#39;input <b>Mappa vettoriale</b>.    Questo scostamento *crea stack* con i parametri <b>Posizione casuale</b> e <b>Scostamento Quincux</b>. |
| <b>Scostamento Quincux X</b> *Mobile* | Applica la quantità di offset specificata a *ogni altra riga* di vertici, relativamente alle *dimensioni della relativa cella* nella griglia.   Questo offset *stacks* con i parametri <b>Posizione casuale</b> e <b>Spostamento mappa vettoriale</b>. |
| <b>Scostamento Quincux Y</b> *Mobile* | Applica la quantità di offset specificata a *ogni altra colonna* di vertici, relativamente alle *dimensioni della relativa cella* nella griglia.    Questo offset *stacks* con i parametri <b>Posizione casuale</b> e <b>Spostamento mappa vettoriale</b>. |
| <b>Rotazione</b> *Mobile* | Applica la quantità di rotazione *specificata* a ciascun vertice attorno alla *posizione di base*, ovvero la posizione *prima* dell&#39;applicazione dello spostamento e dello scostamento casuale.    Questa rotazione *si accumula* con il parametro <b>Disturbo di rotazione</b>. |
| <b>Disturbo della rotazione</b> *Mobile* | Applica un valore *casuale* di rotazione a ciascun vertice attorno alla *posizione di base*, ovvero la posizione *prima* dell&#39;applicazione dello spostamento e dello scostamento casuale.    Questa rotazione *consente di impilare* con il parametro <b>Rotazione</b>. |
| <b>Moltiplicatore di input Height</b> *Mobile* | Regola la posizione Z di ciascun vertice utilizzando i valori *campionati* dall&#39;input <b>Height</b>.    Questo offset *stacks* con il parametro <b>Height casuale</b>. |
| <b>Height casuale</b> *Mobile* | Applica uno scostamento casuale alla posizione Z di ciascun vertice.  Questo offset *stacks* con il parametro <b>Moltiplicatore di input Height</b>. |
| <b>Metodo fusione</b> *Numero intero* | Imposta il metodo di fusione dei valori di *triangoli sovrapposti*. La modalità consente di selezionare *quali* dei triangoli devono essere visibili: <ul data-preserve-html="true"> <li data-preserve-html="true"><b>Min:</b> Testo</li> <li data-preserve-html="true"><b>Massimo:</b> Testo</li> <li data-preserve-html="true"><b>Profondità test</b>: testo</li> <li data-preserve-html="true"><b>Fusione Alpha:</b> Testo</li> </ul>Nota: i metodi di fusione disponibili dipendono dal valore del parametro <b>Output colore</b>. |
| <b>Origine colore</b> *Intero* *Disponibile quando il parametro &#39;Output colore&#39; è impostato su &#39;Per vertice&#39;, &#39;Per triangolo&#39; o &#39;Linea sottile&#39;.* | Imposta il metodo di *acquisizione del colore*, ovvero della luminanza, che deve essere assegnato al vertice, al triangolo o al segmento, a seconda della modalità <b>Output colore</b> selezionata:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Height</b><b>:</b> utilizza il height del vertice come luminanza</li> <li data-preserve-html="true"><b>Casuale</b><b>:</b> utilizza un valore di luminanza casuale</li> <li data-preserve-html="true"><b>Input colore</b><b>:</b> utilizza il valore campionato dall&#39;input <b style="">Input colore</b></li> </ul> |
| <b>Opacità origine colore</b> *Float* *Disponibile quando il parametro &#39;Color Output&#39; è impostato su &#39;Thin Line&#39;.* | Controlla l&#39;*override* del valore <b>Colore linea</b> con i valori risultanti dall&#39;<b>Origine colore</b> selezionata.   Nota: quando questo valore è impostato su 1, il parametro <b>Colore linea</b> non ha alcun impatto. |
| <b>Distanza dal Thickness di bordi</b> *Virgola mobile* *Disponibile quando il parametro &#39;Output colore&#39; è impostato su &#39;Distanza dal bordo&#39;.* | Imposta il thickness della sfumatura della distanza. Un valore inferiore genera una sfumatura *più breve*. |
| <b>Colore linea</b> *Virgola mobile/Virgola mobile 4* *Disponibile quando il parametro &#39;Output colore&#39; è impostato su &#39;Linea sottile&#39;.* | Il valore di luminanza dei segmenti.   Nota: quando il valore <b>Opacità origine colore</b> è impostato su 1, questo parametro non ha alcun impatto. |
| <b>Colore di sfondo</b> *Virgola mobile/Virgola mobile 4* *Disponibile quando il parametro &#39;Output colore&#39; è impostato su &#39;Linea sottile&#39;.* | Luminanza dello sfondo visibile tra i segmenti.   Nota: quando la <b>modalità Fusione</b> è impostata su *Max*, lo sfondo sovrascriverà i segmenti in cui è *più luminoso*, come previsto. |
| <b>Modalità colore casuale</b> *Intero* *Disponibile quando il parametro &#39;Color Output&#39; è impostato su &#39;Per Vertex&#39;, &#39;Per Triangle&#39; o &#39;Thin Line&#39; e il parametro &#39;Color Source&#39; è impostato su &#39;Random&#39;.* | Metodo di acquisizione del seme utilizzato nella distribuzione pseudo-casuale dei colori:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Numero casuale globale</b><b>:</b> eredita il numero dal grafico del nodo</li> <li data-preserve-html="true"><b>Valore di inizializzazione manuale</b><b>:</b> utilizza un valore di inizializzazione discreto personalizzato</li> </ul> |
| <b>Numero di colori casuale</b> *Numero intero* *Disponibile quando il parametro &#39;Metodo di inizializzazione colore casuale&#39; è impostato su &#39;Inizio manuale&#39; e il parametro &#39;Origine colore&#39; è impostato su &#39;Casuale&#39;.* | Valore di inizializzazione discreto utilizzato nella distribuzione pseudo-casuale dei colori. |
| <b>Non square expansion</b> *Booleano* | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 1](triangle-grid.resources/triangle_grid_color_example_1.jpg "Triangle Grid: Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 2](triangle-grid.resources/trianglegrid-variant2.png "Triangle Grid: Esempio 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 3](triangle-grid.resources/trianglegridcolor-variant2.jpg "Triangle Grid: Esempio 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 4](triangle-grid.resources/triangle_grid_color_example_2.jpg "Triangle Grid: Esempio 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 5](triangle-grid.resources/trianglegridcolor-variant4.jpg "Triangle Grid: Esempio 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid: Esempio 6](triangle-grid.resources/trianglegridcolor-variant3.jpg "Triangle Grid: Esempio 6"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid: pelle](triangle-grid.resources/trianglegrid-demo.png "Triangle Grid: pelle"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid: Grafico](triangle-grid.resources/trianglegrid-node.png "Triangle Grid: Grafico"){zoomable="yes"}

</td>
</tr>
</table>
