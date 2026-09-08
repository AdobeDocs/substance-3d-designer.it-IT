---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/highpass.html"
breadcrumb-title: ''
description: Utilizzate il nodo Passa alte per estrarre dalla texture i dettagli ad alta frequenza e creare effetti di nitidezza e miglioramento dei dettagli.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passa alte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Passa alte

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/high-pass-greyscale.png){width="128px"}

![](../../../../../../assets/high-pass.png){width="128px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue un filtro passa-alto, disponibile sia a colori che in scala di grigio. Simile all’azione Photoshop con lo stesso nome.\
Utile per rimuovere grandi differenze di luminanza nelle immagini, ad Affiancamento quando si rimuovono texture.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Highpass&quot; per gli ingressi del colore e &quot;Highpass Greyscale&quot; per gli ingressi della scala di grigi.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Raggio</b> <i>0.0 - 64.0</i> | Raggio filtro: un raggio piccolo rimuove piccole differenze, un raggio più grande rimuove ampie aree. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/highpass.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/highpass-example.png" />
        </td>
    </tr>
</table>
