---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: Utilizzate il nodo Nitidezza per migliorare i dettagli e i bordi della texture e creare dettagli di superficie nitidi e definiti.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nitidezza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Nitidezza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo contrasta](sharpen.resources/sharpen-4.png "Icona nodo contrasta")

<b>In:</b> Nodi Atomici

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo Nitidezza esegue un&#39;operazione di nitidezza su un input. È un nodo utile per applicare il tocco finale di nitidezza a un’immagine.

</td>
</tr>
</table>

È matematicamente molto simile alla Maschera di contrasto di Photoshop, nonostante il nome sia diverso. Funziona bene per cose come una mappa Basecolor, ma dovrebbe essere evitata su mappe come Normal e Metallic.

## Input

<b>Input</b> *Colore/Scala Di Grigi* (Principale)\
L&#39;immagine da rendere più nitida.

## Parametri

<b>Intensità</b> *Mobile*\
Consente di impostare l’intensità dell’effetto nitidezza.

<b>Alpha Punchthrough</b> *Booleano* (disponibile quando un&#39;immagine a colori è collegata all&#39;<b>Input</b>)\
Determina se il canale alfa dell’immagine deve essere reso più nitido o lasciato inalterato.

## Esempi

![Nodo Sharpen - Esempio 1](sharpen.resources/sharpen-ex.png "Nodo Sharpen - Esempio 1")
