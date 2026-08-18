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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 1%

---


# Irradianza RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/rt-irradiance.png){width="128px"}

**Ingresso:** *Filtri/Effetti*

**Complesso**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Genera l&#39;irradianza ray tracing su un input mappa di height generato da una mappa dell&#39;ambiente e da una mappa di emissione. Può essere utilizzato per &quot;vivacizzare&quot; l’illuminazione in una texture all’interno di un grafico. Utilizzato per falsi segnali luminosi e illuminazione globale.Questo nodo non deve essere utilizzato in combinazione con il motore CPU (SSE) a causa del tempo di calcolo. Restituisce due mappe: un output di irradianza in cui l&#39;irradianza viene applicata agli input del materiale, una mappa di irradianza non elaborata contenente solo i valori di irradianza calcolati.

</td>
</tr>
</table>

## Parametri

### Input

* **Height:** *L&#39;input in scala di grigi* Height è l&#39;unico input richiesto dallo slot del materiale. Senza di esso, il nodo non funzionerà bene.
* **Emissivo:** *Input colore* Emissivo deve essere in un formato in cui il nero puro non emette luce, qualsiasi altro valore di colore emette luce. Alpha ignorato. Per visualizzare i risultati, è necessaria una connessione a questo slot o allo slot Ambiente.
* **Ambiente**: *Input colore*\
  Ambiente di illuminazione HDR con cui calcolare l&#39;irradianza. Per visualizzare i risultati, è necessaria una connessione a questo slot o allo slot di espulsione.

### Parametri

* **Scala Height**: *0,0 - 1,0*\
  Scala per interpretare il height in. Influisce sull’aspetto dell’intera scena.
* **Qualità**: *32 raggi, 64 raggi, 128 raggi*\
  Determina la qualità dei risultati, ma influisce anche sulle prestazioni. Meno raggi significa più rumore.
* **Calcola Rimbalzi**: *Falso/Vero*\
  Attiva/disattiva il calcolo dei rimbalzi. Influenza sulla qualità e la velocità.
* **Rotazione ambiente**: *0.0 - 1.0*\
  Ruota l&#39;ambiente.
* **Esposizione Ambiente (EV)**: *-4.0 - 4.0*\
  Il valore di esposizione da utilizzare per l’ambiente influisce sulla luminosità totale dell’effetto.
* **Intensità di emissione**: *0,0 - 20,0*\
  Moltiplicatore per l&#39;input Emissivo, influisce sull&#39;intensità dell&#39;irradianza da emissivo.
* **Spazio colore mancante**: *sRGB, lineare*\
  Spazio colore utilizzato per interpretare l’input Enissive.
* **Ombre IBL nell&#39;Alpha di irradiamento raw**: *False/True*\
  Attivate/disattivate per aggiungere ombre alla
* **Polarizzazione LOD emessa**: *-1.0 - 1.0* Regolare la qualità dell&#39;irradianza di emissione. Un valore più basso indica più rumore.

## Immagini di esempio

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/rt-irr-03-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/rt-irr-01-1.jpg" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/rt-irr-02-1.jpg" width="300px"/></div> |
| --- | --- | --- |
|  |  |  |
