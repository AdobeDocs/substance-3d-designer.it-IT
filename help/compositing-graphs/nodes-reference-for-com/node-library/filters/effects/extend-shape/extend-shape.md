---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Usate il nodo di Extend Shape per estendere le forme oltre i loro bordi per creare effetti di maschera e pattern espansi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**In:** filtri*/Effects*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Extend Shape** estende una *sezione* dell&#39;**Input** su una direzione e una distanza impostate.

Il parametro **Mostra helper** consente di visualizzare la direzione della sezione estesa e dell&#39;estensione.

</td>
</tr>
</table>

## Parametri

* **Modalità** *Numero intero* Definisce i *parametri* utilizzati per applicare l&#39;estensione:
  * *Bidirezionale*: la sezione dell&#39;**Input** specificata dalla **Posizione dell&#39;estensione** e dall&#39;**Angolo di estensione** viene estesa oltre la **Distanza dell&#39;estensione** in *direzioni opposte*
  * *Unidirezionale*: la sezione dell&#39;**Input** specificata dalla **Posizione di estensione** e dall&#39;**Angolo di estensione** viene estesa oltre la **Distanza di estensione** in una *direzione singola*
  * *Posizioni iniziale/finale*: un&#39;estensione *vettoriale* è definita da **Posizione iniziale** e **Posizione finale**. La sezione *perpendicolare* dell&#39;**Input** nella **Posizione iniziale** è estesa *su questo vettore* fino alla **Posizione finale**
* **Distanza di estensione** *Mobile* La distanza oltre la quale deve essere estesa la sezione specificata dalla **Posizione di estensione** e dall&#39;**Angolo di estensione**. La distanza viene espressa come *proporzione* dell&#39;estensione dell&#39;immagine.
* **Posizione estensione** *Mobile* Posizione nell&#39;immagine della sezione che deve essere estesa. Il valore viene espresso come *offset dal centro*.
* **Angolo di estensione** *Mobile* L&#39;angolo della sezione che deve essere esteso, considerando il punto di partenza, è una *sezione verticale*.
* **Posizione iniziale** *Float2* Posizione iniziale del *vettore di estensione*.
* **Posizione finale** *Float2* Posizione finale del *vettore di estensione*.
* **Inizia scostamento luminanza** *Mobile* Applica uno scostamento luminanza all&#39;area dell&#39;immagine *che precede* la sezione estesa. Questo scostamento di luminanza è *interpolato lungo la sezione* alla luminanza dell&#39;area dell&#39;immagine che segue la sezione.\
  *Nota*: questo parametro è disponibile solo nella versione **Scala di grigi** del nodo.
* **Scostamento luminanza finale** *Mobile* Applica uno scostamento luminanza all&#39;area dell&#39;immagine *che segue* la sezione estesa. Questo scostamento di luminanza è *interpolato lungo la sezione* alla luminanza dell&#39;area dell&#39;immagine che precede la sezione.\
  *Nota*: questo parametro è disponibile solo nella versione **Scala di grigi** del nodo.
* **Lum. Lo scostamento ignora i pixel neri** *booleani* Se impostato su *Vero*, gli scostamenti di luminanza specificati in *entrambi* **Inizia scostamento luminanza** e **Fine scostamento luminanza** vengono applicati solo a *pixel non neri*, ovvero pixel il cui valore è superiore a 0.\
  *Nota*: questo parametro è disponibile solo nella versione **Scala di grigi** del nodo.
* **Modalità filtro** *Numero intero* Definisce come trattare i risultati campionati quando *si interpola* tra i pixel:
  * *Più vicino*: verrà campionato esattamente lo *stesso* valore (più veloce)
  * *Bilineare*: applicherà un filtro bilineare sul risultato per un aspetto *più uniforme*
* **Mostra helper** *booleano* Visualizza la *sezione estesa* come una sovrapposizione con frecce che mostrano la *direzione* dell&#39;estensione.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
