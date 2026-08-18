---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: Usate il nodo Quantizza scala di grigi per ridurre il numero di livelli della scala di grigi per gli effetti di posterizzazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quantizza scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Quantizza scala di grigi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Quantizza scala di grigi](../../../../../../assets/quantize-grayscale.png "Icona Quantizza scala di grigi"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una singola spline a forma di cerchio.

</td>
</tr>
</table>

## Parametri

<b>Passaggi</b> *Intero* Numero di valori separati a cui deve essere approssimato l&#39;intervallo di input.

<b>Scostamento</b> *Mobile* Applica un offset all&#39;intervallo di input, che *sposta* i risultati lungo l&#39;intervallo.

<b>Pendenza</b> *Mobile* Applica una sfumatura pendenza alle *transizioni* tra valori approssimati, fino all&#39;*intera estensione di un passaggio*.

<b>Pendenza curva</b> *Numero intero* Imposta il metodo di acquisizione della curva per la pendenza impostata dal parametro <b>Pendenza</b>:
* *Lineare*: applica una curva lineare, creando una pendenza retta
* *Smoothstep*: applica una curva smoothstep, creando una pendenza uniforme
* *Input curva*: applica la curva descritta dalla mappa di input <b>Input curva</b>. È possibile utilizzare un nodo [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) per descrivere questa curva con una grande quantità di controllo.

## Esempi

![Esempio 1](../../../../../../assets/quantizegrayscale.gif "Esempio 1")

![Esempio 2](../../../../../../assets/quantizegrayscale.png "Esempio 2")
