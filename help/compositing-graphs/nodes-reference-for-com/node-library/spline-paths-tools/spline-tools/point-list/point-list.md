---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Utilizzare il nodo Elenco punti per creare e gestire elenchi di punti per la generazione di spline e percorsi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elenco punti
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Elenco punti

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/point-list-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera un elenco di punti attraversati da una spline.

Se agli input di <b>Point</b> viene fornito un elenco di punti esistente, l&#39;elenco generato viene aggiunto all&#39;elenco di input.

</td>
</tr>
</table>

>[!TIP]
>
> Questo nodo può essere utilizzato per fornire punti al nodo [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) per generare spline.

>[!IMPORTANT]
>
> I connettori <b>Elenco punti</b> e <b>Numero punto</b> sono *incompatibili* con <b>Coord spline</b>, <b>Dati spline</b> e <b>Quantità spline</b>, in quanto si basano su dati diversi.

## Connettori di ingresso

<b>Anteprima </b>*Scala di grigio* Anteprima dei punti come immagine in scala di grigio.

<b>Input elenco punti</b> *Colore*\
Elenco dei punti di input codificati nei canali RGBA di un’immagine a colori:\
    <b>R</b> - Posizione X\
    <b>G</b> - Posizione Y\
    <b>B</b> - Height\
    <b>A</b> - Dati compressi:\
            * Parte intera: Smoothness;\
            * Parte frazionaria: Thickness.

<b>Input numero punto</b> *Numero intero*\
Numero di punti di input.

## Connettori di uscita

<b>Anteprima </b>*Scala di grigio* Anteprima dei punti come immagine in scala di grigio.

<b>Elenco punti </b>*Colore*\
Elenco di output dei punti codificati nei canali RGBA di un’immagine a colori:\
    <b>R</b> - Posizione X\
    <b>G</b> - Posizione Y\
    <b>B</b> - Height\
    <b>A</b> - Dati compressi:\
            * Parte intera: Smoothness;\
            * Parte frazionaria: Thickness.

<b>Numero punto </b>*Numero intero*\
Numero di punti di output.

## Parametri

<b>Numero punto</b> *Numero intero* Numero di punti generati.

<b>Regolazione Smoothness globale</b> *Mobile* Applica un offset uniforme al valore di smoothness di tutti i punti.\
Il valore di smoothness risultante viene fissato all&#39;intervallo [0;1].

+++Proprietà punti
<b>p# Proprietà</b> *Float3* Imposta le proprietà del punto p#.\
*- Height:* regola il height del punto in cui un valore inferiore indica una posizione inferiore o più profonda;\
*- Smoothness:* Sposta l&#39;inizio dell&#39;attenuazione della spline a p#, dove un valore pari a 0 determina una traiettoria rigida e 1 una traiettoria completamente liscia;\
*- Thickness:* Regola il thickness della spline a p#. Thickness viene utilizzato da nodi Spline specifici.

+++

+++Coordinate punti
<b>p#</b> *Float2* Imposta la posizione del punto p# nello spazio della texture.

+++

+++Anteprima
<b>Mostra etichette</b> *Booleano*\
Per ogni punto, visualizza il nome del punto accanto nell&#39;output &quot;Anteprima&quot;.

<b>Dimensione etichetta</b> *Mobile* (disponibile quando &#39;Mostra etichette&#39; è impostato su &#39;True&#39;)\
Dimensione dell’etichetta per ogni punto nello spazio della texture, dove 0,1 è un decimo della larghezza della texture.

<b>Mostra punti</b> *Booleano*\
Visualizza i punti nell&#39;output &quot;Preview&quot;.

<b>Dimensioni punti</b> *Mobile* (disponibile quando &#39;Mostra punti&#39; è impostato su &#39;True&#39;)\
Raggio dei punti nello spazio della texture, dove 0,1 è un decimo della larghezza della texture.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/PointList-Variant1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/PointList-Demo1.gif "Esempio di nodo 2")

</td>
</tr>
</table>
