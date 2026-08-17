---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Utilizzate il nodo Dust per generare maschere di accumulo dust basate sulla geometria della trama per creare effetti di dust e grigio realistici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 1%

---


# Dust

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/dust.png){width="128px"}

## Dust

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questa maschera rappresenta un dust accumulato in aree occluse e in basso, nonché solo in aree rivolte verso l’alto. Richiede che l&#39;AO cotto e World Space Normals funzionino correttamente.

## Parametri

### Input

* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per il posizionamento dei dust. Obbligatorio!
* **Spazio Mondiale Normale**: *Input Colore*\
  Mappa con baking utilizzata per il posizionamento dei dust. Obbligatorio!
* **Disturbo**: *Input scala di grigi*\
  La mappa dust personalizzata (facoltativa) viene visualizzata solo quando l’opzione Sostituisci disturbo è impostata su True.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta l&#39;importo totale del dust.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del dust.
* **Entità Occlusione**: *0.0 - 1.0* Imposta l&#39;influenza di AO; nelle aree occluse verrà visualizzato più dust.
* **Opacità disturbo**: *0.0 - 1.0* Imposta la quantità di disturbo visibile nelle aree polverose.
* **Ignora disturbo**: *Falso/Vero* Impostato per l&#39;utilizzo dell&#39;input della mappa di dust personalizzata.

## Immagini di esempio

![](../../../../../../assets/dust-ex.gif)

</td>
</tr>
</table>
