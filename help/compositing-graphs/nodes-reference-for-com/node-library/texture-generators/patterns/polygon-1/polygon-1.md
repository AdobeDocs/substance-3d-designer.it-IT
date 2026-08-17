---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Usa il nodo Poligono 1 per generare pattern poligonali di base con lati e proprietà personalizzabili per texture geometriche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Poligono 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---


# Poligono 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/polygon-1-1.png){width="128px"}

## Poligono 1

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una forma poligonale, con molte opzioni di regolazione. Per una versione più semplice, vedere [Poligono 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md).

## Parametri

* **Lati**: *3 - 32* Imposta la quantità di lati che il poligono deve avere.
* **Esplodi**: *0.0 - 1.0* Sposta le &quot;sezioni&quot; del poligono.
* **Dimensione triangolo**: *0,0 - 1,0* Regola la dimensione di sezioni/triangoli. Qualsiasi regolazione poteva dividere la forma, solo 1,1. è perfettamente connesso!
* **Scala**: *0.0 - 1.0* Ridimensiona l&#39;intera forma come un&#39;unica entità.
* **Scala automatica**: *False/True* Regola le proporzioni in modo che l&#39;intero poligono si adatti alla visualizzazione, con i parametri predefiniti.
* **Rotazione**: *0.0 - 1.0* Ruota l&#39;intera forma.
* **Sfumatura**: *Falso/Vero* Genera sezioni/triangoli sfumati anziché solidi. Nota: diventa simile al Poligono 2 con questa impostazione attivata.
* **Inversione sfumatura**: *False/True* Inverte la direzione della sfumatura se &quot;Sfumatura&quot; è abilitato.
* **Affiancatura**: *1 - 16*\
  Imposta il numero di volte in cui il risultato deve essere affiancato.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.
* **Affiancatura non quadrata**&#x200B;**:** *False/True*Quando è attivato il Non square expansion, la forma verrà affiancata senza schiacciamenti.

## Immagini di esempio

![](../../../../../../assets/polygon-1-ex.gif)

</td>
</tr>
</table>
