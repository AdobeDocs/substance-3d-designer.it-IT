---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/anisotropic-kuwahara.html"
breadcrumb-title: ''
description: Usate il filtro Anisotropo Kuwahara Color per creare effetti di colore stilizzati e pittorici con arrotondamento direzionale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Anisotropic Kuwahara Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore kuwahara anisotropo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---


# Colore kuwahara anisotropo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Anisotropica Colore Kuwahara](anisotropic-kuwahara.resources/anisotropic-kuwahara-01.png "Icona Anisotropica Colore Kuwahara"){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica una sfocatura direzionale anisotropa conforme ai dettagli dell’immagine. Il risultato è un&#39;immagine che sembra *scorrere* nella direzione delle forme all&#39;interno.

Questa sfocatura regolabile calcola o riceve una *mappa direzionale* per determinare il flusso, che può essere reso più nitido in aree più piatte e definite in modo più chiaro.

Vedere anche: [Scala di grigi Kuwahara anisotropica](../anisotropic-kuwahara-gra/anisotropic-kuwahara-grayscale.md)

</td>
</tr>
</table>

Il flusso può anche essere ridotto ruotando la direzione in cui viene applicata la sfocatura. Allo stesso modo, una mappa direzionale personalizzata può essere utilizzata per ignorare quella calcolata dall’immagine.

Questo filtro può produrre un effetto pittorico ed è utile per la stilizzazione.

+++ Anisotropia

L&#39;intensità del flusso è controllata principalmente dal parametro [Anisotropia](#parameters), come illustrato nell&#39;immagine seguente.

Sinistra: Anisotropia 0.0 / Destra: Anisotropia 1.0

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Una ciotola di frutta con il filtro kuwahara applicato con 0 anisotropia.](anisotropic-kuwahara.resources/anisotropic-kuwahara-02.jpg){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Una ciotola di frutta con il filtro kuwahara applicato con 0 anisotropia.](anisotropic-kuwahara.resources/anisotropic-kuwahara-03.jpg){zoomable="yes"}

</td>
</tr>
</table>

+++

## Input

|                                                   |                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Input</b> <i>Colore</i><br><code>PRIMARIO</code> | Immagine a colori da elaborare. |
| <b>Mappa Angolo di anisotropia</b> <i>Scala di grigi</i> | Immagine in scala di grigio che descrive la rotazione aggiuntiva applicata alla direzione calcolata, in cui il valore della scala di grigio è un numero di giri.   La mappa ha ancora un effetto quando il parametro &#39;Anisotropia&#39; è impostato su 0, in quanto influisce sulla rotazione del kernel utilizzato dal filtro Kuwahara. |
| <b>Pendenza mappa</b> <i>Scala di grigi</i> | La mappa che rappresenta le pendenze a cui è conforme la mappa direzionale, in base al valore del parametro &#39;Pendenza Map Input Multiplier&#39;. |
| <b>Mappa raggio (facoltativa)</b> <i>Scala di grigi</i> | Una volta connesso, il &#39;raggio&#39; della sfocatura viene moltiplicato per l&#39;immagine di input. |
| <b>Mappa direzionale</b> <i>Colore</i> | La mappa che descrive la direzione utilizzata dal kernel filtro anisotropo.   La mappa ha ancora un effetto quando il parametro &#39;Anisotropia&#39; è impostato su 0, in quanto influisce sulla rotazione del kernel utilizzato dal filtro Kuwahara.   Nota: questo input viene utilizzato solo quando il parametro &#39;Usa Mappa direzionale di input&#39; è impostato su &#39;True&#39;. |

## Output

|                                   |                                                                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Output</b> <i>Colore</i> | Risultato della sfocatura anisotropa applicata dal nodo sull&#39;immagine di input. |
| <b>Mappa direzionale</b> <i>Colore</i> | Mappa direzionale calcolata dall’immagine di input e utilizzata per determinare la sfocatura anisotropa.   Se il parametro &#39;Usa Mappa direzionale di input&#39; è impostato su &#39;True&#39;, viene utilizzata l&#39;immagine fornita all&#39;input &#39;Mappa direzionale&#39; e l&#39;output viene eseguito senza modifiche. |

