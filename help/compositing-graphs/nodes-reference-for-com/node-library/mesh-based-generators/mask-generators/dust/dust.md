---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dust per generare maschere di accumulo dust basate sulla geometria della trama per creare effetti di dust e grigio realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un dust accumulato in aree occluse e in basso, nonché solo in aree rivolte verso l’alto. Richiede che AO e World Space Normals eseguiti i baking correttamente funzionino.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per il posizionamento dei dust. Obbligatorio! |
| <b>Spazio globale normale</b> <i>Input colore</i> | Mappa con baking utilizzata per il posizionamento dei dust. Obbligatorio! |
| <b>Disturbo</b> <i>Input scala di grigi</i> | La mappa dust personalizzata (facoltativa) viene visualizzata solo quando l’opzione Sostituisci disturbo è impostata su True. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta l&#39;importo totale del dust. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del dust. |
| <b>Importo Occlusione</b> <i>0.0 - 1.0</i> | Imposta l’influenza di AO; nelle aree occluse apparirà più dust. |
| <b>Opacità disturbo</b> <i>0.0 - 1.0</i> | Consente di impostare la quantità di disturbo visibile nelle aree polverose. |
| <b>Ignora disturbo</b> <i>Falso/Vero</i> | Impostare questa opzione per utilizzare l&#39;input personalizzato della mappa del dust. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>
