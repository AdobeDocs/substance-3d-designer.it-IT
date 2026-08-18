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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# Generatore mattoni

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## Generatore mattoni

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Generatore avanzato di pattern mattone. Ha molte opzioni per la generazione specifica di modelli di mattoni artificiali

Per ulteriori opzioni, vedere [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

## Parametri

* **Mattoni**: *1 - 64* Imposta la quantità di mattoni sia sull&#39;asse X che sull&#39;asse Y.
* **Smussato**: *0.0 - 1.0* Modifica il profilo della smussatura per i mattoni, consente di cambiare in due direzioni e di impostare il profilo di decadimento e l&#39;arrotondamento degli angoli.
* **Mantieni proporzioni**: *False/True* Il profilo dello smusso è legato o meno alle dimensioni del mattone.
* **Spazio**: *0.0 - 1.0* Spazio da lasciare tra i mattoni. Tenete presente che anche la Smussatura introduce uno spazio vuoto; pertanto, impostare lo stesso valore per le smussature significa che dovete compensare con questo parametro.
* **Dimensioni medie**: *0.0 - 1.0* Scostamento pattern mattone, modifica le dimensioni di ogni altra colonna o riga.
* **Height**: *-1.0 - 1.0* Modifica i profili di height. Consente di introdurre la variazione di luminanza e tutti i tipi di randomizzazione.
* **Pendenza**: *-1.0 - 1.0* Introduce una pendenza per mattone, come se alcuni mattoni si trovassero in un angolo.
* **Scostamento**: *0,0 - 1,0*\
  Sposta i mattoni in base alla riga, influisce sulla spaziatura per riga.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.

## Immagini di esempio

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
