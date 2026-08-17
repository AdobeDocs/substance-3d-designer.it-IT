---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Usa il nodo Trasformazione non quadrata per applicare le trasformazioni a texture non quadrate con ridimensionamento X e Y indipendente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione non quadrata
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Trasformazione non quadrata

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Trasformazione non quadrata (scala di grigi)

**Entrata:** *Filtri/Trasformazioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Versione non quadrata sicura di [Trasforma 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Rileva automaticamente le proporzioni non quadrate e può trasformare le immagini con input quadrati in un&#39;area di lavoro non quadrata.

Assicurati di aver compreso appieno i [parametri del grafico](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)per utilizzare al meglio questo nodo, in quanto dovrai impostare alcune impostazioni correttamente:

* La dimensione del **grafico** deve essere non quadrata, altrimenti non è necessario questo nodo.
* Imposta la dimensione dell&#39;output **del nodo** di trasformazione non quadrata su &quot;*Rispetto all&#39;elemento padre*&quot;.
* Se si desidera trasformare l&#39;input in un&#39;unica posizione, impostare la modalità di suddivisione in porzioni del **nodo** su &quot;*Nessuna porzione*&quot;.

## Parametri

* **Modalità riquadro**: *Automatica, Manuale* Abilita o meno le compensazioni automatiche non quadrate.
* **Affianca**: *1 - 16* Accessibile solo quando la modalità Affianca è impostata su Manuale. Consente di modificare la scala in modo sicuro.
* **Scostamento**: *0,0 - 1,0*\
  Sposta o converte il risultato. Fai doppio clic sul cursore per immettere i valori negativi.
* **Rotazione**: *0.0 - 1.0* Ruota l&#39;immagine di input.
* **Rotazione sicura (solo quadrati)**: *False/True* Aggancia ai valori sicuri per mantenere la nitidezza dei pixel.
* **Colore di sfondo**: *(valore colore)*Colore di sfondo con cui riempire l&#39;immagine. Visibile solo quando la modalità di [porzione nei parametri di base è impostata su &quot;*Nessuna porzione*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md).

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
