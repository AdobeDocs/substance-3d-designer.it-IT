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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## Forma

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una varietà di forme procedurali, con opzioni per modificare le forme base. Le forme sono sempre perfettamente interpolate e di alta precisione.

Nonostante la sua semplicità, questo è un nodo molto utile: è l&#39;elemento costitutivo della maggior parte procedurale generazione Heightmap! Combinando forme di base con nodi di trasformazione, è possibile creare una forma Heightmap completamente procedurale, molto più precisa di qualsiasi bitmap.

## Parametri

* **Affiancatura**: *1 - 16*\
  Imposta il numero di volte in cui il risultato deve essere affiancato.
* **Motivo**: *Quadrato, Disco, Paraboloide, Campana, Gaussiano, Torace, Piramide, Mattone, Gradazione, Onde, Mezza Campana, Campana Ridotta, Crescente, Capsula, Cono*, Emisfero**\
  Seleziona la forma del motivo da utilizzare.
* **Specifico per pattern**: *0,0 - 1,0*\
  Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato.
* **Scala**: *0.0 - 1.0* Ridimensiona l&#39;intera forma.
* **Dimensioni**: *0.0 - 1.0* Consente il ridimensionamento non uniforme su un asse X o Y.
* **Angolo**: *0.0 - 1.0* Ruota l&#39;intera forma.
* **Rotazione 45°**: *False/True* Ruota a 45 gradi preimpostati.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Affiancatura non quadrata****:** *False/True*Quando è attivato il Non square expansion, la forma verrà affiancata senza schiacciamenti.

## Immagini di esempio

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
