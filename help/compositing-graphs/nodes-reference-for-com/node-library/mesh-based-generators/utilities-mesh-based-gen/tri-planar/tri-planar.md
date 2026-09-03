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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# Triplo Planare

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/tri-planar-01.png){width="128px"}

![](tri-planar.resources/tri-planar-02.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Utility

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo avanzato esegue la mappatura della proiezione triplanare in 2D, in base ai dati di posizione e di World Space Normal. Ciò significa che in pratica converte completamente le coordinate UV in una mappatura (per lo più) libera dalla giuntura basata sulla trama stessa.

Questo è un buon modo per evitare cuciture senza dover rifare ogni volta (è possibile ottenere qualcosa di simile con il fornaio). Il lato negativo è che questo nodo è piuttosto pesante e quindi non veloce.

Tieni presente che i tuoi dolci dovrebbero essere ad alta precisione: i dolci a 8 bit non porteranno a risultati molto belli.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Posizione</b> <i>Input colore</i> | Mappa posizione al forno. Idealmente precisione di 16 bit o superiore. |
| <b>Spazio globale normale</b> <i>Input colore</i> | Mappa Normale dello Spazio Mondiale al forno, preferibilmente con precisione di 16 bit o superiore. |
| <b>Input X</b> <i>Input colore (input scala di grigi)</i> | Mappa di input da mappare dai raggi UV allo spazio mondiale tramite proiezione triplanare. Utilizzato per tutti gli assi quando Image Inputs è impostato su 1, per l&#39;asse X se è impostato su 3. |
| <b>Input Y</b> <i>Input colore (input scala di grigi)</i> | Solo se Image Inputs è impostato su 3. Mappa di input per il mapping dai raggi UV allo spazio globale sull&#39;asse Y. |
| <b>Input Z</b> <i>Input colore (input scala di grigi)</i> | Solo se Image Inputs è impostato su 3. Mappa di input per il mapping dai raggi UV allo spazio globale sull&#39;asse Z. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Proiezione</b> <i>Tutti gli assi, solo X, solo Y, solo Z</i> | Imposta gli assi con cui creare una fusione. |
| <b>Input immagine</b> <i>1 input, 3 input</i> | Impostare se utilizzare una mappa per tutti gli assi o una mappa specifica per asse. |
| <b>Metodo fusione</b> <i>lineare, avanzato</i> | Aumenta la precisione. |
| <b>Fusione del contrasto</b> <i>0.001 - 1.0</i> | Contrasto di transizione, fusione tra transizioni morbide o dure. |
| <b>Fattore di normalizzazione</b> <i>0.0 - 1.0</i> | Migliora la fusione della proiezione ripristinando la perdita di contrasto nell’area di fusione. |
| <b>Affiancamento Texture</b> <i>0.0 - 10.0</i> | Numero di volte in cui affiancare le texture di input. |
| <b>Rotazione globale</b> <i>0.0 - 1.0</i> | Rotazione globale per tutti gli assi. |
| <b>Correggi proiezione con mirroring</b> <i>Falso/Vero</i> | Impostare la modalità di gestione delle proiezioni specchiate. |
| <b>Rotazione X</b> <i>0.0 - 1.0</i> | Rotazione individuale sull&#39;asse X della proiezione. |
| <b>Rotazione Y</b> <i>0.0 - 1.0</i> | Rotazione individuale sull&#39;asse Y della proiezione. |
| <b>Rotazione Z</b> <i>0.0 - 1.0</i> | Rotazione individuale sull&#39;asse Z della proiezione. |
| <b>Scostamento X</b> <i>0.0 - 1.0</i> | Offset sull&#39;asse X della proiezione. |
| <b>Scostamento Casuale X</b> <i>0.0 - 1.0</i> | Consente la randomizzazione dell’offset dell’asse X. |
| <b>Scostamento Y</b> <i>0.0 - 1.0</i> | Offset sull&#39;asse Y della proiezione. |
| <b>Scostamento casuale Y</b> <i>0.0 - 1.0</i> | Consente la randomizzazione dell’offset dell’asse Y. |
| <b>Scostamento Z</b> <i>0.0 - 1.0</i> | Offset sull&#39;asse Z della proiezione. |
| <b>Scostamento casuale Z</b> <i>0.0 - 1.0</i> | Consente la randomizzazione dell’offset dell’asse Z. |