## Parametri

|                                                                                                                              |                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Raggio</b> <i>Virgola mobile</i> | Raggio di sfocatura, dove un valore più alto determina un effetto di sfocatura più forte.   Il valore massimo è 32. |
| <b>Smoothness</b> <i>Virgola mobile</i> | Regola la quantità di fusione dei colori nella direzione calcolata.   Quando questo valore è pari a 0, la maggior parte dei colori viene spostata in quella direzione e la fusione avviene in misura molto ridotta. |
| <b>Nitidezza</b> <i>Mobile</i> | Aumenta il contrasto nelle aree sfocate, rendendole più piatte e definite. |
| <b>Anisotropia</b> <i>Mobile</i> | Regola il contributo della mappa direzionale nella sfocatura.   La mappa direzionale e tutti i suoi modificatori (parametri e mappe di input) hanno ancora un effetto quando questo valore di parametro è 0, poiché la mappa direzionale viene utilizzata nel kernel del filtro Kuwahara. |
| <b>Usa mappa direzionale di input</b> <i>Booleano</i> | Se è impostato su &quot;True&quot;, dall&#39;immagine di input non viene calcolata alcuna mappa direzionale e l&#39;immagine collegata all&#39;input &quot;Mappa direzionale&quot; viene utilizzata per attivare la sfocatura anisotropa. |
| <b>smoothness del tensore</b> <i>Virgola mobile</i><br><br><i>Disponibile quando &#39;Usa mappa direzionale di input&#39; è impostato su &#39;False&#39;</i> | Regola l’intensità della sfocatura applicata alle direzioni calcolate dall’immagine e memorizzate nella mappa direzionale.   Aumentando questo valore si ottiene un risultato più fluido quando l&#39;immagine presenta molti dettagli ad alta frequenza. |
| <b>Angolo di Anisotropia</b> <i>Virgola mobile</i><br><br><i>Disponibile quando &#39;Usa mappa direzionale di input&#39; è impostato su &#39;False&#39;</i> | Aggiunge una rotazione alla mappa direzionale, in numero di giri.   Questa rotazione aggiuntiva è *cumulativa* con quella specificata dall&#39;input &#39;Mappa angolo Anisotropia&#39;. |
| <b>Moltiplicatore mappa angolo Anisotropia</b> <i>Virgola mobile</i><br><br><i>Disponibile quando &#39;Usa mappa direzionale di input&#39; è impostato su &#39;False&#39;</i> | Regola l’intensità dei valori nell’input &quot;Mappa angolo Anisotropia&quot;, che vengono quindi aggiunti al valore della rotazione applicata alla mappa direzionale, in numero di giri.   Questa rotazione aggiuntiva è *cumulativa* con quella specificata dal parametro &#39;Angolo Anisotropia&#39;. |
| <b>Moltiplicatore di input mappa Pendenza</b> <i>Virgola mobile</i><br><br><i>Disponibile quando &#39;Usa mappa direzionale di input&#39; è impostato su &#39;False&#39;</i> | Regola l’intensità con cui la mappa direzionale viene resa conforme alle pendenze fornite dall’input &quot;Mappa Pendenza&quot;. |
| <b>Ignora alfa</b> <i>Booleano</i> | Se è impostato su &quot;True&quot;, il filtro non influisce sul canale alfa dell’immagine.   Se è impostato su &#39;False&#39;, il filtro viene applicato anche al canale alfa. |

## Esempi

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-04.jpg" alt="anisotropic_kuwahara_color_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-05.jpg" alt="anisotropic_kuwahara_color_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-06.jpg" alt="anisotropic_kuwahara_color_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-07.jpg" alt="anisotropic_kuwahara_color_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-08.jpg" alt="anisotropic_kuwahara_color_example_4_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara.resources/anisotropic-kuwahara-09.jpg" alt="anisotropic_kuwahara_color_example_4_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
