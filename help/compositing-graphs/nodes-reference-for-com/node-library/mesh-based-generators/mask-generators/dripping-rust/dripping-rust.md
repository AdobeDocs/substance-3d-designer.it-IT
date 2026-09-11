---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Utilizzate il nodo Ruggine di gocciolamento (Dripping) per generare serie di gocce di ruggine in base alla geometria della trama e alla direzione della gravità.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruggine gocciolante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# Ruggine gocciolante

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta scaglie e chiazze di ruggine, con perdite che scorrono.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa eseguita i baking o generata per facilitare il posizionamento della ruggine. |
| <b>Occlusione ambientale</b> <i>Input scala di grigi</i> | Mappa eseguita i baking o generata per facilitare il posizionamento della ruggine. |
| <b>Posizione</b> <i>Input scala di grigi</i> | Mappa eseguita i baking o generata per le direzioni di goccia. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Ruggine diffusione</b> <i>0.0 - 1.0</i> | Controllo principale della quantità di ruggine. |
| <b>Ruggine contrasto</b> <i>0.0 - 1.0</i> | Consente di impostare il livello di contrasto nelle chiazze di ruggine generate (non influisce sulle gocce). |
| <b>Diffusione Smoothness</b> <i>0.0 - 1.0</i> | Entità dell’effetto di sfocatura/sbavatura da applicare alle macchie della ruggine. |
| <b>Intensità gocce</b> <i>0.0 - 1.0</i> | Imposta l’intensità e la lunghezza delle gocce dai difetti. |
| <b>Gocce di Smoothness</b> <i>0.0 - 1.0</i> | Quantità di sfocatura e attenuazione da applicare alle gocce. |
| <b>Quantità campioni gocce</b> <i>0 - 32</i> | Imposta il livello di qualità (passi) per l’effetto gocce. Ha un leggero effetto sulla velocità. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
