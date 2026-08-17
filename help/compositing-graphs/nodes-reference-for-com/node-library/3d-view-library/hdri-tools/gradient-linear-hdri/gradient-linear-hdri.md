---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: Utilizza il nodo HDRI lineare sfumatura per creare sfumature lineari in ambienti HDRI per impostazioni di illuminazione personalizzate.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfumatura lineare (HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 1%

---


# Sfumatura lineare (HDRI)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/gradient-linear.png){width="200px"}

## Sfumatura lineare

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Crea una sfumatura lineare attraverso il centro con un punto posizionato dall’utente. Il risultato finale viene regolato in base alla proiezione sferica, a differenza del normale [gradiente lineare 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md).

## Parametri

* **Posizione punto**:\
  Posizione del punto utilizzato per determinare la direzione del gradiente.
* **Colore principale**: *(valore colore)*\
  Colore della parte superiore della sfumatura (al punto)
* **Colore inferiore**: *(valore colore)*\
  Colore della parte inferiore della sfumatura (lontano dal punto).
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.

## Immagini di esempio

![](../../../../../../assets/gradient-ex1.gif)

</td>
</tr>
</table>
