---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dal basso verso l'alto per generare maschere di sfumatura dal basso verso l'alto in base alla posizione del mondo della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dal basso verso l'alto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# Dal basso verso l&#39;alto

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/features/smart-materials-and-masks) in [Painter](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/home).

In questo modo viene generata una transizione dal bianco al nero dal basso verso la parte superiore di un modello, utile per effettuare selezioni e dissolvenze basate sulla geometria.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Posizione</b> <i>Input colore</i> | Mappa posizione al forno. Obbligatorio! |
| <b>Rugosità</b> <i>Input scala di grigi</i> | Questo non ha nulla a che fare con la rugosità PBR, ma è una mappa di variazione (opzionale) per interrompere la transizione. Viene visualizzato solo quando l’opzione Rugosità è impostata su un valore superiore a 0. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Sposta il livello medio del risultato tra bianco o nero, come una regolazione della luminosità. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto della transizione. |
| <b>Variazione_Rugosità</b> <i>0.0 - 1.0</i> | Determina la quantità di mappa di rugosità da combinare per la variazione. Se si aumenta questo valore oltre 0, viene visualizzato lo slot della mappa. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-02.gif" />
        </td>
    </tr>
</table>
