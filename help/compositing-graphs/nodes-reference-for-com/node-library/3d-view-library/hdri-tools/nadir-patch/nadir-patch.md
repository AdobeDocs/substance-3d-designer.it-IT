---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Utilizzate il nodo Nadir patch per applicare una patch all'area inferiore dei panorami HDRI per correggere gli artefatti inferiori nelle mappe dell'ambiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# Nadir patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo fornisce la funzionalità di applicare patch al punto di terra centrale (nadir) di un&#39;immagine mappata a livello sferico. Può essere usato per nascondere o &quot;clonare&quot; un brutto nadir, o una fotocamera visibile o un treppiede. Funziona come una [patch Clona /Clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md), ma con regolazioni per immagini con mappatura sferica. L’utente seleziona un punto altrove nell’immagine, ovvero il punto clonato e fuso in basso. Non sono necessari altri input esterni oltre a un singolo HDRI per l’elaborazione, ma è possibile utilizzare una maschera esterna come canale alfa per l’effetto patch.

l&#39;effetto può essere controllato e convalidato rapidamente con [Nadir extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Input colore</i> |  |
| <b>Input maschera</b> <i>Input scala di grigi</i> | Slot maschera opzionale utilizzato per mascherare la patch. Funziona come un alfa. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Abilita</b> <i>Falso/Vero</i> | Attivare o disattivare l&#39;effetto applicazione di patch. |
| <b>Mostra helper Fotogrammi</b> <i>Falso/Vero</i> | Mostrare o nascondere le linee di supporto per il debug. |
| <b>Thickness di Fotogrammi</b> <i>0.0 - 1.0</i> | Thickness di linee di supporto. |
| <b>Scala patch</b> <i>0.0 - 1.0</i> | Scala globale e uniforme della patch. Influisce sia sull&#39;origine che sulla destinazione. |
| <b>Dimensione patch</b> <i>0.0 - 1.0</i> | Dimensioni non uniformi del cerotto. |
| <b>Rotazione patch</b> <i>0.0 - 1.0</i> | Rotazione del cerotto. Influisce sull&#39;origine e sulla destinazione. |
| <b>Alpha patch</b> <i>Simbolo grafico, gaussiano, input maschera</i> | Imposta il valore alfa utilizzato per fondere il cerotto con lo sfondo. |
| <b>Durezza patch</b> <i>0.0 - 1.0</i> | Impostate la durezza/il contrasto dell&#39;alfa. |
| <b>Offset rotazione origine</b> <i>0.0 - 1.0</i> | Rotazione solo per la sorgente del cerotto. |
| <b>Coordinate posizione</b> |  |
| <b>Posizione di origine</b> | Posizione della sorgente. Ha maniglia nella vista 2D. |
| <b>Posizione patch</b> | Posizione del bersaglio. Ha maniglia nella vista 2D. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nadir-patch-ex.gif" />
        </td>
    </tr>
</table>
