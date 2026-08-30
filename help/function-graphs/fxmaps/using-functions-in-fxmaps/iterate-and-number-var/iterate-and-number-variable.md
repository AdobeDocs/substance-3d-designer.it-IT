---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: Scoprite come utilizzare le variabili di iterazione e numerazione in FXMaps per creare pattern a ciclo continuo e variazioni procedurali.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variabile di iterazione e numerazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9505c371dff25c5d32a409abf76b95655b499571
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Esegui iterazione e variabile `$number`

![](iterate-and-number-variable.resources/iterate-1.jpg)

Il nodo iterazione eseguirà il rendering dei nodi connessi all&#39;output destro per la quantità di tempo specificata dal valore iterazioni.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/1-iteration.png"/></div> | 1 iterazione: il pattern gaussiano viene renderizzato una volta |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/10-iterations.png"/></div> | 10 iterazioni: il pattern gaussiano viene renderizzato 10 volte nello stesso punto |

Quando si utilizza un nodo Iterate, è possibile utilizzare la variabile `$number` per ottenere il valore di iterazione corrente. `$number` è un valore a virgola mobile e inizia da 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Questa funzione, impostata nel parametro Scostamento pattern, verrà eseguita 10 volte, una per ogni pattern.

Il primo pattern ha un valore `$number` uguale a 0 e viene quindi sottoposto a rendering in corrispondenza della coordinata (0, 0). Il secondo pattern ha un valore `$number` uguale a 1, viene quindi sottoposto a rendering in corrispondenza della coordinata (0,1, 0) (1 x 0,1 = 0,1) e così via per i pattern successivi.
