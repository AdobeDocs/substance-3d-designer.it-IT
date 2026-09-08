---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: Utilizzate il nodo Riflessioni caustiche per generare pattern di luce caustica per creare effetti di luce subacquea e rifrattiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Riflessioni caustiche
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# Riflessioni caustiche

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-caustics-grayscale.png){width="128px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera caustiche proiettate in base a una mappa del height e a una direzione della luce.Disponibile sia nella versione in scala di grigio che in quella a colori, le differenze sono lievi, ma la versione a colori aggiunge effetti di dispersione del colore. La luce viene proiettata da un singolo punto, non viene utilizzata alcuna mappa di ambiente.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Spazio colore di output</b> <i>Raw, sRGB</i> | Imposta lo spazio colore di output. |
| <b>Dimensione griglia Photon</b> <i>Automatico, 512, 1024, 2048, 4096</i> | Imposta la qualità regolando le dimensioni della griglia, ma per impostazione predefinita corrisponde all’input. Può essere utilizzato per velocizzare i calcoli. |
| <b>Scala Height Superficie</b> <i>0.0 - 1.0</i> | Moltiplicatore per determinare come viene interpretato il height. |
| <b>Posizione Height Superficie</b> <i>0.0 - 1.0</i> | Impostate la distanza della superficie di rifrazione rispetto alla proiezione. |
| <b>Superficie IOR</b> <i>1.0 - 2.0</i> | Impostate l&#39;indice di rifrazione: nella versione a colori questa opzione aggiunge una maggiore dispersione di colore. |
| <b>Dimensione Photon</b> <i>1.0 - 50.0</i> | La dimensione del fotone influisce sulla nitidezza dell’effetto. |
| <b>Dispersione</b> <i>0.0 - 0.01 (solo versione a colori)</i> | Modificate solo la dispersione dei colori. Non visibile quando lo IOR è basso. |
| <b>Variazione</b> <i>0.0 - 1.0</i> | Aggiungete la variazione irregolare alle particelle di fotoni proiettati. |
| <b>Posizione chiara</b> | Sposta la luce. Eseguito anche tramite un gizmo nella vista 2D. |
| <b>Colore di sfondo</b> <i>(valore colore) (solo versione colore)</i> | Modifica il colore di sfondo. Limitato al nero nella versione in scala di grigi. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Abilita la compensazione di schiaccia e allunga con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/rt-caustics-grayscale-1.png" />
        </td>
    </tr>
</table>
