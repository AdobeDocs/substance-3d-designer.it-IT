---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Utilizzate il nodo Diffusione scala di grigi per applicare effetti di diffusione in scala di grigi e creare transizioni di colore uniformi e fusione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scala di grigi diffusione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# Scala di grigi diffusione

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-icon.png){width="200px"}

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Applicate un processo di diffusione ai valori nell&#39;input dell&#39;immagine **Sorgente** in base all&#39;input dell&#39;immagine **Maschera** fornito, creando gradazioni uniformi tra i valori.

Vengono diffusi solo i valori dei pixel corrispondenti alla maschera; gli altri pixel non partecipano al risultato.

</td>
</tr>
</table>

## Parametri

* **Iterazioni**: *0.0 - 64.0* Numero di iterazioni di diffusione da eseguire (maggiore è il numero migliore, ma più lento). I valori utili sono compresi nell’intervallo [8, 48].\
  Si prega di notare che se non si cerca la correttezza matematica, i valori bassi sono buoni o anche meglio.\
  **Distanza**: **0.0 - 1.0** Regola la distanza massima della diffusione.
* **Attiva dithering**: *True/False* Controlla il metodo di campionamento di ogni passaggio. Il dithering consente la convergenza in meno passaggi, ma introduce disturbi.\
  Senza questa opzione, ogni passata è più veloce ma sono necessarie più passate per ottenere un risultato uniforme senza creare artefatti di banda.

## Input

* **Origine** *Scala di grigi*\
  Immagine da diffondere.
* **Maschera** *Scala di grigi*\
  Maschera di diffusione: i pixel bianchi vengono campionati in *Sorgente* e diffusi in pixel neri. L’immagine deve essere in bianco e nero. Se la maschera include sfumature, il valore di taglio è 0,5.
* **Intensità** *Scala Di Grigi*\
  Definisce localmente la forza con cui viene applicato il processo di diffusione. Questa mappa dovrebbe essere *in contrasto* per ottenere un effetto evidente.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-render.jpg){width="512px"}

</td>
</tr>
</table>
