---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Usa il nodo Rotazione non uniforme per applicare trasformazioni di rotazione non uniformi per creare effetti a spirale e vortice.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotazione non uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Rotazione non uniforme

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**In:** Filtri*/Trasformazioni*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rotazione non uniforme** ruota l&#39;**Input** utilizzando l&#39;input **Mappa di rotazione**.

I valori dell&#39;immagine rappresentano un *numero di giri*. La rotazione viene eseguita attorno alla posizione specificata dal valore **Posizione dei punti cardini** o dall&#39;input **Mappa Posizione dei punti cardini**.\
I valori positivi nell&#39;input **Mappa di rotazione** generano una rotazione *in senso orario*.

</td>
</tr>
</table>

## Parametri

### Input

* **Input** *Scala di grigi/Colore*\
  Immagine in scala di grigio di input da ruotare.
* **Mappa di rotazione** *Scala di grigi* La mappa utilizzata per controllare la quantità di rotazione, in *numero di giri*. I valori campionati vengono moltiplicati per **il moltiplicatore dell&#39;angolo di rotazione**. I valori negativi generano una rotazione di *senso antiorario*.
* **Mappa Posizione dei punti cardini rotazione** *Colore*\
  Immagine utilizzata per specificare la posizione della rotazione *pivot*. La posizione **X/Y** è mappata ai canali **R/G** dell&#39;immagine.

### Parametri

* **Moltiplicatore Angolo Di Rotazione** *Mobile*\
  Regola l&#39;intensità dell&#39;input **Mappe di rotazione**.
* **Scostamento angolo di rotazione** *Mobile*\
  Applica la quantità di rotazione aggiuntiva specificata.
* **Usa mappa Posizione dei punti cardini** *Booleano*\
  Utilizzare un *input bitmap* per specificare la posizione del perno di rotazione. La posizione **X/Y** è mappata ai canali **R/G** dell&#39;input **Mappa posizione**.
* **Posizione dei punti cardini** *Float2*\
  Posizione del perno attorno al quale viene ruotata l’immagine.
* **Colore di sfondo** *Float/Float4*\
  Colore di sfondo per visualizzare *all&#39;esterno* dei limiti dell&#39;immagine nel caso in cui la suddivisione in porzioni non sia impostata su **H e V in porzioni**.
* **Modalità filtro** *Numero intero*\
  Definisce come trattare i risultati campionati quando *si interpola* tra i pixel:
  * *Più vicino*: verrà campionato esattamente lo *stesso* valore (più veloce)
  * *Bilineare*: applicherà un filtro bilineare sul risultato per un aspetto *più uniforme*

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
