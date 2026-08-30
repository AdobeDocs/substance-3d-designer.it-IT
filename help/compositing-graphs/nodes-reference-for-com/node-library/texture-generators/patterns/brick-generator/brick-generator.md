---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Utilizzare il nodo Brick Generator per creare pattern di mattoni procedurali con proprietà personalizzabili di dimensioni, scostamento e malta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore mattoni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# Generatore mattoni

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator.png){width="128px"}

<b>Ingresso:</b> Generatori texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Generatore avanzato di pattern mattone. Ha molte opzioni per la generazione specifica di modelli di mattoni artificiali

Per ulteriori opzioni, vedere [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Mattoni</b> <i>1 - 64</i> | Imposta la quantità di mattoni lungo gli assi X e Y. |
| <b>Smussato</b> <i>0.0 - 1.0</i> | Modifica il profilo di smussatura dei mattoni, consente di effettuare modifiche in due direzioni e di impostare il profilo di decadimento e l’arrotondamento degli angoli. |
| <b>Mantieni rapporto</b> <i>Falso/Vero</i> | Rende il profilo Smussato legato o meno alla dimensione del mattone. |
| <b>Spazio vuoto</b> <i>0.0 - 1.0</i> | Spazio tra i mattoni. Tenete presente che anche la Smussatura introduce uno spazio vuoto; pertanto, impostare lo stesso valore per le smussature significa che dovete compensare con questo parametro. |
| <b>Dimensioni Medie</b> <i>0.0 - 1.0</i> | Scostamento motivo mattone, modifica le dimensioni di ogni altra colonna o riga. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Modifica i profili di height. Consente di introdurre la variazione di luminanza e tutti i tipi di randomizzazione. |
| <b>Pendenza</b> <i>-1.0 - 1.0</i> | Introduce una pendenza per mattoni, come se alcuni mattoni si trovassero in un angolo. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta i mattoni in base alla riga, influisce sulla spaziatura per riga. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>
