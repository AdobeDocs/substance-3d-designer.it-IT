---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Utilizzate il nodo Pennello superficie (Surface Brush) per generare maschere basate sull'orientamento della superficie e creare così effetti di usura e meteorologia direzionali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pennello superficie
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---


# Pennello superficie

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un effetto interessante del pennello metallico sulla superficie di un oggetto, occluso dalla geometria dell&#39;oggetto e da AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Spazio globale normale</b> <i>Input colore</i> |  |
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Posizione</b> <i>Input scala di grigi</i> |  |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta il livello dell’effetto globale, rivelandolo gradualmente. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Durata Scratches</b> <i>0.0 - 8.0</i> | Consente di impostare la lunghezza dei graffi. I valori più piccoli somigliano di più ai punti, mentre quelli più alti sono striature lunghe. |
| <b>Occludi asse</b> <i>X, Y, Z, nessuno</i> | Asse dell’oggetto che deve ricevere i graffi. Non modifica la direzione dei graffi. |
| <b>Intensità asse occlusivo</b> <i>0.0 - 1.0</i> | Intensità dell’effetto occlusione asse. |
| <b>Occlusione</b> <i>0.0 - 1.0</i> | Intensità dell’AO sui graffi occlusivi. |
| <b>Intensità nitidezza</b> <i>0.0 - 1.0</i> | Impostate la quantità di post-nitidezza da applicare ai graffi. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-ex.gif" />
        </td>
    </tr>
</table>
