---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry.html"
breadcrumb-title: ''
description: Utilizzate il nodo Simmetria (Symmetry) per creare serie simmetriche specchiando le texture lungo assi specificati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Simmetria
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# Simmetria

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry.resources/symmetry-9.png){width="128px"}

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue una serie di operazioni di simmetria su un&#39;immagine di input. Può essere utilizzato per rendere simmetriche le forme geometriche.

Questo nodo è molto simile a [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md), ma dispone di controlli aggiuntivi per i metodi di fusione.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità Simmetria</b> <i>Specchio Y, Specchio X, Diagonale Sinistra, Diagonale Destra, Specchio X/Y, Specchio X / Specchio Y, Diagonale Sinistra/Diagonale Destra, Diagonale Destra/Diagonale Sinistra, 8</i> | Consente di scegliere la modalità simmetria geometrica. |
| <b>Modalità di trasferimento</b> <i>0 - 6</i> | Scegli il metodo di fusione simmetria: Copia, Aggiungi, Sottrai, Moltiplica, Aggiungi secondario, Max, Min. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry.resources/symmetry-ex.png" />
        </td>
    </tr>
</table>
