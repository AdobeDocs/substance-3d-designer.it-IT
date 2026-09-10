---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Usa il nodo di Trasforma non quadrato per applicare le trasformazioni alle texture non quadrate con ridimensionamento X e Y indipendente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione non quadrata
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# Trasformazione non quadrata

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/safe-transform.png)

![](non-square-transform.resources/safe-transform-grayscale.png)

<b>Ingresso:</b> Filtri > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione non quadrata sicura di [Trasforma 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Rileva automaticamente le proporzioni non quadrate e può Trasforma immagini di input quadrate in un&#39;area di lavoro non quadrata.

Assicurati di aver compreso appieno i [parametri del grafico](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)per utilizzare al meglio questo nodo, in quanto dovrai impostare alcune impostazioni correttamente:

* La dimensione del **grafico** deve essere non quadrata, altrimenti non è necessario questo nodo.
* Imposta la dimensione dell&#39;output **del nodo** del Trasforma non quadrato su &quot;*Rispetto al padre*&quot;.
* Impostare la modalità di Affiancamento **del nodo** su &quot;*Nessun Affiancamento*&quot; se si desidera Trasforma l&#39;input in un&#39;unica posizione.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità riquadro</b> <i>Automatico, Manuale</i> | Abilita o meno le compensazioni automatiche non quadrate. |
| <b>Affianca</b> <i>1 - 16</i> | Accessibile solo quando la modalità Affianca è impostata su Manuale. Consente di modificare la scala in modo sicuro per gli Affiancamenti. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Fai doppio clic sul cursore per immettere i valori negativi. |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota l&#39;immagine di input. |
| <b>Rotazione sicura (solo quadrato)</b> <i>Falso/Vero</i> | Aggancia a valori sicuri per mantenere la nitidezza dei pixel. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Colore di sfondo con cui riempire l’immagine. Visibile solo quando [Modalità affiancamento nei parametri di base è impostato su &quot;*Nessun Affiancamento*&quot;](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md). |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/nonsquare-ex.png" />
        </td>
    </tr>
</table>
