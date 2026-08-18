---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Trasformazione sicura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Trasformazione sicura (scala di grigi)

**Entrata:** *Filtri/Trasformazioni*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Versione di [Trasformazione 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) sicura per la stampa in porzioni. Consente di ridimensionare, ruotare e scostare senza interrompere le porzioni e senza perdere i dettagli dei pixel (perdita di nitidezza/nitidezza) a causa di piccoli scostamenti e rotazioni.

Utile per la trasformazione del disturbo quando è necessario il massimo controllo o la nitidezza perfetta.

## Parametri

* **Affianca**: *1 - 16* Ridimensiona l&#39;input affiancandolo.
* **Modalità scostamento**: *Manuale, casuale* Passa a uno scostamento casuale anziché a uno definito manualmente.
* **Scostamento**: *0,0 - 1,0*\
  Sposta o converte il risultato. Verifica che i pixel siano allineati e non interpolati.
* **Rotazione**: *0.0 - 1.0* Ruota l&#39;input lungo l&#39;angolo.
* **Rotazione sicura porzione**: *False/True* Determina il comportamento della rotazione e se deve essere agganciata a valori sicuri che non sfocano alcun pixel.
* **Simmetria**: *nessuna, X, Y, X+Y*
* **Colore sfondo**: *(Valore colore) (Solo versione colore)*
* **Modalità Mipmap**: *Automatica, Manuale* Determina la modalità Mipmapping. Impostando questa opzione su Manuale si ottengono risultati più nitidi.
* **Livello mipmap**: *0 - 10* Quando la modalità Mipmap è impostata su Manuale, consente di scegliere una Mipmap diversa.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
