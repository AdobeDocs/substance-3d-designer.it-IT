---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: Utilizzare il nodo Irradianza RT per calcolare in tempo reale le informazioni di irradianza dalla geometria per calcoli di illuminazione realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Irradianza RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# Irradianza RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera l&#39;irradianza ray tracing su un input mappa di altezza generato da una mappa di ambiente e da una mappa di emissivo. Può essere usato per &quot;eseguire i baking&quot; l’illuminazione in una texture all’interno di un grafico. Utilizzato per falsi segnali luminosi e illuminazione globale.Questo nodo non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo. Restituisce due mappe: un output di irradianza in cui l&#39;irradianza viene applicata agli input del materiale, una mappa di irradianza non elaborata contenente solo i valori di irradianza calcolati.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Height</b> <i>Input in scala di grigi</i> | Height è l&#39;unico input richiesto dallo slot del materiale. Senza di esso, il nodo non funzionerà bene. |
| <b>Emissivo</b> <i>Input colore</i> | L’Emissivo deve essere in un formato in cui il nero puro non emette luce, qualsiasi altro valore di colore emette luce. Alpha ignorato. Per visualizzare i risultati, è necessaria una connessione a questo slot o allo slot Ambiente. |
| <b>Ambiente</b> <i>Input colore</i> | Ambiente di illuminazione HDR con cui calcolare l&#39;irradianza. Per visualizzare i risultati, è necessario un collegamento a questo slot o allo slot Emissivo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala Height</b> <i>0.0 - 1.0</i> | Scala per interpretare il height in. Influisce sull’aspetto dell’intera scena. |
| <b>Qualità</b> <i>32, 64, 128, </i> | Determina la qualità dei risultati, ma influisce anche sulle prestazioni. Meno raggi significa più rumore. |
| <b>Calcola rimbalzi</b> <i>Falso/Vero</i> | Attiva/disattiva il calcolo dei rimbalzi. Influenza sulla qualità e la velocità. |
| <b>Rotazione ambiente</b> <i>0.0 - 1.0</i> | Ruota l&#39;ambiente. |
| <b>Esposizione dell&#39;ambiente (EV)</b> <i>-4.0 - 4.0</i> | Il valore di esposizione da utilizzare per l’ambiente influisce sulla luminosità totale dell’effetto. |
| <b>Intensità di emissione</b> <i>0.0 - 20.0</i> | Moltiplicatore per l&#39;input Emissivo, influisce sull&#39;intensità dell&#39;irradianza da emissivo. |
| <b>Spazio cromatico Emissivo</b> <i>sRGB, lineare</i> | Spazio colore utilizzato per interpretare l’input Enissive. |
| <b>Ombre IBL nell&#39;Alpha di irradiamento raw</b> <i>Falso/Vero</i> | Attivate/disattivate per aggiungere ombre alla |
| <b>Polarizzazione LOD Emissivo</b> <i>-1.0 - 1.0</i> | Regola la qualità dell&#39;irradianza emissivo. Un valore più basso indica più rumore. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-04.jpg" />
        </td>
    </tr>
</table>
