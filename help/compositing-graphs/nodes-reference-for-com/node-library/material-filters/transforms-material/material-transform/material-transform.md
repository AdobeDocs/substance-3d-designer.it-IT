---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasformazione materiale per applicare le trasformazioni agli output del materiale, tra cui rotazione, scala e offset.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# Trasformazione materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## Trasformazione materiale

**Entrata:** *Filtri/Trasformazioni materiale*

**Semplice**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Material Transform è semplicemente la versione &quot;Multi-Channel&quot; Materials di [il nodo atomic Transformation 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Trasforma allo stesso tempo tutti i canali di un materiale in ingresso, con la stessa interfaccia di Trasforma 2D.

È sufficiente impostare correttamente i canali. Per impostazione predefinita, sono attivate entrambe le opzioni Metallico/Rugosità e Specular/Lucidità, il che potrebbe creare confusione.

## Parametri

* **Trasformazione**: *(Matrice Di Trasformazione)*\
  Ruota e ridimensiona il risultato. Lo spostamento e il panning vengono eseguiti tramite il parametro Offset
* **Scostamento**: *-0,5 - 0,5*\
  Sposta o converte il risultato. Quando è presente il controllo Trasformazione, il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Formato Normale**\
  Scegliete tra il formato DirectX e OpenGL (capovolgi verde).
* **Canali**\
  Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
