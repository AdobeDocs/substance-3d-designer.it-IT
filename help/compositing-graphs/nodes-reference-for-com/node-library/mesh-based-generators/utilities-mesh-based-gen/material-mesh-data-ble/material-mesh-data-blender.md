---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Utilizzate il nodo Miscelatore dati mesh materiale (Material Mesh Data Blender) per fondere i dati della mesh del materiale e creare transizioni uniformi tra le diverse zone materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Miscelatore dati mesh materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# Miscelatore dati mesh materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Utility

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo ha lo scopo di semplificare notevolmente l&#39;aggiunta di dettagli in base ai dati elaborati. Viene fornito con molti cursori per modificare un materiale completo di input, basato su qualsiasi e tutte le mappe con baking come input. Sperimenta, dato che ci sono molte opzioni.

È utile ad esempio per aggiungere l’evidenziazione dei bordi in base alla curvatura o ad altre mappe, eseguire la fusione in alcuni oggetti AO con Diffusione/Colore di base, aggiungere Occlusioni di Specular basate su Curvatura e/o AO, ecc.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input materiale completo (gruppo &quot;Materiale&quot;)</b> | Set completo di mappe di materiale.<br><br>Questi elementi sono stati modificati da questo nodo e sono stati restituiti come output. |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Height</b> <i>Input scala di grigi</i> |  |
| <b>Normale</b> <i>Input colore</i> |  |
| <b>Colore vertice</b> <i>Input colore</i> |  |
| <b>Spazio globale normale</b> <i>Input colore</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. Influisce sulla disponibilità dei parametri seguenti. |
| <b>Mappe con baking</b> | Indica se utilizzare o meno le mappe con baking elencate per i calcoli. Influisce sulla disponibilità dei parametri seguenti. |
| <b>Diffusa AO</b> <i>0.0 - 1.0</i> | Quantità di Occlusione ambientale da fondere nella Diffusa. |
| <b>Bordi Netti Diffusa</b> <i>0.0 - 1.0</i> | Quantità della mappa di curvatura da fondere con Diffusione. |
| <b>Colore Diffusa Da Colore Vertice</b> <i>0.0 - 1.0</i> | Quantità del Color Bake Vertice da fondere con Diffusione. |
| <b>Pre-illuminazione Diffusa</b> <i>0.0 - 1.0</i> | Quantità di (falsa) pre-illuminazione, in base ai World Space Normals. |
| <b>Bilanciamento illuminazione cartone animato Diffusa</b> <i>0.0 - 1.0</i> | Si sposta tra un’illuminazione realistica e in stile cartone animato per Diffusione. |
| <b>Livelli di pre-illuminazione per cartone animato Diffusa</b> <i>0 - 10</i> | Controlla l’aspetto dei calcoli di illuminazione per i cartoni animati. |
| <b>Contorni cartone animato Diffusa</b> <i>0.0 - 1.0</i> | Controlla l’aspetto dei calcoli di illuminazione per i cartoni animati. |
| <b>Colore di base AO</b> <i>0.0 - 1.0</i> | Quantità di Occlusione ambiente da fondere con il colore di base. |
| <b>Colore di base bordi netti</b> <i>0.0 - 1.0</i> | Quantità della mappa di curvatura da fondere con il colore di base. |
| <b>Colore di base Da Colore Vertice</b> <i>0.0 - 1.0</i> | Quantità del colore Vertice da unire al colore di base. |
| <b>Intensità materiale normale</b> <i>0.0 - 1.0</i> | Intensità di fusione della Normalmap cotta (tangente). |
| <b>SpecularAO</b> <i>0.0 - 1.0</i> | Forza di fusione dell’AO nello Specular. |
| <b>Bordi netti con Specular chiaro</b> <i>0.0 - 1.0</i> | Intensità di fusione della curvatura nello Specular. |
| <b>Specular contorni cartone animato</b> <i>0.0 - 1.0</i> | Intensità di fusione di un effetto Specular bordo-contorno, in base alla curvatura. |
| <b>Lucentezza bordi netti scuri</b> <i>0.0 - 1.0</i> | Forza di fusione della curvatura nella Lucentezza. |
| <b>Rugosità Bordi Netti E Luminosi</b> <i>0.0 - 1.0</i> | Forza di fusione della curvatura nella rugosità. |
| <b>Contorni fumetto rugosità</b> <i>0.0 - 1.0</i> | Intensità di fusione di un effetto bordo rugosità fumetto, in base alla curvatura. |
| <b>Bordi Netti Luminosi Metallici</b> <i>0.0 - 1.0</i> | Intensità di fusione della curvatura nel metallizzato. |
| <b>Contorni metallizzati dei cartoni animati</b> <i>0.0 - 1.0</i> | Intensità di fusione di un effetto bordo metallico del cartone animato, in base alla curvatura. |
| <b>Intensità materiale AO</b> <i>0.0 - 1.0</i> | Fusione la forza di mappa con baking AO con AO generato dal materiale, a che livello combinare entrambe le mappe AO. |
| <b>Intensità materiale Height</b> <i>0.0 - 1.0</i> | Fusione la forza del Height mappa con baking con il Height generato dal materiale, a che livello combinare entrambe le mappe altezza. |
| <b>Tipo di fusione materiale Height</b> <i>Rafforzare, Interpolazione</i> | Modalità Fusione per combinare entrambe le mappe di altezza. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/blenddata-ex.gif" />
        </td>
    </tr>
</table>
