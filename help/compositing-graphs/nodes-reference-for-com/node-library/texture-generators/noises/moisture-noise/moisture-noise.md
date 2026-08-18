---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo umidità per generare pattern di umidità e condensazione per creare effetti di superficie bagnata.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rumore di umidità 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# Rumore di umidità 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Disturbo umidità 1 - Icona](../../../../../../assets/moisture_noise_1.png "Disturbo umidità 1 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una variazione dei rumori <b>di umidità</b> ricchi e spugnosi.

Dischi di diversa durezza e dimensione, distribuiti e addizionati o sottratti dal colore sottostante, a partire da un grigio di base.

Vedere anche: [Rumore di umidità 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

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
| <b>Dimensione motivo</b> Float2 | Moltiplicatore per la dimensione di un motivo a dispersione., dove 1,0 è la dimensione di deformazione originale. |
| <b>Angolo motivo</b> Mobile | Angolo utilizzato per impostare la direzione della serie diffusa, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo pattern casuale</b> Mobile | Quantità massima di variazione casuale applicata al valore <b>Angolo pattern</b>, in numero di giri. |
| <b>Opacità globale</b> float | Opacità di tutti gli ingredienti del disturbo, dove 0,0 si traduce in un grigio piatto di base e 1,0 è il risultato dell’aggiunta o della sottrazione completa applicata dagli ingredienti. |
| <b>Scostamento porzione</b> Float2 | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> Booleano | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore di umidità 1 - Esempio 1](../../../../../../assets/moisture_noise_1_1.png "Rumore di umidità 1 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore di umidità 1 - Esempio 2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "Rumore di umidità 1 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore di umidità 1 - Esempio 3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "Rumore di umidità 1 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore di umidità 1 - Esempio 4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "Rumore di umidità 1 - Esempio 4"){zoomable="yes"}

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
