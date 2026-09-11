---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Usate il nodo Sezione Simmetria per suddividere in sezioni le texture lungo gli assi delle simmetrie per creare pattern ed effetti specchiati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sezione simmetria
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# Sezione simmetria

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/mirror-2.png){width="128px"}

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo complesso dell&#39;operazione di Simmetria/mirroring. Consente un&#39;ampia varietà di operazioni geometriche con pieno controllo, ma richiede alcuni esperimenti.

Rispetto a [Mirror](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) e [Simmetrie](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), questo nodo offre molte più opzioni.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità Simmetria</b> <i>0 - 6</i> | Selezionate simmetria geometria/linea di specchiatura. Le opzioni disponibili sono Orizzontale, Verticale, Diagonale sinistra-destra, Diagonale destra-sinistra, Inverti verticale, Angolo e Angolo diagonale. |
| <b>Modalità di trasferimento</b> <i>0 - 6</i> | Modalità Fusione. Le opzioni disponibili sono: |
| <b>Fusione</b> <i>0.0 - 1.0</i> | Fusione nuovamente l’immagine originale nel risultato. |
| <b>Capovolgi lateralmente</b> <i>Falso/Vero</i> | Capovolge l&#39;origine, ovvero il lato di origine dell&#39;operazione viene invertito. La simmetria da sinistra a destra, ad esempio, diventa da destra a sinistra. |
| <b>Capovolgi lato2</b> <i>Falso/Vero</i> | Utilizzato solo quando la modalità Simmetria è 5 o 6. Inverti origine angolo. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symslice.png" />
        </td>
    </tr>
</table>
