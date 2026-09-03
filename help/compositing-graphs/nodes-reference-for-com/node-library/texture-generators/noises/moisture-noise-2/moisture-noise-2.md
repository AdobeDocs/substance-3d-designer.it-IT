---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise-2.html"
breadcrumb-title: ''
description: Utilizzate il nodo Disturbo umidità 2 per generare pattern di umidità organica per texture di superficie realistiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rumore umidità 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---


# Rumore umidità 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Disturbo umidità 2 - Icona](moisture-noise-2.resources/moisture-noise-2-01.png "Disturbo umidità 2 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una variazione dei rumori <b>di umidità</b> ricchi e spugnosi.

Dischi di diversa durezza e dimensione, distribuiti e addizionati o sottratti dal colore sottostante, a partire da un grigio di base.

Vedere anche: [Rumore di umidità 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise/moisture-noise.md)

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
| <b>anisotropia disturbo</b> <i>Virgola mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disturbo</b> quando il parametro <b>anisotropia disturbo</b> è diverso da zero. |
| <b>Dimensione motivo</b> <i>Float2</i> | Moltiplicatore per la dimensione di un motivo a dispersione., dove 1,0 è la dimensione di deformazione originale. |
| <b>Angolo motivo</b> <i>Virgola mobile</i> | Angolo utilizzato per impostare la direzione della serie diffusa, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo pattern casuale</b> <i>Virgola mobile</i> | Quantità massima di variazione casuale applicata al valore <b>Angolo pattern</b>, in numero di giri. |
| <b>Opacità globale</b> <i>Virgola mobile</i> | Opacità di tutti gli ingredienti del disturbo, dove 0,0 si traduce in un grigio piatto di base e 1,0 è il risultato dell’aggiunta o della sottrazione completa applicata dagli ingredienti. |
| <b>Scostamento porzione</b> <i>Virgola mobile 2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore di umidità 2 - Esempio 1](moisture-noise-2.resources/moisture-noise-2-02.png "Rumore di umidità 2 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore di umidità 2 - Esempio 2](moisture-noise-2.resources/moisture-noise-2-03.gif "Rumore di umidità 2 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Rumore di umidità 2 - Esempio 3](moisture-noise-2.resources/moisture-noise-2-04.gif "Rumore di umidità 2 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Rumore di umidità 2 - Esempio 4](moisture-noise-2.resources/moisture-noise-2-05.gif "Rumore di umidità 2 - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
