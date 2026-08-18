---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Utilizza il nodo Scratches direzionali per creare pattern di graffi direzionali per aggiungere effetti di usura e danneggiamento ai materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graffi direzionali
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# Graffi direzionali

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Graffi direzionali - Icona](../../../../../../assets/directional_scratches.png "Graffi direzionali - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Dispersione casuale di pattern di graffi con angolo e dimensioni regolabili.

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
| <b>Scala</b> Intero | Suddivisione della griglia utilizzata per generare le porzioni di disturbo.    Un valore più elevato determina la creazione di più riquadri e un disturbo maggiore. |
| <b>Disturbo</b> Mobile | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> Mobile | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> Mobile | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>Angolo di anisotropia disturbo</b> Mobile | Controlla la direzione dello spostamento applicato dal parametro <b>Disturbo</b> quando il parametro <b>anisotropia disturbo</b> è diverso da zero. |
| <b>Angolo</b> Mobile | Angolo utilizzato per impostare la direzione dei graffi, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> Mobile | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Quantità pattern</b> float | Un moltiplicatore per la quantità di pattern di memoria virtuale da spargere. |
| <b>Dimensione motivo</b> Float2 | La dimensione del rettangolo di selezione per il pattern di graffio.    Il valore Y controlla la lunghezza massima dei graffi. |
| <b>Dimensione del pattern casuale</b> Float2 | Un moltiplicatore per la quantità casuale di downscaling applicato ai graffi.    Il valore Y lo applica alla lunghezza dei graffi. |
| <b>Scostamento porzione</b> Float2 | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 1](../../../../../../assets/directional_scratches_1.png "Graffi direzionali - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "Graffi direzionali - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "Graffi direzionali - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 4](../../../../../../assets/noise-directional-scrat-1.gif "Graffi direzionali - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 5](../../../../../../assets/noise-directional-scrat-2.gif "Graffi direzionali - Esempio 5"){zoomable="yes"}

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
