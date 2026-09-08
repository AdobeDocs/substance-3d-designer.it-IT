---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Utilizzate il nodo Forma per generare forme geometriche di base per la creazione di pattern e texture in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# Forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una varietà di forme procedurali, con opzioni per modificare le forme base. Le forme sono sempre perfettamente interpolate e di alta precisione.

Nonostante la sua semplicità, questo è un nodo molto utile: è l&#39;elemento costitutivo della maggior parte procedurale generazione Heightmap! Combinando forme di base con nodi di trasformazione, è possibile creare una forma Heightmap completamente procedurale, molto più precisa di qualsiasi bitmap.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Affiancatura</b> <i>1 - 16</i> | Imposta il numero di volte in cui il risultato deve essere affiancato. |
| <b>Pattern</b> <i>Quadrato, Disco, Paraboloide, Campana, Gaussiano, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Crescente, Capsula, Cono, Emisfero</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Specifico per pattern</b> <i>0.0 - 1.0</i> | Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato. |
| <b>Scala</b> <i>0.0 - 1.0</i> | Ridimensiona l&#39;intera forma. |
| <b>Dimensioni</b> <i>0.0 - 1.0</i> | Consente il ridimensionamento non uniforme su un asse X o Y. |
| <b>Angolo</b> <i>0.0 - 1.0</i> | Ruota l&#39;intera forma. |
| <b>Rotazione 45°</b> <i>Falso/Vero</i> | Ruota a 45 gradi preimpostati. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |
| <b>Affiancamento non quadrato</b> <i>Falso/Vero</i> | Quando è abilitato il Non square expansion, la forma verrà affiancata senza schiacciamenti. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-ex.gif" />
        </td>
    </tr>
</table>
