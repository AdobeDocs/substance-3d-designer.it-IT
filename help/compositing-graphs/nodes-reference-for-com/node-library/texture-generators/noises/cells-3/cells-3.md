---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: Utilizza il nodo Cella 3 per generare pattern cellulari intermedi per la creazione di effetti di texture organici e biologici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CELLE 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# CELLE 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Celle 3 - Icona](cells-3.resources/cells_3.png "Celle 3 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Variazione dei <b>Celle</b> rumori muri.

L&#39;intersezione dei dischi produce celle con pareti sottili di morbidezza irregolare.

Vedere anche: [Celle 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Celle 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Celle 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Durezza</b> <i>Mobile</i> | Definizione delle pareti delle celle, in cui un valore più elevato determina pareti nitide e definite. |
| <b>Inverti</b> <i>Booleano</i> | Inverte i valori in scala di grigio dell’output dell’immagine. |
| <b>Disturbo</b> <i>Mobile</i> | Sposta gli ingredienti del disturbo.    Può essere utilizzato per animare il disturbo. |
| <b>Velocità del disturbo</b> <i>Mobile</i> | Regola la distanza di spostamento applicata dal parametro <b>Disturbo</b>.    Questa opzione consente di controllare la velocità di spostamento durante l’animazione del disturbo. |
| <b>anisotropia disturbo</b> <i>Mobile</i> | Controlla l&#39;estensione delle direzioni dello spostamento applicato dal parametro <b>Disturbo</b>, in cui un valore più alto determina una direzione più stretta e definita.    La direzione è controllata dal parametro <b>Angolo di anisotropia disturbo</b>. |
| <b>angolo di anisotropia di disturbo</b> <i>Mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disorder</b> quando il parametro &#39;anisotropia del disturbo&#39; è diverso da zero. |
| <b>Dimensione motivo</b> <i>Float2</i> | Moltiplicatore per la dimensione di un disco sparso nella relativa cella, dove 1,0 rappresenta l&#39;intera estensione della cella. |
| <b>Scala pattern</b> <i>Mobile</i> | Un moltiplicatore per la <b>dimensione del pattern</b>, dove 1,0 corrisponde alla dimensione reale. |
| <b>Angolo</b> <i>Mobile</i> | Angolo utilizzato per impostare la direzione dei dischi, in numero di giri e a partire da destra orizzontale. |
| <b>Angolo casuale</b> <i>Mobile</i> | L&#39;importo massimo della variazione casuale applicata al valore <b>Angolo</b>, in numero di giri. |
| <b>Scostamento porzione</b> <i>Float2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celle 3 - Esempio 1](cells-3.resources/cells_3_1.png "Celle 3 - Esempio 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celle 3 - Esempio 2](cells-3.resources/noise_cells_3_v2_speed0.6_aniso0.gif "Celle 3 - Esempio 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Celle 3 - Esempio 3](cells-3.resources/noise_cells_3_v2_speed0.6_aniso1.gif "Celle 3 - Esempio 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Celle 3 - Esempio 4](cells-3.resources/noise_cells_3_v2_speed0.3_aniso0.6.gif "Celle 3 - Esempio 4"){zoomable="yes"}

</td>
</tr>
</table>
