---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dal basso verso l'alto per generare maschere di sfumatura dal basso verso l'alto in base alla posizione del mondo della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dal basso verso l'alto
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# Dal basso verso l&#39;alto

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## Dal basso verso l&#39;alto

**Ingresso:** *Generatori Mesh/Generatori Maschera*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) in [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home).

In questo modo viene generata una transizione dal bianco al nero dal basso verso la parte superiore di un modello, utile per effettuare selezioni e dissolvenze basate sulla geometria.

## Parametri

### Input

* **Posizione**: *Input colore*\
  Mappa posizione al forno. Obbligatorio!
* **Rugosità:** *Input scala di grigi*\
  Questo non ha nulla a che fare con la rugosità PBR, ma è una mappa di variazione (opzionale) per interrompere la transizione. Viene visualizzato solo quando l’opzione Rugosità è impostata su un valore superiore a 0.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Sposta il livello medio del risultato tra bianco o nero, come una regolazione della luminosità.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto della transizione.
* **Rugosità\_Variazione**: *0.0 - 1.0* Determina la quantità della mappa di rugosità da combinare per la variazione. Se si aumenta questo valore oltre 0, viene visualizzato lo slot della mappa.

## Immagini di esempio

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
