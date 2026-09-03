---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: Utilizzate il nodo Bitmap per importare e utilizzare immagini bitmap come texture nei grafici di composizione delle Substance.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# Bitmap

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Bitmap](bitmap.resources/bitmap-01.png "Nodo atomico: Bitmap"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Carica una [risorsa bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) nel grafico.

Questo nodo viene utilizzato per importare una [bitmap](../../../../glossary/glossary.md) nel grafico oppure per creare una nuova bitmap da utilizzare con gli [strumenti di pittura bitmap](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Esistono alcuni modi per creare questo nodo e tutti richiedono che tu comprenda[la differenza tra il collegamento e l&#39;importazione delle risorse.](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

Potete creare il nodo da zero o rilasciando una [bitmap](../../../../glossary/glossary.md) in un formato supportato nella vista Grafico.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Le bitmap generate o importate a 8 bit possono essere colorate con [strumenti di pittura bitmap](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) nel dock [vista 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Questo nodo dipende da una risorsa esterna, pertanto è necessario tenere presente alcuni punti quando si lavora con queste risorse:
> 
> * I nodi bitmap possono restituire colore o scala di grigi, ma per impostazione predefinita il colore viene applicato anche se la risorsa è una bitmap in scala di grigi. Questo può influire sulle prestazioni e sulla complessità del grafico, quindi assicuratevi sempre di passare al [metodo colore](#parameters) in scala di grigi, se necessario.
> * L&#39;eliminazione di un nodo bitmap non comporta l&#39;eliminazione della [risorsa bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) nel [pacchetto](../../../../glossary/glossary.md). È necessario eseguire questa operazione manualmente in [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md).
> * D&#39;altra parte, prestare attenzione quando si elimina una [risorsa bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) in Esplora risorse: funzionerà ancora nel grafico per quella sessione poiché è mantenuta nella cache, ma la risorsa verrà contrassegnata come mancante al successivo caricamento del [pacchetto](../../../../glossary/glossary.md).
> * Quando un grafico a Substance è [cucinato](../../../../glossary/glossary.md), la risoluzione della bitmap verrà fissata in base alla sua risoluzione all&#39;interno del grafico e non in base alle sue dimensioni originali. Si consiglia di verificare che il parametro &#39;Output size&#39; [base](../../../../glossary/glossary.md) di un nodo Bitmap utilizzi il [metodo di ereditarietà](../../../../glossary/glossary.md) &#39;Absolute&#39; e che il nodo sia seguito da un nodo [Transform 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) impostato su &#39;Relative to parent&#39; (ovvero, la risoluzione del grafico host).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parametri

</td>
<td style="border: 0;" valign="top">

### Strumenti di pittura Bitmap

</td>
<td style="border: 0;" valign="top">

### Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Metodo colore</b> *Booleano* | Determina il tipo di output del nodo da restituire a colori o in scala di grigio. |
| <b>Percorso risorsa PKG</b> *Stringa* | Percorso della risorsa [Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) a cui fa riferimento il nodo.   Si consiglia di non digitare manualmente ma di copiare una risorsa dall&#39;elenco delle cartelle e incollarla nel campo di testo del parametro oppure di trascinare una risorsa bitmap direttamente da [Esplora risorse](../../../../interface/the-explorer-window/the-explorer-window.md) nel nodo Bitmap del grafico. |
| <b>Metodo Resize</b> *Numero intero* | Metodo di ricampionamento da utilizzare per il ridimensionamento verso l’alto o verso il basso di una bitmap:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>allungamento uniforme:</i> applicate un [filtro bilineare](../../../../glossary/glossary.md) per interpolare sui pixel di origine dell&#39;immagine allungamento.</li> <li data-preserve-html="true"><i>allungamento più vicina:</i> Allungamento l&#39;immagine e utilizzate il colore del pixel di origine più vicino così com&#39;è.</li> </ul> |

## Strumenti di pittura Bitmap

Le bitmap possono essere modificate in Designer. Ulteriori informazioni sugli strumenti di modifica in [questa sezione](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
