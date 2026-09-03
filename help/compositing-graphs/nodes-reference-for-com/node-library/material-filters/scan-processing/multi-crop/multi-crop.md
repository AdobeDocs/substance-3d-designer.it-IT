---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Usa il nodo Multi Crop per ritagliare più canali texture contemporaneamente per elaborare i materiali scansionati in modo efficiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglio multiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# Ritaglio multiplo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-crop.resources/multi-crop-01.png){width="128px"}

![](multi-crop.resources/multi-crop-02.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questa è la versione multicanale di Ritaglio. Ritaglia un’area da un’immagine ed è destinato principalmente all’uso con foto con più angoli, che vengono quindi combinate con [Da multiangolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multiangolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Per ulteriori informazioni, consultate il [ritaglio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) originale.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Conteggio input</b> <i>1 - 8</i> | Imposta il numero di input da elaborare in parallelo. |
| <b>Dimensione input</b> <i>0 - 8192</i> | Immettere la risoluzione e le proporzioni delle immagini. Molto importante per immagini non quadrate. |
| <b>Sfondo</b> <i>(valore colore) / (valore scala di grigi)</i> | Valore uniforme dello sfondo per le superfici non coperte dalla funzione Ritaglio. |
| <b>Trasformazione</b> <i>(Matrice di trasformazione)</i> | Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Normale (solo per la versione a colori)</b> <i>Falso/Vero</i> | Indica se l&#39;input deve essere trattato come una Normalmap. |
