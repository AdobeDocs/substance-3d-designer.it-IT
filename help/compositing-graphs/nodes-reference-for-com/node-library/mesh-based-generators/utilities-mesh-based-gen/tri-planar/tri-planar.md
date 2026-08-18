---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Utilizzate il nodo Piano trim (Tri Planar) per proiettare le texture da tre piani ortogonali per una mappatura uniforme delle texture su geometria complessa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triplo Planare
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Triplo Planare

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## Triplo Planare (Scala Di Grigi)

**Ingresso:** *Generatori Basati Su Trama**/Utility*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo avanzato esegue la mappatura della proiezione triplanare in 2D, in base ai dati di posizione e di World Space Normal. Ciò significa che in pratica converte completamente le coordinate UV in una mappatura (per lo più) libera dalla giuntura basata sulla trama stessa.

Questo è un buon modo per evitare cuciture senza dover rifare ogni volta (è possibile ottenere qualcosa di simile con il fornaio). Il lato negativo è che questo nodo è piuttosto pesante e quindi non veloce.

Tieni presente che i tuoi dolci dovrebbero essere ad alta precisione: i dolci a 8 bit non porteranno a risultati molto belli.

## Parametri

### Input

* **Posizione**: *Input colore*\
  Mappa posizione al forno. Idealmente precisione di 16 bit o superiore.
* **Spazio Mondiale Normale**: *Input Colore*\
  Mappa Normale dello Spazio Mondiale al forno, preferibilmente con precisione di 16 bit o superiore.
* **Input X**: *Input colore (input scala di grigi)*Mappa di input da mappare da UV a World Space tramite proiezione triplanare. Utilizzato per tutti gli assi quando Image Inputs è impostato su 1, per l&#39;asse X se è impostato su 3.
* **Input Y**: *Input colore (input scala di grigi)*Solo se Image Inputs è impostato su 3. Mappa di input per il mapping dai raggi UV allo spazio globale sull&#39;asse Y.
* **Input Z**: *Input colore (input scala di grigi)*Solo se Image Inputs è impostato su 3. Mappa di input per il mapping dai raggi UV allo spazio globale sull&#39;asse Z.

### Parametri

* **Proiezione**: *Tutti gli assi, solo X, solo Y, solo Z* Imposta gli assi con cui creare una fusione.
* **Input immagine**: *1 input, 3 input*\
  Impostare se utilizzare una mappa per tutti gli assi o una mappa specifica per asse.
* **Metodo fusione**: *lineare, avanzato* Aumenta la precisione.
* **Contrasto di fusione**: *0.001 - 1.0* Contrasto di transizione, fusione tra transizioni morbide o dure.
* **Fattore di normalizzazione**: *0,0 - 1,0*\
  Migliora la fusione della proiezione ripristinando la perdita di contrasto nell’area di fusione.
* **Affiancatura texture**: *0.0 - 10.0* Numero di volte in cui affiancare le texture di input.
* **Rotazione globale**: *0.0 - 1.0*\
  Rotazione globale per tutti gli assi.
* **Correggi proiezioni con mirroring**: *False/True* Imposta come gestire le proiezioni con mirroring.
* **Rotazione X**: *0,0 - 1,0* Rotazione individuale sull&#39;asse X della proiezione.
* **Rotazione Y**: *0,0 - 1,0* Rotazione individuale sull&#39;asse Y della proiezione.
* **Rotazione Z**: *0,0 - 1,0* Rotazione individuale sull&#39;asse Z della proiezione.
* **Scostamento X**: *0,0 - 1,0* Scostamento sull&#39;asse X della proiezione.
* **Scostamento Casuale X**: *0,0 - 1,0*\
  Consente la randomizzazione dell’offset dell’asse X.
* **Scostamento Y**: *0,0 - 1,0* Scostamento sull&#39;asse Y della proiezione.
* **Scostamento casuale Y**: *0,0 - 1,0*\
  Consente la randomizzazione dell’offset dell’asse Y.
* **Scostamento Z**: *0,0 - 1,0* Scostamento sull&#39;asse Z della proiezione.
* **Scostamento casuale Z**: *0,0 - 1,0*\
  Consente la randomizzazione dell’offset dell’asse Z.

## Immagini di esempio

</td>
</tr>
</table>
