---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Utilizzate il nodo Selettore materiale per selezionare i materiali in base ai dati della trama per la creazione di effetti di texture multimateriale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Selettore materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Selettore materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Utility

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Converte una mappa ID a colori in una maschera binaria in bianco e nero. Consente di fondere e combinare colori diversi in una maschera.

Questa funzione è utile se non desideri utilizzare [Fusione multimateriale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) e preferisci utilizzare la maschera manualmente oppure se desideri utilizzare manualmente le stesse maschere in altre posizioni.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Materiali</b> <i>1 - 16</i> | Imposta il numero di materiali per cui è abilitata la combinazione. |
| <b>Abilita #1-16 materiale</b> <i>Falso/Vero</i> | Attiva o disattiva la fusione e la combinazione di colori nella maschera di output finale. Può essere attivato per tutti i colori che desideri combinare. |
| <b>Materiale #1-16</b> <i>(valore colore)</i> | Selettore colore per il colore dei materiali che verrà convertito in bianco e nero. |
| <b>Parametri Selettore colore</b> | Modifica la fusione e la conversione del colore in bianco e nero. |
| <b>Fuzziness</b> <i>0.01 - 1.0</i> | Quanto miscelare con i colori adiacenti. |
| <b>Spaziatura interna</b> <i>0.0 - 1.0</i> | Nitidezza della transizione, ad esempio Contrasto. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>
