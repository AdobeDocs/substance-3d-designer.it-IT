---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Usate il nodo Scansione istogramma per eseguire la scansione e l’analisi degli istogrammi delle texture per la correzione e le regolazioni del colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scansione istogramma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# Scansione istogramma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo molto semplice ma utile che fornisce un modo intuitivo per ridefinire il contrasto e la luminosità delle immagini in scala di grigi in ingresso. Può essere utilizzato per &quot;far crescere&quot; e &quot;rimpicciolire&quot; le maschere in modo dinamico.

[Fate clic qui per guardare un video dell’Accademia di Substance sulle operazioni dell’Istogramma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Posizione</b> <i>0.0 - 1.0</i> | Analogamente a un controllo della luminosità, sposta il punto medio del risultato. Quando viene utilizzato su un input sfumatura, questo espande e riduce il punto di transizione.<br><br>Importante: un valore predefinito pari a 0 significa che il risultato finale è sempre nero, quindi prova a iniziare con 0,5! |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. Può essere utilizzato per impostare la durezza della transizione. |
| <b>Inverti posizione</b> <i>Falso/Vero</i> | Inverte il risultato finale. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/histogram-scan3.gif" />
        </td>
    </tr>
</table>
