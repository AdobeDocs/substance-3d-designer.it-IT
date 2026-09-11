---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Utilizzate il nodo Bagliore per aggiungere effetti di bagliore alle texture per creare aspetti di materiale luminoso e emissivo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bagliore
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# Bagliore

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](glow.resources/glow-greyscale.png){width="128px"}

![](glow.resources/glow-3.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue un effetto del tipo &quot;Bagliore esterno&quot;, tipico di altri software di editing di immagini molto diffusi. In sostanza, aggiunge un contorno sfumato di dissolvenza attorno all’input.

Tenete presente che questa opzione non è adatta per immagini con Canali alfa, come potreste aspettarvi. Anche la versione a colori si aspetta solo maschere binarie, in bianco e nero come input; consente solo di utilizzare un bagliore colorato. Se state seguendo una versione che funziona su immagini con trasparenza, consultate [Bagliore forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Glow&quot; per gli input di colore o &quot;Glow Greyscale&quot; per gli input di scala di grigio.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Quantità bagliore</b> <i>0.0 - 1.0</i> | Opacità globale per l’effetto bagliore. |
| <b>Cancella quantità</b> <i>0.0 - 1.0</i> | Soglia massima per quando interrompere l’effetto bagliore. Utile per aree semitrasparenti. |
| <b>Dimensione bagliore</b> <i>0.0 - 20.0</i> | Controlla il valore raggiunto dall’effetto bagliore. |
| <b>Colore bagliore</b> <i>(Valore colore) (Solo versione colore)</i> | Consente di impostare il colore dell’effetto bagliore. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="glow.resources/glow-ex.png" />
        </td>
    </tr>
</table>
