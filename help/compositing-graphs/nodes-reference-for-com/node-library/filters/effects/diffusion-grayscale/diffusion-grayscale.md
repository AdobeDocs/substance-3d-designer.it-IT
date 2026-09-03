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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# Scala di grigi diffusione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-01.png){width="200px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applicate un processo di diffusione ai valori nell&#39;input dell&#39;immagine **Sorgente** in base all&#39;input dell&#39;immagine **Maschera** fornito, creando gradazioni uniformi tra i valori.

Vengono diffusi solo i valori dei pixel corrispondenti alla maschera; gli altri pixel non partecipano al risultato.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Origine</b> <i>Scala di grigi</i> | Immagine da diffondere. |
| <b>Maschera</b> <i>Scala di grigi</i> | Maschera di diffusione: i pixel bianchi vengono campionati in <i>Sorgente</i> e diffusi in pixel neri. L’immagine deve essere in bianco e nero. Se la maschera include sfumature, il valore di taglio è 0,5. |
| <b>Intensità</b> <i>Scala di grigi</i> | Definisce localmente la forza con cui viene applicato il processo di diffusione. Questa mappa dovrebbe essere <i>in contrasto</i> per ottenere un effetto evidente. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Iterazioni</b> <i>0.0 - 64.0</i> | Numero di iterazioni di diffusione da eseguire (maggiore è migliore ma più lento). I valori utili sono compresi nell’intervallo [8, 48].<br>Si noti che se non si cerca la correttezza matematica, i valori bassi sono corretti o addirittura migliori. |
| <b>Distanza</b> <i>0.0 - 1.0</i> | Regola la distanza massima della diffusione. |
| <b>Abilita dithering</b> <i>Vero/Falso</i> | Controlla il metodo di campionamento di ogni passata. Il dithering consente la convergenza in meno passaggi, ma introduce disturbi.<br>In caso contrario, ogni passaggio è più veloce, ma sono necessarie più passaggi per ottenere un risultato uniforme senza artefatti di striatura. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-07.jpg" />
        </td>
    </tr>
</table>
