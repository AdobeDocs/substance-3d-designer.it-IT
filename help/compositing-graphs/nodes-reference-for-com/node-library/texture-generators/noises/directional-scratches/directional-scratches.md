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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Graffi direzionali

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Graffi direzionali - Icona](directional-scratches.resources/directional-scratches-01.png "Graffi direzionali - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Dispersione casuale di pattern di graffi con angolo e dimensioni regolabili.

</td>
</tr>
</table>

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Il disturbo generato come bitmap in scala di grigio. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>Numero intero</i> | Suddivisione della griglia utilizzata per generare le porzioni di disturbo.    Un valore più elevato determina la creazione di più riquadri e un disturbo maggiore. |
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> <i>Mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disturbo</b> quando il parametro <b>anisotropia disturbo</b> è diverso da zero. |
| <b>Angolo</b> <i>Mobile</i> | Angolo utilizzato per impostare la direzione dei graffi, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> <i>Mobile</i> | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Quantità motivo</b> <i>Mobile</i> | Un moltiplicatore per la quantità di pattern di memoria virtuale da spargere. |
| <b>Dimensione motivo</b> <i>Float2</i> | La dimensione del rettangolo di selezione per il pattern di graffio.    Il valore Y controlla la lunghezza massima dei graffi. |
| <b>Dimensione del pattern casuale</b> <i>Float2</i> | Un moltiplicatore per la quantità casuale di downscaling applicato ai graffi.    Il valore Y lo applica alla lunghezza dei graffi. |
| <b>Scostamento porzione</b> <i>Float2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 1](directional-scratches.resources/directional-scratches-02.png "Graffi direzionali - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 2](directional-scratches.resources/directional-scratches-03.gif "Graffi direzionali - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 3](directional-scratches.resources/directional-scratches-04.gif "Graffi direzionali - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 4](directional-scratches.resources/directional-scratches-05.gif "Graffi direzionali - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Graffi direzionali - Esempio 5](directional-scratches.resources/directional-scratches-06.gif "Graffi direzionali - Esempio 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
