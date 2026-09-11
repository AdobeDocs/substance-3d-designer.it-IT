---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: Utilizzate il nodo Selezione bordo per generare maschere selezionando i bordi della trama per creare effetti di usura e di resistenza agli agenti atmosferici basati sui bordi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selezione bordo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# Selezione bordo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-select.resources/edge-select.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera è il modo migliore per selezionare qualsiasi tipo di bordo in base alla curvatura. È possibile isolare un oggetto convesso, concavo a qualsiasi livello o contrasto, fornendo una scelta rapida da tastiera eccellente per evitare di farlo manualmente tramite un [nodo Livelli](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per evidenziare i bordi. Obbligatorio! |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta la quantità totale di evidenziazione del bordo per Convesso e Convesso. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto dell’evidenziazione sia per Convesso che per Convesso. |
| <b>Convessa</b> |  |
| <b>Larghezza Bordi Convessi</b> <i>0.0 - 1.0</i> | Imposta la larghezza dell&#39;evidenziazione per i bordi convessi. Tenete presente che aumentando leggermente il valore Morbidezza si possono ottenere bordi più sottili. |
| <b>Morbidezza convessa</b> <i>0.0 - 1.0</i> | Impostate la morbidezza della transizione per i bordi convessi. |
| <b>Intensità convessa</b> <i>0.0 - 1.0</i> | Imposta l&#39;intensità massima dell&#39;evidenziazione del bordo per i bordi convessi. Impostare su 0 per non evidenziare. |
| <b>Concave</b> |  |
| <b>Larghezza bordi concavi</b> <i>0.0 - 1.0</i> | Impostate la larghezza dell&#39;evidenziazione per i bordi concavi. Tenete presente che aumentando leggermente il valore Morbidezza si possono ottenere bordi più sottili. |
| <b>Sfumatura concava</b> <i>0.0 - 1.0</i> | Impostate la morbidezza della transizione per i bordi concavi. |
| <b>Intensità concava</b> <i>0.0 - 1.0</i> | Impostate l&#39;intensità massima dell&#39;evidenziazione dei bordi per i bordi concavi. Impostare su 0 per non evidenziare. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-select.resources/edge-select-ex.gif" />
        </td>
    </tr>
</table>
