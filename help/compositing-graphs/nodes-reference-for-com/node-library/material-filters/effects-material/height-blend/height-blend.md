---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione Height (Blend) per fondere le texture in base alle mappe di height per creare transizioni di materiale realistiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Fusione height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Fusione height

**Ingresso:** *Filtri/Effetti Materiale*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Combina due Heightmap in base alle informazioni di height. Genera una mappa di altezza con fusione, ma anche una maschera Bianco e nero che può essere utilizzata altrove.

Questo è utile quando si dispone di due Heightmap di alta qualità da combinare, ma non necessariamente di un materiale completo, come è richiesto per [Material Height Blend](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

## Parametri

### Input

* **Inizio Height**: *Input scala di grigi*
* **Height inferiore**: *Input scala di grigi*
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Scostamento Height**: *0.0 - 1.0* Sposta le mappe di altezza in modo che il livello di fusione venga spostato lungo l&#39;asse del height. Questo è il controllo principale per la fusione.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto della fusione, rendendo le transizioni più nitide.
* **Modalità**: *height bilanciato, priorità height inferiore* Consente di passare da un metodo di fusione all&#39;altro.
* **Opacità**: *0,0 - 1,0*\
  Opacità di fusione del height in primo piano, determina la dissolvenza in entrata o in uscita.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
