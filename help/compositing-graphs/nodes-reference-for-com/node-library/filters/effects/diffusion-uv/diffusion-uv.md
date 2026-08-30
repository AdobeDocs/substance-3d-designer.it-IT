---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# UV diffusione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-icon.png){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applicate un processo di diffusione alle coordinate UV nell&#39;input dell&#39;immagine **Sorgente** in base all&#39;input dell&#39;immagine **Maschera** fornito, interpolando le coordinate tra i valori della **Sorgente**.

Vengono diffusi solo gli UV dei pixel corrispondenti alla maschera; gli altri pixel non partecipano al risultato.

Si noti che la suddivisione in porzioni viene gestita in modo speciale: quando la suddivisione in porzioni è *abilitata* (che è il caso per impostazione predefinita), è possibile calcolare la media delle coordinate adiacenti per il limite 0/1.

Ad esempio, se il valore della coordinata U è 0,1 su un pixel e 0,8 su un altro, il valore medio sarà 0,95 anziché 0,45 perché si presuppone che *le coordinate siano affiancate*. Ciò è indipendente dalla posizione effettiva dei pixel: i valori delle coordinate vengono gestiti allo stesso modo in tutta l’immagine.

Ciò può portare a risultati indesiderati quando si utilizza questo filtro per *deformazioni della texture*. In tal caso, assicurati che la maschera definisca &quot;curve/punti di controllo&quot; a non più di *mezza lunghezza della texture*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Origine</b> <i>Colore</i> | UV da diffondere. In questo filtro la suddivisione in porzioni viene gestita in modo speciale (vedere <i>Descrizione</i>). |
| <b>Maschera</b> <i>Scala di grigi</i> | Maschera di diffusione: i pixel bianchi vengono campionati in <i>Sorgente</i> e diffusi in pixel neri. L’immagine deve essere in bianco e nero. Se la maschera include sfumature, il valore di taglio è 0,5. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Iterazioni</b> <i>0.0 - 64.0</i> | Numero di iterazioni di diffusione da eseguire (maggiore è migliore ma più lento). I valori utili sono compresi nell’intervallo [8, 48].<br>Si noti che se non si cerca la correttezza matematica, i valori bassi sono corretti o addirittura migliori. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>
