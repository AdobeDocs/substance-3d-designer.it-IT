---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: Utilizza il nodo Celle 4 per generare pattern cellulari avanzati per la creazione di effetti di texture organici e biologici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLE 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---


# CELLE 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celle 4 - Icona](../../../../../../assets/cells_4.png "Celle 4 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei <b>Celle</b> rumori muri.

A ogni cella viene assegnato un colore piatto, che può essere casuale o campionato da un&#39;immagine di input.

Vedere anche: [Celle 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Celle 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Celle 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Input

</td>
<td style="border: 0;" valign="top">

### Output

</td>
<td style="border: 0;" valign="top">

### Parametri

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Input

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi* |  |

## Output

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | Il disturbo generato come bitmap in scala di grigio. |

## Parametri

|  |  |
| --- | --- |
| <b>Scala</b> Intero | Suddivisione della griglia utilizzata per generare le porzioni di disturbo.    Un valore più elevato determina la creazione di più riquadri e un disturbo maggiore. |
| <b>Disturbo</b> Mobile | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> Mobile | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Origine colore</b> Numero intero | Origine del colore piatto applicato alle celle:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>Casuale:</i></b> utilizzare un colore casuale controllato dal valore di inizializzazione casuale del nodo</li> <li data-preserve-html="true"><b><i>Pseudorandom:</i></b> Utilizzare un colore casuale preimpostato da un valore diverso impostato dall&#39;utente</li> <li data-preserve-html="true"><b><i>Input immagine:</i></b> utilizzare il colore campionato nella posizione della cella nell&#39;immagine di input</li> </ul> |
| <b>Valore di inizializzazione pseudorandom</b> Valore intero *Disponibile quando &#39;Origine colore&#39; è impostato su &#39;Pseudorandom&#39;* | Consente di modificare il valore di inizializzazione del colore separatamente dal valore di inizializzazione del nodo. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celle 4 - Esempio 1](../../../../../../assets/cells_4_1.png "Celle 4 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celle 4 - Esempio 2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "Celle 4 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
