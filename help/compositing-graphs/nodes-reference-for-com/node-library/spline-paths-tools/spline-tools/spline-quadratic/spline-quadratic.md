---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---


# Spline (Quadratico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadratic): icon](../../../../../../assets/spline-quadratic-icon.png "Spline (Quadratic): icon")

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

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Anteprima</b> *Scala di grigi* | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> *Colore* | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori: <b>R</b> - Posizione X <b>G</b> - Posizione Y <b>B</b> - Height <b>A</b> - Dati compressi: - Segno: la spline è chiusa (negativa) o aperta (positiva); - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> *Colore* | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori: <b>R</b> - Tangenti X <b>G</b> - Tangenti Y <b>B</b> - Tangenti Z <b>A</b> - Non utilizzati |
| <b>Quantità spline</b> *Numero intero* | Numero di spline di input. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Anteprima</b> *Scala di grigi* | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> *Colore* | Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori: <b>R</b> - Posizione X <b>G</b> - Posizione Y <b>B</b> - Height <b>A</b> - Dati compressi: - Segno: la spline è chiusa (negativa) o aperta (positiva); - Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> *Colore* | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori: <b>R</b> - Tangenti X <b>G</b> - Tangenti Y <b>B</b> - Tangenti Z <b>A</b> - Non utilizzati |
| <b>Quantità spline</b> *Numero intero* | Numero di spline di output. |

## Parametri

|  |  |
| --- | --- |
| <b>Inverti direzione</b> *Booleano* | Inverte la direzione della spline. |
| <b>Distribuzione uniforme</b> *Booleano* | Se *Vero*, i punti della spline sono equamente distanziati dall&#39;inizio alla fine. |
| <b>Aggiungi spline di input</b> *Booleano* | Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>. |
| <b>Correzione non quadrata</b> *Booleano* | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline in risoluzioni non quadrate. Questo incide anche sulla distribuzione uniforme. |
| <b>Smoothness</b> *Mobile* | Regola l&#39;*estensione dell&#39;arco* formato dalla spline, dove 1 indica che la spline è completamente arcuata e 0 indica che la spline è completamente dritta. L&#39;arco progredisce dal punto <b>p3</b> lungo la spline fino alle estremità. |

+++Altezza

|  |  |
| --- | --- |
| <b>Inizia height</b> *Mobile* | Regola il height del punto <b>p1</b> in cui un valore più basso indica una posizione più bassa o più profonda.  Ciò influisce sul height della spline a <b>p1</b>. |
| <b>Fine height</b> *Mobile* | Regola il height del punto <b>p3</b> in cui un valore più basso indica una posizione più bassa o più profonda.  Ciò influisce sul thickness della spline a <b>p3</b>. |
| <b>height tangente automatico</b> *Booleano* | Regola il height del punto <b>p3</b> in cui un valore più basso indica una posizione più bassa o più profonda.  Ciò influisce sul thickness della spline a <b>p3</b>. |
| <b>height tangente</b> *Mobile* | Regola il height in base alle tangenti controllate dal punto <b>p2</b>.  Ciò influisce sul height lungo la spline che si allontana da <b>p1</b> e va in <b>p3</b>.   *Nota:* questo parametro è disponibile solo quando <b>height tangente automatico</b> è impostato su &#39;False&#39;. |


+++

+++Spessore

|  |  |
| --- | --- |
| <b>Inizia thickness</b> *Mobile* | Regola il thickness del punto <b>p1</b>. Ciò influisce sul thickness della spline a <b>p1</b>.   *Nota: il Thickness* è utilizzato da nodi spline specifici. |
| <b>Fine thickness</b> *Mobile* | Regola il thickness del punto <b>p3</b>. Ciò influisce sul thickness della spline a <b>p3</b>.   *Nota: il Thickness* è utilizzato da nodi spline specifici. |
| <b>thickness tangente automatico</b> *Booleano* | Imposta automaticamente il thickness delle tangenti della spline per l&#39;interpolazione lineare dal <b>Thickness iniziale</b> al <b>Thickness finale</b>.   *Nota: il Thickness* è utilizzato da nodi spline specifici. |
| <b>thickness tangente</b> *Mobile* | Regola il thickness in base alle tangenti controllate dal punto <b>p2</b>.  Ciò influisce sul thickness lungo la spline che si allontana da <b>p1</b> e va in <b>p3</b>.   *Nota: il Thickness* è utilizzato da nodi spline specifici.  *Nota 2:* Questo parametro è disponibile solo quando <b>thickness tangente automatico</b> è impostato su &#39;False&#39;. |


+++

+++Coordinate punti

|  |  |
| --- | --- |
| <b>p1</b> *Float2* | Imposta la posizione del punto <b>p1</b> nello spazio della texture. |
| <b>p2</b> *Float2* | Imposta la posizione del punto <b>p2</b> nello spazio della texture.  Il punto <b>p2</b> controlla le *tangenti* di <b>p1</b> e <b>p3</b> punti. |
| <b>p3</b> *Float2* | Imposta la posizione del punto <b>p3</b> nello spazio della texture. |


+++

+++Anteprima

|  |  |
| --- | --- |
| <b>Mostra tangenti</b> *Booleano* | Visualizza la tangente &quot;out&quot; del punto <b>p1</b> e la tangente &quot;in&quot; del punto <b>p3</b> nell&#39;output <b>Preview</b>.Inverte la direzione della spline. |
| <b>Mostra helper di direzione</b> *Booleano* | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output <b>Anteprima</b>. |
| <b>Mostra busta thickness</b> *Booleano* | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Importo segmenti</b> *Numero intero* | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output <b>Anteprima</b>.  Un valore più alto genera una linea più morbida. |
| <b>Thickness (px)</b> *Mobile* | Regola il thickness in pixel della visualizzazione della spline nell&#39;output <b>Anteprima</b>. |


+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Esempio 1](../../../../../../assets/spline-quadratic-example-1.png "Spline (Quadratic): Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadratic): Esempio 2](../../../../../../assets/spline-quadratic-example-2.png "Spline (Quadratic): Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadratic): Demo](../../../../../../assets/spline-quadratic-demo.gif "Spline (Quadratic): Demo"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
