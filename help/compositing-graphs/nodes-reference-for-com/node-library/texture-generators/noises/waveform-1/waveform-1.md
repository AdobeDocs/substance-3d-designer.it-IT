---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: Utilizza il nodo Forma d’onda 1 per generare pattern di forma d’onda per creare texture organiche e variazioni procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma d’onda 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---


# Forma d’onda 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Forma d&#39;onda 1 - Icona](../../../../../../assets/waveform_01_v2.png "Forma d&#39;onda 1 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Disposizione orizzontale di motivi selezionati dall&#39;utente impilati in una forma simile a una forma d&#39;onda.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
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

## Output

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi* | Il disturbo generato come bitmap in scala di grigio. |

## Parametri

|  |  |
| --- | --- |
| <b>Esempi</b> Interi | Quantità di pattern posizionati lungo l’asse X per disegnare la forma d’onda, dove un valore inferiore determina un aspetto più graduale. |
| <b>Funzione</b> Intero | Funzione utilizzata per disegnare la forma d’onda.   Questa opzione controlla la dimensione verticale del pattern posizionato su ciascun campione:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Disturbo valore:</i> Distribuzione casuale dei valori</li> <li data-preserve-html="true"><i>Coseno:</i> I valori seguono la progressione di una funzione coseno</li> <li data-preserve-html="true"><i>Funzione personalizzata:</i> Utilizzare una funzione creata dall&#39;utente per guidare i valori</li> </ul> |
| <b>Funzione personalizzata</b> Mobile *Disponibile quando &#39;Funzione&#39; è impostato su &#39;Funzione personalizzata&#39;* | Calcola la dimensione verticale del pattern posizionato su ciascun campione.   Variabili disponibili:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) Posizione del pattern sull&#39;asse X. Questa opzione può essere utilizzata per selezionare i pattern.</li> </ul> |
| <b>Rugosità</b> Mobile | Interpola una forma d’onda pulita e liscia con una più ruvida e uniformemente distribuita.    Può essere considerato come un segnale pulito rispetto a un disturbo bianco. |
| <b>Scala</b> Intero | L’estensione orizzontale della forma d’onda visibile nell’immagine. |
| <b>Ampiezza min.</b>  A virgola mobile | Il valore minimo (o thickness) della forma d’onda. |
| <b>Ampiezza max.</b>  A virgola mobile | Il valore massimo (o thickness) della forma d’onda. |
| <b>Disturbo</b> Mobile | Applica disturbo alla forma d’onda che si sottrae casualmente dalla sua estensione verticale. |
| <b>Posizione</b> Intero | Posizione della forma d’onda nell’immagine:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Centrato:</i> L&#39;origine si trova al centro verticale dell&#39;immagine</li> <li data-preserve-html="true"><i>In basso:</i> l&#39;origine si trova nella parte inferiore dell&#39;immagine</li> </ul> |
| <b>Pattern</b> Integer | Pattern posizionato su ogni campione della forma d’onda. |
| <b>Variazione motivo</b> Float | È disponibile un&#39;ulteriore regolazione per alcuni pattern. |
| <b>Disturbo</b> Mobile | Sposta i valori della forma d’onda.    Questa opzione può essere utilizzata per animarlo. |
| <b>Velocità del disturbo</b> Mobile | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione può essere utilizzata per controllare la velocità di spostamento durante l’animazione della forma d’onda. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Forma d&#39;onda 1 - Esempio 1](../../../../../../assets/waveform_01_v2_speed0.1_aniso0.gif "Forma d&#39;onda 1 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



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
