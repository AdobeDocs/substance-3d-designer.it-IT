---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Usa il nodo Height Extrude per applicare l’estrusione alle forme in base alle mappe dell’altezza per creare effetti profondità 3D nelle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Extrude
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# Height Extrude

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Height Extrude esegue il rendering di una Profondità Z 3D da una mappa Altezza di input. Proprio come l&#39;[Estrusione forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) e il [Cubo 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), consente di ruotare una videocamera all&#39;interno del vista 2D. Il suo obiettivo principale è quello di fungere da generatore per la creazione di forme ruotate in 3D da una mappa di altezza piatta. Queste forme possono quindi essere utilizzate con [Splatter forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

La differenza principale con [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) è che la mappa di input non deve essere un tipo binario &quot;alfa&quot; di mappa, ma una mappa in scala di grigi a intervallo completo. Ciò significa che hai un maggiore controllo sul height di estrusione (forme organiche e complesse), ma nessun controllo su nulla come lo smussamento dei profili (forme hard-surface, più semplici).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Angolo videocamera</b> | Angoli più alti della fotocamera, in semicerchi. Tieni presente che la rotazione orizzontale e la scala vengono applicate direttamente all&#39;input. |
| <b>Scala fotocamera</b> <i>0.001 - 3.0</i> | Scala globale applicata all’output. |
| <b>Scala Height</b> <i>0.0 - 2.0</i> | Applica un fattore globale ai valori del height di input. |
| <b>Scostamento verticale</b> <i>-1.0 - 1.0</i> | Sposta l’output finale verso l’alto o il basso. |
| <b>Terra</b> <i>Disattivato/Attivato</i> | Se Ground (Terra) è disattivato, viene visualizzato uno sfondo nero in cui l&#39;input è 0 anziché un piano simile a quello del terreno. |
| <b>Formato Normale</b> <i>DirectX/OpenGL</i> | Il parametro <b>Formato normale</b> inverte la coordinata y della mappa normale. |
| <b>Intensità normale</b> <i>0.0 - 256.0</i> | Uguale al parametro <b>Intensità</b> del nodo <b>Normale</b>. Impostatelo su 256 per ottenere una normale assenza di taglio durante la rotazione. |
