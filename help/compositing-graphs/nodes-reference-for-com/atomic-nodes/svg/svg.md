---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ''
description: Utilizzate il nodo SVG per importare ed eseguire il rendering della grafica vettoriale di SVG come texture per la creazione di elementi grafici scalabili.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# SVG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: SVG](../../../../assets/comp_svg_1.png "Nodo atomico: SVG"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Esegue il rendering di un&#39;immagine [SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) come bitmap. In altre parole, mappa le forme vettoriali sui pixel.

Esistono alcuni modi per creare questo nodo e tutti richiedono di comprendere[la differenza tra il collegamento e l&#39;importazione delle risorse](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

</td>
</tr>
</table>

Potete creare il nodo da zero o rilasciando un file SVG nella vista Grafico.

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
> Le immagini SVG generate o importate possono essere modificate utilizzando gli [strumenti di modifica vettoriale](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) nell&#39;ancoraggio [vista 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Questo nodo dipende da una risorsa esterna, pertanto è necessario tenere presente alcuni punti quando si lavora con tali risorse:
> 
> * I nodi SVG possono restituire colore o scala di grigi, ma per impostazione predefinita il colore viene applicato anche se la risorsa è un vettore in scala di grigi. Questo può influire sulle prestazioni e sulla complessità del grafico, quindi assicuratevi sempre di passare al [metodo colore](#parameters) in scala di grigi, se necessario.
> * L&#39;eliminazione di un nodo SVG non comporta l&#39;eliminazione della [risorsa SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) nel [pacchetto](../../../../glossary/glossary.md). È necessario eseguire questa operazione manualmente in [Esplora risorse](../../../../interface/the-explorer-window/the-explorer-window.md).
> * Le forme SVG sono [tassellate](../../../../glossary/glossary.md) in geometria/poligoni, quindi *rasterizzate* per essere utilizzate nei grafici a Substance come bitmap. La tecnologia utilizzata per queste operazioni non supporta diverse proprietà vettoriali, ad esempio i contorni. Ulteriori informazioni su queste limitazioni [qui](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> Le forme SVG sono [tassellate](../../../../glossary/glossary.md) in geometria/poligoni, quindi *rasterizzate* per essere utilizzate nei grafici a Substance come bitmap.
> 
> La tecnologia utilizzata per queste operazioni non supporta diverse proprietà vettoriali, ad esempio i contorni.
> 
> Ulteriori informazioni su queste limitazioni [qui](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Esempi

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Metodo colore</b> *Booleano* | Determina il tipo di output del nodo da restituire a colori o in scala di grigio. |
| <b>Colore di sfondo</b> *Colore/Scala di grigi* | Imposta il colore di sfondo dell&#39;immagine di output da utilizzare nelle aree non coperte da una forma vettoriale.   *È sottoposto a override dall&#39;input &#39;[Background](#inputs)&#39; quando l&#39;input è connesso.* |
| <b>Percorso risorsa PKG</b> *Stringa* | Percorso della risorsa [SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) a cui fa riferimento il nodo.   Si consiglia di non digitare manualmente ma di copiare una risorsa dall&#39;elenco delle cartelle e incollarla nel campo di testo del parametro oppure di trascinare una risorsa bitmap direttamente da [Esplora risorse](../../../../interface/the-explorer-window/the-explorer-window.md) nel nodo SVG del grafico. |

## Strumenti di modifica vettoriale

Le forme vettoriali possono essere modificate in Designer. Ulteriori informazioni sugli strumenti di modifica in [questa sezione](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Sfondo</b> *Scala di grigi/Colore* PRIMARIO | Imposta il colore di sfondo dell&#39;immagine di output da utilizzare nelle aree non coperte da una forma vettoriale.   *Ignora il parametro &#39;[Colore di sfondo](#parameters)&#39; quando è connesso.* |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
