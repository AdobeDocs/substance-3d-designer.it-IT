---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione Height di materiali per fondere più materiali in base alle mappe di height per creare effetti di materiale su più livelli.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione Height di materiali
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Fusione Height di materiali

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-height-blend.resources/material-height-blend.png){width="128px"}

<b>Tra:</b> Filtri materiali > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo è una versione più avanzata di [Fusione Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) che fonde due materiali in base alle loro Heightmap. Non esiste una maschera definita dall&#39;utente, quindi è necessario disporre di due Heightmap, una per ogni materiale, di cui almeno una non è un valore uniforme.

Questo può essere utile per combinare due diversi materiali di alta qualità senza una maschera di fusione di alta qualità.

Se si desidera fondere in acqua o neve, sono disponibili i nodi [Copertura Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e [Livello acqua](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Scostamento Height</b> <i>0.0 - 1.0</i> | Sposta le mappe di altezza in modo che il livello di fusione venga spostato lungo l&#39;asse del height. Questo è il controllo principale per la fusione. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto della fusione, rendendo le transizioni più nitide. |
| <b>Modalità</b> <i>height bilanciato, priorità height inferiore</i> |  |
| <b>Opacità</b> <i>0.0 - 1.0</i> | Opacità di fusione del height in primo piano, determina la dissolvenza in entrata o in uscita. |
| <b>Albedo corrispondente</b> <i>0.0 - 1.0</i> | Quantità di corrispondenza colore interna da eseguire tra i colori di Albedo. |
