---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/gradient-radial.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Sfumatura radiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/gradient-radial.png){width="128px"}

## Sfumatura radiale

**Ingresso:** *Generatori Di Texture**/Pattern*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Simile a [Sfumatura circolare](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-circular/gradient-circular.md), crea una transizione di sfumatura in scala di grigio definita da due punti personalizzati in modo radiale. La transizione è da a a b, definita da centerpoint e raggio. Tieni presente che i risultati non verranno sempre affiancati.

## Parametri

* **Forma: *Cono, Emisfero***Determina il profilo di transizione. Il cono è una transizione netta e lineare, l&#39;emisfero è morbido e arrotondato al centro.
* **Punto 1**:\
  Punto centrale della sfumatura. Inizia con il bianco.
* **Punto 2**:\
  Punto del raggio per determinare l’estensione della sfumatura. Termina in nero.
* **Non square expansion**: *Falso/Vero*\
  Abilita la compensazione di schiaccia e allunga con rapporti non quadrati.

</td>
</tr>
</table>
