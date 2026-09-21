---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-1.html"
breadcrumb-title: ""
description: Utilizzate il nodo Gaussiana macchie 1 per generare pattern di macchie gaussiane per creare variazioni e dettagli della texture organica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Macchie gaussiane 1
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 1%
---

# Macchie gaussiane 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Macchie gaussiane 1 - Icona](gaussian-spots-1.resources/gaussian_spots_1.png "Macchie gaussiane 1 - Icona"){width="200px"}

<b>Ingresso:</b> Generatori di texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una variazione dei <b>rumori gaussiani</b> uniformi.\
In base al nodo [Gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), con sfumature più strette.

Vedere anche: [macchie gaussiane 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-2/gaussian-spots-2.md)

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
| <b>angolo di anisotropia di disturbo</b> <i>Virgola mobile</i> | Controlla la direzione dello spostamento applicato dal parametro <b>Disturbo</b> quando il parametro <b>anisotropia disturbo</b> è diverso da zero. |
| <b>Scostamento porzione</b> <i>Virgola mobile 2</i> | Controlla la posizione della porzione di piano infinito utilizzata per eseguire il rendering del disturbo. |
| <b>Espansione non quadrata</b> <i>Booleano</i> | Nelle immagini non quadrate, mantiene il riquadro quadrato generato ed espande la generazione del disturbo fino ai limiti dell&#39;immagine. |

## Esempi

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="gaussian-spots-1.resources/gaussian_spots_1_1.png" class="modal-image" alt="Macchie gaussiane 1 - Esempio 1" />
        </td>
        <td style="border: 0;">
            <img src="gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.6_aniso0.gif" class="modal-image" alt="Macchie gaussiane 1 - Esempio 2" />
        </td>
        <td style="border: 0;">
            <img src="gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.6_aniso1.gif" class="modal-image" alt="Macchie gaussiane 1 - Esempio 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="gaussian-spots-1.resources/noise_gaussian_spots_1_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Macchie gaussiane 1 - Esempio 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
