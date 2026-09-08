---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Usate il nodo Ombra esterna forma per aggiungere effetti di ombra esterna alle forme per creare profondità e dimensione nelle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombra esterna forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Ombra esterna forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue il noto effetto &quot;Ombra esterna&quot; di altri software di elaborazione di immagini 2D su una maschera di input in bianco e nero (per la versione in scala di grigio) o un’immagine con trasparenza (per la versione a colori).

Si differenzia dall&#39;effetto [Ombre](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) in quanto restituisce immagini a cui è stata applicata la trasparenza completa, il che garantisce un effetto più completo simile a quello che ci si aspetterebbe da altri software.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Angolo</b> <i>0.0 - 1.0</i> | Angolo incidenza della luce (falsa). |
| <b>Distanza</b> <i>-0.5 - 0.5</i> | Distanza tra il valore di ombra (drop down) e/o quello di ombra (move away) e la forma. |
| <b>Dimensioni</b> <i>0.0 - 1.0</i> | Controlla la sfocatura/i fuzzine dell’ombra. |
| <b>Pagine affiancate</b> <i>0.0 - 1.0</i> | Taglia/soglia per l’effetto di sfocatura, allontana ulteriormente l’ombra. |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Opacità di fusione per l’effetto ombra. |
| Colore <b>(Ombra)</b> <i>(valore colore)</i> | Tinta di colore da applicare all’ombra. |
| <b>Colore maschera</b> <i>(Valore colore) (Solo versione in scala di grigio)</i> | Tinta unita da utilizzare per l’output con mappatura della trasparenza. |
| <b>Input Premoltiplicato</b> <i>False/True (Solo Versione A Colori)</i> | Indica se l&#39;input deve essere considerato premoltiplicato. |
| <b>Pre-Moltiplica output</b> <i>Falso/Vero</i> | Indica se l&#39;output deve essere premoltiplicato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dropshadowex.png" />
        </td>
    </tr>
</table>
