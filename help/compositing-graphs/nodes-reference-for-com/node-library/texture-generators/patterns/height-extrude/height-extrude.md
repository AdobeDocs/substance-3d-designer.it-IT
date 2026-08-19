---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Usate il nodo Height Extrude per applicare l’estrusione alle forme in base alle mappe dei height e creare effetti profondità 3D nelle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height Extrude
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Height Extrude

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## Height Extrude

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Height Extrude esegue il rendering della Profondità Z 3D da una mappa del Height di input. Proprio come l&#39;[Estrusione forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) e il [Cubo 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), consente di ruotare una videocamera nella vista 2D. Il suo obiettivo principale è quello di fungere da generatore per la creazione di forme ruotate in 3D da una mappa di altezza piatta. Queste forme possono quindi essere utilizzate con [Splatter forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

La differenza principale con [Shape Extrude](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) è che la mappa di input non deve essere un tipo binario &quot;alfa&quot; di mappa, ma una mappa in scala di grigi a intervallo completo. Ciò significa che hai un maggiore controllo sul height di estrusione (forme organiche e complesse), ma nessun controllo su nulla come lo smussamento dei profili (forme hard-surface, più semplici).

## Parametri

* **Angolo fotocamera**:\
  Angoli più alti della fotocamera, in semicerchi. Tieni presente che la rotazione orizzontale e la scala vengono applicate direttamente all&#39;input.
* **Scala fotocamera**: *0.001 - 3.0*\
  Scala globale applicata all’output.
* **Scala Height**: *0,0 - 2,0*\
  Applica un fattore globale ai valori del height di input.
* **Scostamento verticale**: *-1,0 - 1,0*\
  Sposta l’output finale verso l’alto o il basso.
* **Terra**: *Disattivato/Attivato*\
  Se Ground (Terra) è disattivato, viene visualizzato uno sfondo nero in cui l&#39;input è 0 anziché un piano simile a quello del terreno.
* **Formato normale**: *DirectX/OpenGL*\
  Il parametro **Formato normale** inverte la coordinata y della mappa normale.
* **Intensità normale**: *0,0 - 256,0*\
  Uguale al parametro **Intensità** del nodo **Normale**. Impostatelo su 256 per ottenere una normale assenza di taglio durante la rotazione.

## Immagini di esempio

</td>
</tr>
</table>
