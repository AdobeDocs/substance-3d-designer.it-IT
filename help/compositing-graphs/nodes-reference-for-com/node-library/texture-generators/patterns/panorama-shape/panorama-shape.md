---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: Utilizzate il nodo Forma panorama per creare forme associate a coordinate panoramiche per la generazione di texture nell'ambiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma panorama
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# Forma panorama

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-1.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo è un nodo utile per generare mappe panoramiche procedurali di tipo &quot;Studio&quot;. Consente di posizionare e modificare le immagini in evidenza, nonché di impostarne le proprietà HDR. Può essere concatenato per più forme.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Matrice forme</b> | Sposta o converte il risultato, che può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Forma</b> <i>quadrato, disco</i> | Imposta il tipo di forma. |
| <b>Colore forma</b> <i>(valore colore)</i> | Imposta il colore della forma. |
| <b>Intensità forma</b> <i>0.0 - 100.0</i> | Imposta l’intensità HDR della forma. |
| <b>Bordo sfumato forma</b> <i>0.0 - 1.0</i> | Modifica la morbidezza dei bordi della forma. |
| <b>Intensità hotspot</b> <i>0.0 - 100.0</i> | Imposta l&#39;intensità HDR del punto attivo della forma. |
| <b>Dimensione hotspot</b> <i>0.0 - 1.0</i> | Modifica le dimensioni del punto attivo all&#39;interno della forma. |
| <b>Falloff hotspot</b> <i>0.0 - 1.0</i> | Modifica il decadimento e la fusione dei bordi del punto attivo. |
| <b>Posizione punto attivo</b> <i>0.0 - 1.0</i> | Sposta il punto attivo in relazione alla forma. |
| <b>Abilita sfondo</b> <i>Falso/Vero</i> | Consente di riempire lo sfondo con una tinta unita. Tenete presente che non è più possibile concatenarli mediante fusione. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Consente di impostare il colore in tinta unita dello sfondo. |
| <b>Abilita input Texture</b> <i>Falso/Vero</i> | Consente un input personalizzato anziché un tipo di forma predefinito. |
