---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: Utilizzate il nodo Quadratico spline per creare spline quadratiche uniformi con tre punti di controllo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Quadratico)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# Spline (Quadratico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadratic): icon](spline-quadratic.resources/spline-quadratic-icon.png "Spline (Quadratic): icon")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una singola spline tra due punti <b>p1</b> e <b>p3</b> in posizioni arbitrarie.

La traiettoria della spline è controllata dalla tangente &quot;out&quot; di <b>p1</b> e dalla tangente &quot;in&quot; di <b>p3</b>, *entrambe* controllate da un singolo punto <b>p3</b>.

L&#39;estensione dell&#39;arco formato dalla spline è *regolabile*, in modo che parte della traiettoria dalle estremità possa rimanere dritta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Tangenti Z<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di output codificati nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br> - Segno: la spline è chiusa (negativa) o aperta (positiva);<br> - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Tangenti Z<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti direzione</b> <i>Booleano</i> | Inverte la direzione della spline. |
| <b>Distribuzione uniforme</b> <i>Booleano</i> | Se <i>Vero</i>, i punti della spline sono equamente distanziati dall&#39;inizio alla fine. |
| <b>Aggiungi spline di input</b> <i>Booleano</i> | Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline in risoluzioni non quadrate. Questo incide anche sulla distribuzione uniforme. |
| <b>Smoothness</b> <i>Mobile</i> | Regola l&#39;<i>estensione dell&#39;arco</i> formato dalla spline, dove 1 indica che la spline è completamente arcuata e 0 indica che la spline è completamente dritta. L&#39;arco progredisce dal punto <b>p3</b> lungo la spline fino alle estremità. |
| <b>Height</b> |  |
| <b>Inizia height</b> <i>Mobile</i> | Regola il height del punto <b>p1</b> in cui un valore più basso indica una posizione più bassa o più profonda.<br>Questo influisce sul height della spline in <b>p1</b>. |
| <b>Fine height</b> <i>Mobile</i> | Regola il height del punto <b>p3</b> in cui un valore più basso indica una posizione più bassa o più profonda.<br>Questo influisce sul thickness della spline in <b>p3</b>. |
| <b>height tangente automatico</b> <i>Booleano</i> | Regola il height del punto <b>p3</b> in cui un valore più basso indica una posizione più bassa o più profonda.<br>Questo influisce sul thickness della spline in <b>p3</b>. |
| <b>height tangente</b> <i>Mobile</i> | Regola il height in base alle tangenti controllate dal punto <b>p2</b>.<br>Questa impostazione influisce sul height lungo la spline poiché si allontana da <b>p1</b> e si estende a <b>p3</b>.<br><i>Nota:</i> Questo parametro è disponibile solo quando <b>height tangente automatico</b> è impostato su &#39;False&#39;. |
| <b>Thickness</b> |  |
| <b>Inizia thickness</b> <i>Mobile</i> | Regola il thickness del punto <b>p1</b>. Ciò influisce sul thickness della spline in <b>p1</b>.<br><i>Nota:</i> il Thickness viene utilizzato da nodi della spline specifici. |
| <b>Fine thickness</b> <i>Mobile</i> | Regola il thickness del punto <b>p3</b>. Ciò influisce sul thickness della spline in <b>p3</b>.<br><i>Nota:</i> il Thickness viene utilizzato da nodi della spline specifici. |
| <b>thickness tangente automatico</b> <i>Booleano</i> | Imposta automaticamente il thickness delle tangenti della spline per l&#39;interpolazione lineare dal <b>Thickness iniziale</b> al <b>Thickness finale</b>.<br><i>Nota:</i> il Thickness viene utilizzato da nodi della spline specifici. |
| <b>thickness tangente</b> <i>Mobile</i> | Regola il thickness in base alle tangenti controllate dal punto <b>p2</b>.<br>Questa operazione influisce sul thickness lungo la spline poiché si allontana da <b>p1</b> e va in <b>p3</b>.<br><i>Nota:</i> il Thickness viene utilizzato da nodi della spline specifici.<br><i>Nota 2:</i> Questo parametro è disponibile solo quando <b>thickness tangente automatico</b> è impostato su &#39;False&#39;. |
| <b>Coordinate punti</b> |  |
| <b>p1</b> <i>Float2</i> | Imposta la posizione del punto <b>p1</b> nello spazio della texture. |
| <b>p2</b> <i>Float2</i> | Imposta la posizione del punto <b>p2</b> nello spazio della texture.<br>Il punto <b>p2</b> controlla le <i>tangenti</i> di <b>p1</b> e <b>p3</b> punti. |
| <b>p3</b> <i>Float2</i> | Imposta la posizione del punto <b>p3</b> nello spazio della texture. |
| <b>Anteprima</b> |  |
| <b>Mostra tangenti</b> <i>Booleano</i> | Visualizza la tangente &quot;out&quot; del punto <b>p1</b> e la tangente &quot;in&quot; del punto <b>p3</b> nell&#39;output <b>Preview</b>. Inverte la direzione della spline. |
| <b>Mostra helper di direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output <b>Anteprima</b>. |
| <b>Mostra busta thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output <b>Anteprima</b>.<br>Un valore più elevato determina una linea più morbida. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness in pixel della visualizzazione della spline nell&#39;output <b>Anteprima</b>. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Esempio 1](spline-quadratic.resources/spline-quadratic-example-1.png "Spline (Quadratic): Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratic): Esempio 2](spline-quadratic.resources/spline-quadratic-example-2.png "Spline (Quadratic): Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Demo](spline-quadratic.resources/spline-quadratic-demo.gif "Spline (Quadratic): Demo"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
