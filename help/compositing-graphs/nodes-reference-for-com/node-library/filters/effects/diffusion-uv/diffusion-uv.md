---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Utilizzate il nodo UV Diffusione per applicare effetti di diffusione nello spazio UV per creare transizioni di colore uniformi e fusione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV diffusione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# UV diffusione

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**Ingresso:** *Filtri/Effetti*

**Intermedio**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Applicate un processo di diffusione alle coordinate UV nell&#39;input dell&#39;immagine **Sorgente** in base all&#39;input dell&#39;immagine **Maschera** fornito, interpolando le coordinate tra i valori della **Sorgente**.

Vengono diffusi solo gli UV dei pixel corrispondenti alla maschera; gli altri pixel non partecipano al risultato.

Si noti che la suddivisione in porzioni viene gestita in modo speciale: quando la suddivisione in porzioni è *abilitata* (che è il caso per impostazione predefinita), è possibile calcolare la media delle coordinate adiacenti per il limite 0/1.

Ad esempio, se il valore della coordinata U è 0,1 su un pixel e 0,8 su un altro, il valore medio sarà 0,95 anziché 0,45 perché si presuppone che *le coordinate siano affiancate*. Ciò è indipendente dalla posizione effettiva dei pixel: i valori delle coordinate vengono gestiti allo stesso modo in tutta l’immagine.

Ciò può portare a risultati indesiderati quando si utilizza questo filtro per *deformazioni della texture*. In tal caso, assicurati che la maschera definisca &quot;curve/punti di controllo&quot; a non più di *mezza lunghezza della texture*.

</td>
</tr>
</table>

## Parametri

* **Iterazioni**: *0.0 - 64.0* Numero di iterazioni di diffusione da eseguire (maggiore è il numero migliore, ma più lento). I valori utili sono compresi nell’intervallo [8, 48].\
  Si prega di notare che se non si cerca la correttezza matematica, i valori bassi sono buoni o anche meglio.

## Input

* **Origine** *Colore*\
  UV da diffondere. In questo filtro la suddivisione in porzioni viene gestita in modo speciale (vedere *Descrizione*).
* **Maschera** *Scala di grigio* Maschera di diffusione: i pixel bianchi vengono campionati in *Sorgente* e diffusi in pixel neri. L’immagine deve essere in bianco e nero. Se la maschera include sfumature, il valore di taglio è 0,5.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
