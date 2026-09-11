---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Usa il nodo Temperatura Crepe per aggiungere pattern di crepe ai materiali in base alla curvatura della trama e ai punti di sollecitazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Crepe meteorologiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Crepe meteorologiche

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Meteo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Aggiunge un pattern di crepe casuale, con controllo sulle pagine affiancate e sulla profondità.

Assicurati di aver compreso correttamente le [modalità di creazione del collegamento](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) quando lavori con i materiali completi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappe infornate o generate utilizzate per effetti interni e mascheratura. |
| <b>Height</b> <i>Input scala di grigi</i> | Mappe infornate o generate utilizzate per effetti interni e mascheratura. |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Avanzate</b> |  |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera. |
| <b>Effetto</b> |  |
| <b>Propagazione Crepe</b> <i>0.0 - 1.0</i> | La distanza di diffusione delle crepe. Questo è il controllo principale di questo effetto. |
| <b>Profondità Crepe</b> <i>0.0 - 1.0</i> | Profondità dell’effetto crepa. Questo influisce principalmente sul height e leggermente sul thickness visivo. |
| <b>Fusione</b> | Consente di controllare l’entità della fusione dell’effetto in ciascun canale risultante. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-ex.gif" />
        </td>
    </tr>
</table>
