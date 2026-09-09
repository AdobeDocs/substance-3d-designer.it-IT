---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/anisotropic-blur.html"
breadcrumb-title: ''
description: Utilizzate il nodo Sfocatura anisotropa per applicare effetti di sfocatura direzionale per creare effetti di sfocatura movimento e striatura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Anisotropic Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sfocatura anisotropa
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# Sfocatura anisotropa

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](anisotropic-blur.resources/anisotropic-blur-grayscale.png){width="128px"}

![](anisotropic-blur.resources/anisotropic-blur.png){width="128px"}

<b>Ingresso:</b> Filtri > Sfocature

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue una [sfocatura direzionale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-blur/directional-blur.md) di alta qualità, con alcune impostazioni per personalizzare l&#39;aspetto. Detto anche &quot;effetto movimento&quot;.

Importante: assicurati di utilizzare la versione appropriata per il tuo input. Usate &quot;Sfocatura anisotropa&quot; per gli input di colore o &quot;Scala di grigi Sfocatura anisotropa&quot; per gli input di scala di grigi.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> <i>0.0 - 16.0</i> | Intensità (raggio) della sfocatura. Più alto è questo valore, maggiore sarà la sfocatura. |
| <b>Anisotropia</b> <i>0.0 - 1.0</i> | Direzione della sfocatura. Impostare questo valore su 0,0 equivale a eseguire una sfocatura normale. |
| <b>Angolo</b> <i>0.0 - 1.0</i> | Imposta l’angolo per la direzione di sfocatura. |
| <b>Qualità</b> <i>0 - 1</i> | Consente di passare internamente da una sfocatura a [box](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) a una sfocatura HQ. Scambia in velocità per qualità. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="anisotropic-blur.resources/aniso-blur-example.gif" />
        </td>
    </tr>
</table>
