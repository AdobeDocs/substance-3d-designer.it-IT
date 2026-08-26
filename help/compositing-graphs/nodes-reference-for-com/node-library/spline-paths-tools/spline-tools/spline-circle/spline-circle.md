---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Utilizzate il nodo Cerchio spline (Spline Circle) per creare spline circolari per generare pattern e forme arrotondate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cerchio spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Cerchio spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-circle-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una singola spline a forma di cerchio.

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

<b>Raggio cerchio</b> *Mobile*\
Regola il raggio del cerchio nello spazio della texture.

<b>Pre-rotazione cerchio</b> *Mobile*\
Applica una rotazione al cerchio di base prima di applicare la dimensione.

<b>Dimensione cerchio</b> *Float2*\
Regola la dimensione orizzontale (X) e verticale (Y) del cerchio.

<b>Cerchio dopo la rotazione</b> *Mobile*\
Applica una rotazione al cerchio di base dopo l’applicazione di Dimensione.

<b>Posizione cerchio</b> *Float2*\
Imposta la posizione del centro del cerchio nello spazio della texture.

<b>Inizia Thickness</b> *Mobile* Regola il thickness del punto iniziale del cerchio.\
Questo thickness viene interpolato lungo la spline fino al Thickness finale.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>Fine Thickness</b> *Mobile* Regola il thickness dell&#39;estremità del cerchio.\
Questo thickness viene interpolato lungo la spline nel Thickness Inizio.\
Nota: il Thickness viene utilizzato da nodi Spline specifici.

<b>Inizia Height</b> *Mobile* Regola il height del punto iniziale del cerchio in cui un valore inferiore indica una posizione più bassa o più profonda.\
Questo height viene interpolato lungo la spline fino al Height finale.

<b>Fine Height</b> *Mobile* Regola il height dell&#39;estremità del cerchio dove un valore più basso indica una posizione più bassa o più profonda.\
Questo height viene interpolato lungo la spline dal Height Inizio.

<b>Taglia</b> *Float2* Sposta i punti iniziale e finale della spline lungo il cerchio.\
Questi valori vengono normalizzati.

<b>Spirale</b> *Mobile* Sposta il punto iniziale del cerchio dal raggio al centro.\
La distanza dal centro viene quindi interpolata lungo la spline fino all&#39;estremità della spline.\
Questo valore è normalizzato.

<b>Cicli a spirale</b> *Mobile* Definisce il numero di giri effettuati dalla spirale attorno al suo centro.

<b>Potenza a spirale</b> *Mobile* Applica una curva di potenza alla distanza dal centro utilizzata per disegnare la spirale.\
Un valore maggiore di uno significa che una porzione maggiore della spirale rimane vicina al centro.

<b>Direzione capovolgimento</b> *Booleano*\
Inverte la direzione della spline.

<b>Distribuzione uniforme</b> *Booleano*\
Se è impostato su True, i punti della spline sono distribuiti uniformemente dall&#39;inizio alla fine.

<b>Aggiungi spline di input</b> *Booleano*\
Aggiunge la spline generata alla fine dell&#39;elenco di spline connesse agli input <b>Spline</b>.

<b>Correzione non quadrata </b>*Booleano* Regola le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

+++Anteprima
<b>Mostra helper direzione</b> *Booleano* Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima.

<b>Mostra busta Thickness</b> *Booleano*\
Visualizza le linee aggiuntive ai bordi del thickness della spline.

<b>Importo segmenti</b> *Numero intero* Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.\
Un valore più alto genera una linea più morbida.

<b>Thickness (px)</b> *Mobile* Regola il thickness in pixel della visualizzazione spline nell&#39;output di anteprima.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/SplineCircle-Variant1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineCircle-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio 3](../../../../../../assets/SplineCircle-Variant2.jpg "Esempio 3")

</td>
<td style="border: 0;" valign="top">

![Esempio 4](../../../../../../assets/SplineCircle-Variant3.jpg "Esempio 4")

</td>
</tr>
</table>
