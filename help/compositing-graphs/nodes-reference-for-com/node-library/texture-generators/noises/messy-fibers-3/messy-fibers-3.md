---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ''
description: Usa il nodo 3 di Fibre disordinate per generare modelli di fibre complessi per creare effetti di tessuto e texture tessile.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibre disordinate 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# Fibre disordinate 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibre disordinate 3 - Icona](../../../../../../assets/messy_fibers_3.png "Fibre disordinate 3 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei <b>rumori strutturati</b> delle fibre disordinate.

Vedere anche: [Fibre disordinate 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibre disordinate 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>Angolo di anisotropia disturbo</b> Mobile | Controlla la direzione dello spostamento applicato dal parametro <b>Disorder</b> quando il parametro &#39;anisotropia del disturbo&#39; è diverso da zero. |
| <b>Angolo</b> Mobile | Angolo utilizzato per impostare la direzione dei filetti, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> Mobile | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Luminanza casuale</b> Mobile | Intervallo di luminanza sottratto casualmente dai concatenamenti, dove 1 rappresenta l’intervallo completo. |
| <b>Scostamento porzione</b> Float2 | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibre disordinate 3 - Esempio 1](../../../../../../assets/messy_fibers_3_1.png "Fibre disordinate 3 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibre disordinate 3 - Esempio 2](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.gif "Fibre disordinate 3 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibre disordinate 3 - Esempio 3](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso1.gif "Fibre disordinate 3 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibre disordinate 3 - Esempio 4](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif "Fibre disordinate 3 - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
