---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-2.html"
breadcrumb-title: ''
description: Usa il nodo 2 di Fibre disordinate per generare pattern di fibre intermedie per creare texture tessuti e tessili.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibre disordinate 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# Fibre disordinate 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibre disordinate 2 - Icona](messy-fibers-2.resources/messy-fibers-2-01.png "Fibre disordinate 2 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei <b>rumori strutturati</b> delle fibre disordinate.

Vedere anche: [Fibre disordinate 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibre disordinate 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>anisotropia disturbo</b> <i>Mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disorder</b> quando il parametro &#39;anisotropia del disturbo&#39; è diverso da zero. |
| <b>Angolo</b> <i>Virgola mobile</i> | Angolo utilizzato per impostare la direzione dei filetti, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> <i>Mobile</i> | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Numero righe</b> <i>Mobile</i> | Quantità di Affiancamento applicata ai thread di base, in cui un valore più alto genera thread più densi e sottili. |
| <b>Scostamento porzione</b> <i>Virgola mobile 2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibre disordinate 2 - Esempio 1](messy-fibers-2.resources/messy-fibers-2-02.png "Fibre disordinate 2 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibre disordinate 2 - Esempio 2](messy-fibers-2.resources/messy-fibers-2-03.gif "Fibre disordinate 2 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibre disordinate 2 - Esempio 3](messy-fibers-2.resources/messy-fibers-2-04.gif "Fibre disordinate 2 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibre disordinate 2 - Esempio 4](messy-fibers-2.resources/messy-fibers-2-05.gif "Fibre disordinate 2 - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
