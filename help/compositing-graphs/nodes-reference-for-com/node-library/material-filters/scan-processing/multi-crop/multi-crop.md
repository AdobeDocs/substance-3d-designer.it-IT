---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Usa il nodo Multi Crop per ritagliare più canali di texture contemporaneamente per elaborare i materiali scansionati in modo efficiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglio multiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Ritaglio multiplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## Ritaglio multiplo (scala di grigi)

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questa è la versione multicanale di Ritaglio. Ritaglia un’area da un’immagine ed è destinato principalmente all’uso con foto con più angoli, che vengono quindi combinate con [Da multiangolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multiangolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Per ulteriori informazioni, consultate il [ritaglio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) originale.

## Parametri

### Parametri

* **Numero di input**: *1 - 8* Imposta il numero di input da elaborare in parallelo.
* **Dimensione input**: *0 - 8192* Risoluzione e proporzioni delle immagini di input. Molto importante per immagini non quadrate.
* **Sfondo**: *(Valore colore) / (Valore scala di grigi)*Valore uniforme dello sfondo per le aree non coperte dal ritaglio.
* **Trasformazione**: *(Matrice Di Trasformazione)*\
  Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Scostamento**: *0,0 - 1,0*\
  Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Normale (solo per la versione a colori)**: *Falso/Vero* Indica se l&#39;input deve essere trattato come una mappa normale.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
