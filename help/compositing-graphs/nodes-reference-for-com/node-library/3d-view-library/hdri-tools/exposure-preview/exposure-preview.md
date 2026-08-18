---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Utilizzate il nodo Anteprima esposizione per visualizzare in anteprima le regolazioni di esposizione negli ambienti HDRI prima del rendering finale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Anteprima esposizione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Anteprima esposizione

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## Anteprima esposizione

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Nodo helper per visualizzare l&#39;anteprima dei passaggi di esposizione. Gli utenti impostano un valore minimo e un valore massimo, il nodo genera un&#39;immagine molto più grande con un numero diverso di versioni esposte dell&#39;input originale. Le diverse versioni sono sempre impilate orizzontalmente, la quantità dipende dalla risoluzione del nodo o del grafico.

## Parametri

* **Esposizione massima (EV)**: *-8,0 - 8,0*\
  Esposizione massima dell’immagine più luminosa in alto.
* **Esposizione minima (EV)**: *-8.0 - 8.0* Esposizione minima dell&#39;immagine più scura nella parte inferiore.

## Immagini di esempio

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
