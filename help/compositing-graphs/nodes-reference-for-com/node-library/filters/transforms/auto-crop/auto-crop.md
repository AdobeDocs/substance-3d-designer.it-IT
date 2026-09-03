---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Utilizzare il nodo Ritaglio automatico per ritagliare automaticamente le texture per rimuovere i bordi vuoti e ottimizzare le dimensioni delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglio automatico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Ritaglio automatico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/auto-crop-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/auto-crop-02.png){width="200px"}

</td>
</tr>
</table>

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Ritaglio automatico** regola l&#39;**Input** in modo che il relativo contenuto venga posizionato al *centro* dell&#39;immagine senza essere ridimensionato oppure *ridimensionato all&#39;estensione* dell&#39;immagine.

Il contenuto dell&#39;immagine è definito da un riquadro adattato al *primo e ultimo pixel* su **X** e **Y**, i cui valori sono *superiori a 0* (ovvero non neri). La versione **Color** consente di scegliere tra RGB e Canali alfa per la definizione della casella.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità</b> <i>Numero intero</i> | Impostate il metodo di ritaglio da applicare:<br><br>- <i>Ritaglia quadrato</i>: l&#39;immagine viene ritagliata in modo che la forma si trovi al centro dell&#39;immagine <i>quadrata</i> più piccola che può includerla completamente<br>- <i>Ritaglia automatica</i>: l&#39;immagine viene ritagliata in modo che la forma si trovi al centro dell&#39;immagine <i>quadrata o non quadrata</i> più piccola che può includerla completamente<br>- <i>Adatta (mantieni proporzioni)</i>: l&#39;immagine viene ridimensionata in base all&#39;<i>estensione completa</i> dell&#39;immagine le sue <i>proporzioni</i> (ovvero il rapporto larghezza/lunghezza)<br>- <i>Riempimento (Allungamento)</i>: l&#39;immagine viene ridimensionata alla <i>estensione completa</i> dell&#39;immagine |
| <b>Usa canale alfa</b> <i>Booleano</i> | Utilizza il canale alfa dell&#39;<b>Input</b> per determinare i <i>limiti</i> del contenuto dell&#39;immagine per il ritaglio. Se impostato su <i>False</i>, vengono utilizzati pixel neri.<br><br><i>Nota:</i> Questo parametro è disponibile solo nella versione <b>Color</b> del nodo. |
| <b>Modalità filtro</b> <i>Numero intero</i> | Definisce come trattare i risultati campionati quando <i>si interpola</i> tra i pixel:<br><br>- <i>Più vicini</i>: verrà campionato esattamente lo <i>stesso</i> valore (più veloce)<br>- <i>Bilineare</i>: verrà applicato un filtro bilineare al risultato per un aspetto <i>più uniforme</i><br>- <i>Automatico</i>: utilizza la modalità più appropriata tra le due precedenti a seconda della <b>Modalità</b> selezionata per il ritaglio |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-06.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-07.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/auto-crop-08.png" />
        </td>
    </tr>
</table>
