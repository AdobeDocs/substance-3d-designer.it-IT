---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spline Cubic per creare spline cubiche uniformi con quattro punti di controllo per tracciati curvi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Cubic)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# Spline (Cubic)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-cubic-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una singola spline tra due punti <b>p1 </b>e <b>p2</b> in posizioni arbitrarie.

La traiettoria della spline è controllata dalla tangente &quot;out&quot; di <b>p1</b> e dalla tangente &quot;in&quot; di <b>p2</b>.

</td>
</tr>
</table>

## Connettori di ingresso

<b>Anteprima</b> *Scala di grigio* Anteprima delle spline di input come immagine in scala di grigio.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:\
<b> R</b> - Posizione X\
<b> G</b> - Posizione Y\
<b> B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.\
<b> R</b> - Tangenti X\
<b> G</b> - Tangenti Y\
<b> B</b> - Non in uso\
<b> A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di input.

## Connettori di uscita

<b>Anteprima</b> *Scala di grigi* Anteprima delle spline di output come immagine in scala di grigi.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Posizione X\
<b>G</b> - Posizione Y\
<b>B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Tangenti X\
<b>G</b> - Tangenti Y\
<b>B</b> - Non utilizzato\
<b>A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di output.

## Parametri

<b>Direzione capovolgimento</b> *Booleano*\
Inverte la direzione della spline.

<b>Aggiungi spline di input</b> *Booleano*\
Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>.

<b>Correzione non quadrata </b>*Booleano* Regola le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

+++Altezza
<b>Inizia Height</b> *Mobile* Regola il height del punto p1 in cui un valore inferiore indica una posizione più bassa o più profonda.\
Questo influisce sul height della spline a p1.

<b>Fine Height</b> *Mobile* Regola il height del punto p2 in cui un valore inferiore indica una posizione più bassa o più profonda.\
Questo influisce sul thickness della spline a p2.

<b>Height tangente automatico</b> *Booleano* Imposta automaticamente il height delle tangenti della spline in modo che si interpolino in modo lineare dal Height iniziale al Height finale.

<b>p1 Height tangente</b> *Float* (disponibile quando &quot;Height tangente automatico&quot; è True)\
Regola il height della tangente &quot;out&quot; del punto p1 in cui un valore inferiore indica una posizione più bassa o più profonda.\
Questo influisce sul height lungo la spline quando si allontana da p1.

<b>Height tangente p2</b> *Float* (disponibile quando &quot;Height tangente automatico&quot; è True)\
Regola il height della tangente &quot;in&quot; del punto p2 in cui un valore inferiore indica una posizione più bassa o più profonda.\
Questo influisce sul height lungo la spline quando si allontana da p2.

+++

+++Spessore
<b>Inizia Thickness</b> *Mobile* Regola il thickness del punto p1.\
Questo influisce sul thickness della spline a p1.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>Fine Thickness</b> *Mobile* Regola il thickness del punto p2.\
Questo influisce sul thickness della spline a p2.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>Thickness tangente automatico</b> *Booleano* Imposta automaticamente il thickness delle tangenti della spline in modo che si interpolino in modo lineare dal Thickness iniziale al Thickness finale.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>p1 Thickness tangente</b> *Float* (disponibile quando &quot;Thickness tangente automatico&quot; è True)\
Regola il thickness della tangente &quot;out&quot; del punto p1.\
Questo influisce sul thickness lungo la spline quando si allontana da p1.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>Thickness tangente p2</b> *Float* (disponibile quando &quot;Thickness tangente automatico&quot; è True)\
Regola il thickness della tangente del punto p2.\
Questo influisce sul thickness lungo la spline quando si allontana da p2.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

+++

+++Coordinate punti
<b>p1</b> *Float2* Imposta la posizione del punto p1 nello spazio della texture.

<b>p1 Tangente</b> *Float2* Imposta la posizione della maniglia tangente del punto p1 &quot;out&quot; nello spazio della texture.

<b>p2</b> *Float2* Imposta la posizione del punto p2 nello spazio della texture.

<b>P2 Tangente</b> *Float2* Imposta la posizione della maniglia tangente &quot;in&quot; del punto p2 nello spazio della texture.

+++

+++Anteprima
<b>Mostra tangenti</b> *Booleano* Visualizza la tangente &quot;out&quot; del punto p1 e la tangente &quot;in&quot; del punto p2 nell&#39;output di anteprima.

<b>Mostra helper direzione</b> *Booleano* Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima.

<b>Importo segmenti</b> *Numero intero* Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.\
Un valore più alto genera una linea più morbida.

<b>Thickness (px)</b> *Mobile* Regola il thickness in pixel della visualizzazione spline nell&#39;output di anteprima.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/SplineCubic-Variant1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineCubic-Variant2.jpg "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 3](../../../../../../assets/SplineCubic-Demo.gif "Esempio di nodo 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
