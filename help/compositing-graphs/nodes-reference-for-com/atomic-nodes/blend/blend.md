---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: Utilizzate il nodo Fusione per fondere due texture insieme utilizzando vari metodi di fusione per creare effetti compositi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fusione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# Fusione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Fusione](blend.resources/comp_blend_1.png "Nodo atomico: Fusione"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Combina due immagini usando un metodo di fusione specificato e una maschera facoltativa.

È il nodo più utile di tutti i nodi atomici, quasi tutti i grafici creati in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) utilizzeranno questo nodo.

</td>
</tr>
</table>

La sua funzionalità è simile a quella di due livelli sovrapposti in [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) o [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html), che si fondono insieme in base al metodo di fusione impostato sul livello superiore.

>[!TIP]
>
> Scopri i metodi di fusione disponibili nel nodo Fusione in [questa pagina dedicata](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md).

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
| <b>Opacità</b> *Mobile* | Opacità del livello di primo piano che si fonde con lo sfondo. Funziona indipendentemente dall’input Opacità e funge da moltiplicatore aggiuntivo. |
| <b>Metodo fusione</b> *Intero* [Statico](../../../../glossary/glossary.md) | Imposta l&#39;operazione di fusione da utilizzare.   Consulta la [pagina dedicata sui metodi di fusione](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md). |
| <b>Fusione Alpha</b> *Intero* [Statico](../../../../glossary/glossary.md) | Determina il comportamento di fusione quando gli input di colore hanno canali di Alpha:<ul data-preserve-html="true"> <li data-preserve-html="true">Usa alfa sorgente</li> <li data-preserve-html="true">Ignora alfa</li> <li data-preserve-html="true">Fusione alfa semplice</li> <li data-preserve-html="true">Fusione alfa premoltiplicata</li> </ul> |
| <b>Area di ritaglio</b> *Float4* [Statico](../../../../glossary/glossary.md) | Consente di impostare un’area di ritaglio personalizzata che si comporti come una maschera di opacità aggiuntiva. Qualsiasi area ritagliata mostra solo lo sfondo. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Primo piano</b> *Scala di grigi/Colore* | Livello superiore o di primo piano dell’operazione Fusione. |
| <b>Sfondo</b> *Scala di grigi/Colore* PRIMARIO | Livello inferiore o di sfondo dell&#39;operazione di fusione. |
| <b>Opacità</b> *Scala di grigi* | Input maschera di Alpha opzionale. |

>[!IMPORTANT]
>
> I nodi Fusione dispongono di input dinamici che passano da Scala di grigio a Colore a seconda delle connessioni.<b> Un nodo Fusione può unire solo due input dello stesso tipo</b>.
> 
> Collegando un input a colori e in scala di grigi a primo piano e sfondo si ottiene una linea di connessione tratteggiata rossa, a indicare un errore di calcolo.
> 
> Questo è il motivo principale per cui i nuovi utenti incontrano problemi con le connessioni a colori e in scala di grigi: assicurati che entrambe le connessioni siano dello stesso tipo!

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
