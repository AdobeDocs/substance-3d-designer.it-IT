---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Utilizzare il nodo QG Normale al Height per convertire le mappe normali in mappe di altezza di alta qualità per l'estrazione dei dettagli della superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale alla sede centrale del Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Normale alla sede centrale del Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di conversione inversa che tenta di riconvertire una Normalmap dello spazio tangente in una Heightmap. Questo è il nodo più avanzato; [Normale al Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) ha meno opzioni e utilizza calcoli diversi.

Utile per quando si dispone solo di una sorgente Normalmap, ma si desidera comunque eseguire operazioni combinandole con una Heightmap. Tenete presente che questo non sarà mai in grado di fornire un risultato corretto al 100%, poiché le informazioni vengono perse per natura del processo quando il Height viene convertito in Normale. Non può mai sostituire una mappa dell&#39;altezza generata correttamente.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Saldo Rilievo</b> <i>0.0 - 1.0</i> | Fusione tra distorsione a bassa e alta frequenza. |
| <b>Intensità Height</b> <i>0.0 - 1.0</i> | L’intensità o il moltiplicatore per Heightmap funziona un po’ come l’opacità globale. |
| <b>Normalizzazione Height</b> <i>Falso/Vero</i> | Ridimensiona automaticamente l&#39;intervallo della mappa di altezza in modo da utilizzare l&#39;intero contrasto, ad esempio [livelli automatici](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md). |
| <b>Qualità</b> <i>Normale, Alto</i> | Consente di passare dalla velocità alla qualità. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal-to-height-hq-02.png" />
        </td>
    </tr>
</table>
