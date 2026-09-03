---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Utilizzate il nodo Trasformazione sicura per applicare le trasformazioni mantenendo i bordi della texture ed evitando gli artefatti.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione sicura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# Trasformazione sicura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform-01.png)

![](safe-transform.resources/safe-transform-02.png)

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione di [Trasformazione 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) sicura per la stampa in porzioni. Consente di ridimensionare, ruotare e scostare senza interrompere le porzioni e senza perdere i dettagli dei pixel (perdita di nitidezza/nitidezza) a causa di piccoli scostamenti e rotazioni.

Utile per la trasformazione del disturbo quando è necessario il massimo controllo o la nitidezza perfetta.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Affianca</b> <i>1 - 16</i> | Riduce l&#39;input mediante l&#39;Affiancamento. |
| <b>Modalità offset</b> <i>Manuale, Casuale</i> | Passa a uno scostamento casuale anziché a uno definito manualmente. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Verifica che i pixel siano allineati e non interpolati. |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota l&#39;input lungo l&#39;angolo. |
| <b>Rotazione sicura riquadro</b> <i>Falso/Vero</i> | Determina il comportamento della Rotazione, se deve essere agganciata a valori sicuri che non sfocano alcun pixel. |
| <b>Simmetria</b> <i>nessuno, X, Y, X+Y</i> |  |
| <b>Colore di sfondo</b> <i>(Valore colore) (Solo versione colore)</i> |  |
| <b>Modalità Mipmap</b> <i>Automatico, Manuale</i> | Determina la modalità mipmapping. Impostando questa opzione su Manuale si ottengono risultati più nitidi. |
| <b>Livello mipmap</b> <i>0 - 10</i> | Quando la modalità Mipmap è impostata su Manuale, è possibile scegliere una Mipmap diversa. |
