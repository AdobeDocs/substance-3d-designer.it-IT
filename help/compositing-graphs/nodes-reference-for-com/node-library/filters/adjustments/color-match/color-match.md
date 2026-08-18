---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Utilizza il nodo Corrispondenza colori per far corrispondere i colori tra le texture per creare tavolozze di colori coerenti e armonizzare le texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corrispondenza colori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Corrispondenza colori

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## Corrispondenza colori

**Ingresso:** *Filtri/Regolazioni*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Tenta di trovare una corrispondenza tra l&#39;intervallo definito di *Colore di origine* e un intervallo di *Colore di destinazione*, con supporto per gli slot di input per definire Origine e Destinazione.

Per versioni più semplici, consulta [Sostituisci intervallo colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) o [Sostituisci colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

## Parametri

### Input

* **Input**: input *Color*\
  Input principale da modificare per il risultato.
* **Colore di origine**: *Input colore*\
  Slot di input per il colore di origine, utilizzato solo quando &quot;Metodo colore di origine&quot; è impostato su *Input*.
* **Colore di destinazione**: *Input colore* Slot di input per il colore di destinazione, utilizzato solo quando &quot;Metodo colore di destinazione&quot; è impostato su *Input*.

### Parametri

* **Metodo colore di origine**: *Media, Parametro, Input* Imposta se il colore di origine è definito calcolando la media dell&#39;immagine di input, impostando un parametro o utilizzando uno slot di input.
* **Colore di origine**: *(valore colore)* Se Metodo colore di origine è impostato su *Parametro*, questo parametro determina il colore di origine.
* **Modalità colore di destinazione**: *Parametro, Input immagine* Imposta se il colore di origine è definito calcolando la media dell&#39;immagine di input, impostando un parametro o utilizzando uno slot di input.
* **Colore di destinazione**: *(valore colore)* Se Metodo colore di destinazione è impostato su *Parametro*, questo parametro determina il colore di destinazione.
* **Variazione colore personalizzata**: False/True\
  Abilita una variazione di colore aggiuntiva.
* **Variazione colore**\
  Imposta le variazioni di tonalità, crominanza o luminanza sul risultato, se attivate.
* **Usa maschera**: *False/True*\
  Attiva/disattiva l’utilizzo di Input maschera o Output, a seconda della Modalità maschera riportata di seguito.
* **Modalità maschera**: *Il parametro, l&#39;input* la modalità parametro genera una maschera che descrive in dettaglio come è cambiato il colore. La modalità di input consente a una maschera di controllare l’intensità dell’effetto Corrispondenza colore.
* **Maschera**\
  Genera una maschera che mostra esattamente dove è stato applicato l’effetto Corrispondenza colore, con controlli aggiuntivi per smussare e sfocare la maschera risultante.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
