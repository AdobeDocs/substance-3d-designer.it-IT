---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---


# Fusione Height di materiali

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

## Fusione Height di materiali

**Ingresso:** *Filtri/Effetti Materiale*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo è una versione più avanzata di [Fusione Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) che fonde due materiali in base alle loro Heightmap. Non esiste una maschera definita dall&#39;utente, quindi è necessario disporre di due Heightmap, una per ogni materiale, di cui almeno una non è un valore uniforme.

Questo può essere utile per combinare due diversi materiali di alta qualità senza una maschera di fusione di alta qualità.

Se si desidera fondere in acqua o neve, sono disponibili i nodi [Copertura Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e [Livello acqua](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

## Parametri

### Parametri

* **Canali**\
  Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Scostamento Height**: *0.0 - 1.0* Sposta le mappe di altezza in modo che il livello di fusione venga spostato lungo l&#39;asse del height. Questo è il controllo principale per la fusione.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto della fusione, rendendo le transizioni più nitide.
* **Modalità**: *height bilanciato, priorità height inferiore* Consente di passare da un metodo di fusione all&#39;altro.
* **Opacità**: *0,0 - 1,0*\
  Opacità di fusione del height in primo piano, determina la dissolvenza in entrata o in uscita.
* **Corrispondenza Albedo**: *0.0 - 1.0* Quantità di corrispondenza colore interna da eseguire tra i colori di Albedo.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
