---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Utilizza il nodo Generatore Scratches per creare pattern di graffi procedurali per aggiungere usura e danni ai materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore Scratches
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 8%

---


# Generatore Scratches

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](scratches-generator.resources/scratches-generator.png)

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

In questo modo si creano graffi casuali con molte opzioni di personalizzazione, ad esempio per impostare direzione, pagine affiancate e distorsione.

Esiste una versione speciale di Generatore di Scratches, Normale di Generatore di Scratches, che genera Normalmap basate sulla profondità di questi graffi. La maggior parte delle opzioni è esattamente la stessa, ma ha alcuni parametri aggiuntivi chiaramente contrassegnati per le impostazioni Normale (vedi di seguito).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Numero spline</b> <i>1 - 512</i> | Quantità di graffi (spline) da inserire. |
| <b>Numero Massimo Di Segmenti Per Spline</b> <i>2 - 256</i> | Quantità di segmenti/suddivisioni sulla lunghezza di un graffio. Porta a curve e distorsioni più uniformi. L’effetto è più evidente con valori di Distorsione più alti. |
| <b>Rotazione spline</b> <i>0.0 - 1.0</i> | Rotazione uniforme di tutte le spline per orientarle in una direzione. |
| <b>Rotazione spline casuale</b> <i>0.0 - 1.0</i> | Variazione dell&#39;angolo, ruota casualmente ogni spline. |
| <b>Scala spline</b> <i>0.0 - 1.0</i> | Ridimensiona in modo uniforme tutte le spline. |
| <b>Scala spline casuale</b> <i>0.0 - 1.0</i> | Ridimensiona ogni spline in modo casuale singolarmente. |
| <b>Distorsione spline</b> <i>0.0 - 1.0</i> | Livello di distorsione uniforme su tutte le spline. |
| <b>Distorsione spline casuale</b> <i>0.0 - 1.0</i> | Rende casuale il livello di distorsione di ogni spline singolarmente. |
| <b>Frequenza Distorsione spline</b> <i>0.0 - 1.0</i> | Consente di impostare la frequenza della distorsione e di controllare la scala dei dettagli della distorsione. |
| <b>Larghezza spline</b> <i>0.0 - 2.0</i> | Imposta la larghezza di tutte le spline in modo uniforme. |
| <b>Larghezza spline casuale</b> <i>0.0 - 1.0</i> | Rende casuale la larghezza della spline di ogni spline singolarmente. |
| <b>Posizione spline casuale</b> <i>0.0 - 1.0</i> | Rende casuale la posizione di ogni spline singolarmente. Più è basso questo valore, più spline si raggrupperanno al centro dell&#39;area di lavoro. Può essere utilizzato per creare macchie di graffi. |
| <b>Imposta larghezza spline in px</b> <i>Falso/Vero</i> | Determina le unità utilizzate per le impostazioni della larghezza della spline. |
| <b>Luminanza casuale (solo versione in scala di grigio)</b> <i>0.0 - 1.0</i> | Rende casuale la Luminanza di ogni spline singolarmente. |
| <b>Intensità normale (solo versione normale)</b> <i>0.0 - 1.0</i> | Imposta l&#39;intensità dell&#39;effetto Normale per ogni spline a livello globale. |
| <b>Intensità normale casuale (solo versione normale)</b> <i>0.0 - 1.0</i> | Rende casuale l&#39;intensità normale di ogni spline singolarmente. |
| <b>Formato normale (solo versione normale)</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Modalità dissolvenza</b> <i>Nessuno, Inizio, Fine, Inizio + Fine</i> | Consente di impostare se e in quale direzione le spline vengono dissolte. |
| <b>Lunghezza dissolvenza</b> <i>0.0 - 1.0</i> | Consente di impostare la lunghezza dell’effetto di dissolvenza, se attivato in precedenza. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="scratches-generator.resources/scratches-ex2.png" />
        </td>
    </tr>
</table>
