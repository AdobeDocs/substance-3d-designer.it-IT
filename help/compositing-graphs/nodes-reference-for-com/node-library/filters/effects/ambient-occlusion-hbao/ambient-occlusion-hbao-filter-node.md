---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Utilizza il nodo del filtro HBAO di Occlusione ambientale per generare mappe di occlusione ambientale utilizzando algoritmi basati sull'orizzonte per un'ombreggiatura realistica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Occlusione ambiente (HBAO) (nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Occlusione ambiente (HBAO) (nodo filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Utilizza una mappa di altezza come input e genera una mappa di Occlusione ambientale da tale mappa. Utilizza l&#39;Occlusione ambientale basata su orizzonte, un algoritmo originariamente destinato alla generazione di AO in tempo reale dello spazio dello schermo. Molto utile per la creazione di mappe AO procedurali da mappe altezza procedurali.

Per una versione alternativa, più avanzata ma più lenta di AO, vedere [Occlusione ambientale (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Usa unità globali</b> <i>Falso/Vero</i> | Attiva/disattiva l’uso di unità di spazio mondo o schermo. Abilita parametri aggiuntivi che consentono un controllo più preciso. |
| <b>Profondità Height</b> <i>0.0 - 1.0</i> | Utilizzato solo quando l&#39;opzione Unità globali è impostata su False. Controlla il ridimensionamento globale. |
| <b>Dimensioni superficie</b> <i>0.0 - 1000.0</i> | Utilizzato solo quando l&#39;opzione Unità di misura mondo è impostata su True. Controlla il ridimensionamento globale. |
| <b>Scala Height (cm)</b> <i>0.0 - 1000.0</i> | Utilizzato solo quando l&#39;opzione Unità di misura mondo è impostata su True. Controlla il ridimensionamento globale. |
| <b>Raggio</b> <i>0.0 - 1.0</i> | Controlla la diffusione dell’AO. |
| <b>Qualità</b> <i>4 campioni, 8 campioni, 16 campioni</i> | Imposta il livello di qualità determinando la quantità di campioni utilizzati per il calcolo. |
| <b>Ottimizzazione GPU</b> <i>Falso/Vero</i> | Ottimizzazione interna della GPU, elaborazione più rapida. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>
