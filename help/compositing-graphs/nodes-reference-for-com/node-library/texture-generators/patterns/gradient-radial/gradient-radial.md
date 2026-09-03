---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
breadcrumb-title: ''
description: Utilizzate il nodo radiale sfumatura per creare sfumature radiali che si irradiano da un punto centrale per transizioni di colore circolari.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Gradient Radial
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfumatura radiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# Sfumatura radiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-radial.resources/gradient-radial-01.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Simile a [Sfumatura circolare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md), crea una transizione di sfumatura in scala di grigio definita da due punti personalizzati in modo radiale. La transizione è da a a b, definita da centerpoint e raggio. Tieni presente che i risultati non verranno sempre affiancati.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Forma</b> <i>Cono, Emisfero</i> | Determina il profilo di transizione. Il cono è una transizione netta e lineare, l&#39;emisfero è morbido e arrotondato al centro. |
| <b>Punto 1</b> | Punto centrale della sfumatura. Inizia con il bianco. |
| <b>Punto 2</b> | Punto del raggio per determinare l’estensione della sfumatura. Termina in nero. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Abilita la compensazione di schiaccia e allunga con rapporti non quadrati. |
