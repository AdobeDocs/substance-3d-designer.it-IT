---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilizza il nodo del filtro HBAO Occlusione ambiente per generare mappe di occlusione ambiente utilizzando algoritmi basati sull'orizzonte per un'ombreggiatura realistica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusione ambiente (HBAO) (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Occlusione ambiente (HBAO) (nodo filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Occlusione ambientale (HBAO)

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Utilizza una mappa dell’altezza come input e genera una mappa di Occlusione ambientale da tale mappa. Utilizza l&#39;Occlusione ambientale basata su orizzonte, un algoritmo originariamente destinato alla generazione di AO in tempo reale dello spazio-schermo. Molto utile per creare mappe AO procedurali da Heightmaps procedurali.

Per una versione alternativa, più avanzata ma più lenta di AO, vedere [Occlusione ambientale (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## Parametri

* **Usa unità globali**: *False/True* Attiva/disattiva l&#39;utilizzo di unità globali o dello spazio della schermata. Abilita parametri aggiuntivi che consentono un controllo più preciso.
* **Profondità Height**: *0.0 - 1.0* Utilizzato solo quando Unità globali è impostato su False. Controlla il ridimensionamento globale.
* **Dimensioni superficie**: **0.0 - 1000.0** Utilizzato solo quando Unità internazionali è impostato su True. Controlla il ridimensionamento globale.
* **Scala Height (cm)**: *0.0 - 1000.0* Utilizzata solo quando Unità globali è impostato su True. Controlla il ridimensionamento globale.
* **Raggio**: *0.0 - 1.0* Controlla la diffusione dell&#39;oggetto AO.
* **Qualità**: *4 campioni, 8 campioni, 16 campioni*\
  Imposta il livello di qualità determinando la quantità di campioni utilizzati per il calcolo.
* **Ottimizzazione GPU**: *False/True* Abilita l&#39;ottimizzazione interna della GPU e velocizza l&#39;elaborazione.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
