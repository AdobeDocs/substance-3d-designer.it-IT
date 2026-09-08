---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: Utilizzate il nodo Ritaglio materiali per ritagliare le aree della texture dai materiali scansionati per isolare aree di interesse specifiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ritaglio materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Ritaglio materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo è la versione di materiale completa multicanale di [Ritaglio](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Consente di eseguire un’operazione di ritaglio su uno o più canali di materiale in parallelo.

>[!NOTE]
>
> [Per ulteriori informazioni, consultate l&#39;originale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[Ritaglia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali di materiale in questo gruppo quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Dimensione input</b> <i>0 - 8192</i> | Specificate la risoluzione e le proporzioni dell’immagine. Molto importante per immagini non quadrate. |
| <b>Sfondo</b> <i>(valore colore) / (valore scala di grigi)</i> | Valore uniforme dello sfondo per le superfici non coperte dalla funzione Ritaglio. |
| <b>Trasformazione</b> <i>(Matrice di trasformazione)</i> | Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro. |
