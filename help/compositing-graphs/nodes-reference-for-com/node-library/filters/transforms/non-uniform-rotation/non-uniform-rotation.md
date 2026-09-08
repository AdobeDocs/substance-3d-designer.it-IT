---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
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
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Rotazione non uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

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

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rotazione non uniforme** ruota l&#39;**Input** utilizzando l&#39;input **Mappa di rotazione**.

I valori dell&#39;immagine rappresentano un *numero di giri*. La rotazione viene eseguita attorno alla posizione specificata dal valore **Posizione dei punti cardini** o dall&#39;input **Mappa Posizione dei punti cardini**.\
I valori positivi nell&#39;input **Mappa di rotazione** generano una rotazione *in senso orario*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi/Colore</i> | Immagine in scala di grigio di input da ruotare. |
| <b>Mappa di rotazione</b> <i>Scala di grigi</i> | La mappa utilizzata per controllare la quantità di rotazione, in *numero di giri*. I valori campionati vengono moltiplicati per **il moltiplicatore dell&#39;angolo di rotazione**. I valori negativi generano una rotazione di *senso antiorario*. |
| <b>Mappa Posizione dei punti cardini rotazione</b> <i>Colore</i> | Immagine utilizzata per specificare la posizione della rotazione *pivot*. La posizione **X/Y** è mappata ai canali **R/G** dell&#39;immagine. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Moltiplicatore angolo di rotazione</b> <i>Mobile</i> | Regola l&#39;intensità dell&#39;input **Mappe di rotazione**. |
| <b>Scostamento angolo di rotazione</b> <i>Mobile</i> | Applica la quantità di rotazione aggiuntiva specificata. |
| <b>Usa mappa Posizione dei punti cardini</b> <i>Booleano</i> | Utilizzare un *input bitmap* per specificare la posizione del perno di rotazione. La posizione **X/Y** è mappata ai canali **R/G** dell&#39;input **Mappa posizione**. |
| <b>Posizione dei punti cardini</b> <i>Float2</i> | Posizione del perno attorno al quale viene ruotata l’immagine. |
| <b>Colore di sfondo</b> <i>Float/Float4</i> | Colore di sfondo per visualizzare *all&#39;esterno* dei limiti dell&#39;immagine nel caso in cui l&#39;Affiancamento non sia impostato su **Affiancamento H e V**. |
| <b>Modalità filtro</b> <i>Numero intero</i> | Definisce come trattare i risultati campionati quando *si interpola* tra i pixel:<br><br>- *Più vicini*: verrà campionato esattamente lo *stesso* valore (più veloce)<br>- *Bilineare*: verrà applicato un filtro bilineare al risultato per un aspetto *più uniforme* |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonuniformrotation-demo-02-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonuniformrotation-variant-png.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonuniformrotation-node.png" />
        </td>
    </tr>
</table>
