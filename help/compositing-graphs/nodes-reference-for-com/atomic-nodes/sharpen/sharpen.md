---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: Utilizzate il nodo Contrasta (Sharpen) per migliorare i dettagli e gli spigoli delle texture e creare dettagli di superficie nitidi e definiti.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nitidezza
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# Nitidezza

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Icona nodo contrasta](sharpen.resources/sharpen-4.png "Icona nodo contrasta")

<b>In:</b> Nodi Atomici

</td>
<td style="border: 0;" valign="top">

## Descrizione

Il nodo Nitidezza esegue un&#39;operazione di nitidezza su un input. È un nodo utile per applicare il tocco finale di nitidezza a un’immagine.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="sharpen.resources/sharpen-tooltip.gif" alt="descrizione comando nitidezza" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

È matematicamente molto simile alla Maschera di contrasto di Photoshop, nonostante il nome sia diverso. Funziona bene per cose come una mappa Basecolor, ma dovrebbe essere evitata su mappe come Mappe normali e mappe Metallic.

## Input

<b>Input</b> *Colore/Scala Di Grigi* (Principale)\
L&#39;immagine da rendere più nitida.

## Parametri

<b>Intensità</b> *Virgola mobile*\
Consente di impostare l’intensità dell’effetto nitidezza.

<b>Alpha Punchthrough</b> *Booleano* (disponibile quando un&#39;immagine a colori è collegata all&#39;<b>Input</b>)\
Determina se il canale alfa dell&#39;immagine deve essere reso più nitido o lasciato inalterato.

## Esempi

![Nodo Sharpen - Esempio 1](sharpen.resources/sharpen-ex.png "Nodo Sharpen - Esempio 1")
