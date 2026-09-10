---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dirt per generare maschere di accumulo dirt in base alla curvatura, alla posizione e all'occlusione della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Terra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# Terra

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta i dirt in bordi e angoli occlusi e incassati, in base all&#39;AO eseguito i baking e alla curvatura.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. Obbligatorio! |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. Obbligatorio! |
| <b>input Grunge</b> <i>Input scala di grigi</i> | Input mappa grunge personalizzata, facoltativo, abilitato dal parametro. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Spazio globale normale</b> <i>Input colore</i> | Utilizzato solo per Triplanare. |
| <b>Posizione</b> <i>Input colore</i> | Utilizzato solo per Triplanare. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello Dirt</b> <i>0.0 - 1.0</i> | Controllo principale per la quantità di dirt. |
| <b>Contrasto Dirt</b> <i>0.0 - 1.0</i> | Controlla il contrasto principale per il dirt nella maschera. |
| <b>Importo Grungi</b> <i>0.0 - 1.0</i> | Imposta il grado di grunge del dirt. Impostate su 0 per un dirt perfettamente uniforme. |
| <b>Mascheratura bordi</b> <i>0.0 - 1.0</i> | Quantità di dirt da rimuovere dai bordi in rilievo (in base alla mappa di curvatura). |
| <b>Usa Grunge personalizzata</b> <i>Falso/Vero</i> | Consente l&#39;utilizzo di un input di mappa grunge personalizzato anziché di una Grunge incorporata. |
| <b>Scala Grungi</b> <i>1 - 16</i> | Imposta la scala Affiancamento dei dettagli della Grunge. |
| <b>Usa Triplanare</b> <i>Falso/Vero</i> | Usa [Proiezione triplanare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) per la mappatura delle Grungi e rimuove le giunture. |
| <b>Contrasto di fusione triplanare</b> <i>0.001 - 1.0</i> | Imposta il contrasto della proiezione triplanare. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>
