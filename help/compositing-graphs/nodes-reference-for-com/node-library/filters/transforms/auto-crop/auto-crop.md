---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilizzate il nodo Ritaglio automatico per ritagliare automaticamente le texture in modo da rimuovere i bordi vuoti e ottimizzare le dimensioni della texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglio automatico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Ritaglio automatico

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**In:** Filtri*/Trasformazioni*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Ritaglio automatico** regola l&#39;**Input** in modo che il relativo contenuto venga posizionato al *centro* dell&#39;immagine senza essere ridimensionato oppure *ridimensionato all&#39;estensione* dell&#39;immagine.

Il contenuto dell&#39;immagine è definito da un riquadro adattato al *primo e ultimo pixel* su **X** e **Y**, i cui valori sono *superiori a 0* (ovvero non neri). La versione **Color** consente di scegliere tra i canali RGB e Alpha per la definizione della casella.

</td>
</tr>
</table>

## Parametri

* **Modalità** *Numero intero* Impostare il metodo di ritaglio da applicare:
  * *Ritaglia quadrato*: l&#39;immagine viene ritagliata in modo che la forma si trovi al centro dell&#39;immagine *quadrata* più piccola che può includerla completamente
  * *Ritaglio automatico*: l&#39;immagine viene ritagliata in modo che la forma si trovi al centro dell&#39;immagine *quadrata o non quadrata* più piccola che può includerla completamente
  * *Adatta (mantieni proporzioni)*: l&#39;immagine viene ridimensionata in base all&#39;*intera estensione* dell&#39;immagine mantenendo le *proporzioni* (ovvero il rapporto larghezza/lunghezza)
  * *Riempi (Allunga)*: l&#39;immagine viene ridimensionata nell&#39;*intera estensione* dell&#39;immagine
* **Usa canale alfa** *booleano* Usa il canale alfa dell&#39;**Input** per determinare i *limiti* del contenuto dell&#39;immagine per il ritaglio. Se impostato su *False*, vengono utilizzati pixel neri.\
  *Nota*: questo parametro è disponibile solo nella versione **Color** del nodo.
* **Modalità filtro** *Numero intero* Definisce come trattare i risultati campionati quando *si interpola* tra i pixel:
  * *Più vicino*: verrà campionato esattamente lo *stesso* valore (più veloce)
  * *Bilineare*: applicherà un filtro bilineare sul risultato per un aspetto *più uniforme*
  * *Automatico*: utilizza la modalità più appropriata tra le due a seconda della **Modalità** selezionata per il ritaglio

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
