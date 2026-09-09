---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Utilizzare il nodo Normale a Height per convertire le mappe normali in mappe height per estrarre le informazioni sulle profondità di superficie.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale al Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Normale al Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height.png){width="128px"}

<b>Ingresso:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo di conversione inversa che tenta di riconvertire una Normalmap dello spazio tangente in una Heightmap. Questa è la versione leggermente più semplice; [Normale alla sede centrale del Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) dispone di più opzioni.

Utile per quando si dispone solo di una sorgente Normalmap, ma si desidera comunque eseguire operazioni combinandole con una Heightmap. Tenete presente che questo non sarà mai in grado di fornire un risultato corretto al 100%, poiché le informazioni vengono perse per natura del processo quando il Height viene convertito in Normale. Se regoli le impostazioni di conseguenza, questa versione non-HQ esegue un buon lavoro di conversione dei dettagli semplici.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Saldo Rilievo</b> <i>0.0 - 1.0</i> | Regolate la misura in cui le diverse frequenze influenzano il risultato finale. Ciò dipende in larga misura dalla mappa di input e richiede un po&#39; di modifica. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Opacità globale</b> <i>0.0 - 1.0</i> | Regola l’opacità globale dell’effetto. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal2heightex.png" />
        </td>
    </tr>
</table>
