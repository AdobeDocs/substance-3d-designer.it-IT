---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: Usa il nodo Trasformazione 2D per applicare trasformazioni 2D alle texture, tra cui traslazione, rotazione e ridimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Trasformazione 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# Trasformazione 2D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: trasformazione 2D](../../../../assets/comp_transformation_1.png "Nodo atomico: trasformazione 2D"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Applica all’immagine una matrice di trasformazione 2D: traslazione, rotazione, ridimensionamento, simmetria e inclinazione.

È molto simile a Trasformazione (Ctrl-T) in Photoshop o all’utilizzo del manipolatore di mappatura 2D in Substance 3D Painter.

</td>
</tr>
</table>

Si tratta di un nodo estremamente utile e ampiamente applicato, che consente di aumentare la suddivisione in porzioni, rimuovere la suddivisione in porzioni, posizionare un&#39;immagine in una posizione specifica, allungare o schiacciare un input, ecc.

Tuttavia, non può essere perfetto per alcune applicazioni, quindi i seguenti nodi possono essere interessanti: [Trasformazione sicura](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md), [Trasformazione non quadrata](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md), [Trasformazione quadrata](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) e [Trasformazione trapezoidale](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Disabilitazione della suddivisione in porzioni
> 
> Impostare il [metodo di ereditarietà](../../../../glossary/glossary.md) del parametro di base [&#x200B; &#39;Tiling mode&#39; &#x200B;](../../../../glossary/glossary.md) su &#39;Absolute&#39;, che consente di impostare il valore del parametro su &#39;No Tiling&#39;:
> 
> ![](../../../../assets/tilingmode.png)

>[!NOTE]
>
> I valori di ridimensionamento e rotazione nelle proprietà del nodo sono *relativi alla trasformazione corrente* e non vengono applicati alla vista 2D finché non si fa clic sul pulsante &#39;Applica&#39;.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Matrice di trasformazione</b> *Float4* | Aprite la matrice di trasformazione sottostante per la modifica diretta. Consente di modificare la rotazione e il ridimensionamento. Può essere regolato anche tramite il gizmo nella vista 2D.   Avvertenza: non sono correlate direttamente alla vista e sono regolazioni relative che possono essere applicate in più passaggi. |
| <b>Scostamento</b> *Float2* | Definisce lo spostamento 2D dell’immagine. Consente di modificare la posizione o lo scostamento. Può essere regolato anche tramite il gizmo nella vista 2D.   Si riferisce direttamente all&#39;output della vista 2D. |
| <b>Modalità Mipmap</b> *Numero intero* | Consente di passare a un livello [mipmap](../../../../glossary/glossary.md) manuale, che riduce gli artefatti in un&#39;immagine utilizzando il filtro delle texture. |
| <b>Livello mipmap</b> *Numero intero* | Imposta il livello [mipmap](../../../../glossary/glossary.md) da utilizzare.     *Disponibile quando la modalità Mipmap è impostata su Manuale* |
| <b>Colore mascherino</b> *Float4* | Il colore utilizzato come sfondo quando la suddivisione in porzioni della trasformazione è disattivata. Imposta il colore usato quando l&#39;input trasformato non copre un&#39;area dell&#39;output.   Può essere reso trasparente se si lavora con il colore RGBA. |
| <b>Filtraggio</b> *Numero intero* | Imposta il metodo di downsampling utilizzato. Non funziona particolarmente bene con la riduzione del Livello mipmap. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | Immagine da trasformare. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
