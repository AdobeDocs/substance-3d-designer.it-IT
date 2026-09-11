---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: Utilizza il nodo Celle 2 per generare modelli cellulari intermedi per la creazione di effetti di texture organici e biologici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLE 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# CELLE 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celle 2 - Icona](cells-2.resources/cells_2.png "Celle 2 - Icona"){width="200px"}

<b>Ingresso:</b> generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei <b>Celle</b> rumori muri.

Maschera binaria delle celle con un thickness di parete regolabile.

Vedere anche: [Celle 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Celle 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Celle 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Larghezza bordo</b> <i>Virgola mobile</i> | Regola il thickness delle pareti tra le celle, come rapporto della griglia. (ovvero non dipendente dalla risoluzione) |
| <b>Inverti</b> <i>Booleano</i> | Scambia i neri e i bianchi nell&#39;immagine di output. |
| <b>Disturbo</b> <i>Virgola mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celle 2 - Esempio 1](cells-2.resources/cells_2_1.png "Celle 2 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celle 2 - Esempio 2](cells-2.resources/noise_cells_2_v2_speed0.3_aniso0.6.gif "Celle 2 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>
