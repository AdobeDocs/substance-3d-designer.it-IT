---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-ridged-noise-fractal.html"
breadcrumb-title: ''
description: Utilizza il nodo Frattale disturbo con scanalature 3D per generare pattern di disturbo frattale con scanalature in uno spazio 3D per creare texture simili a quelle delle montagne.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Ridged Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Frattale disturbo con dorso 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---


# Frattale disturbo con dorso 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-ridged-noise-fractal.resources/3dridgednoisefractal.png){width="200px"}

<b>Ingresso:</b> Generatori di Texture > Rumori

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Il nodo <b>Frattale disturbo con dorso 3D</b> genera un disturbo con dorso <i>frattale</i> in uno spazio 3D in base all&#39;input <b>Mappa posizione</b>.

Questo nodo può essere testato con [Cubo 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) come input anziché come mappa con baking effettiva (come illustrato nell&#39;immagine di esempio seguente).

</td>
</tr>
</table>

>[!WARNING]
>
> Questo rumore deve essere utilizzato solo con <i>motore GPU</i> (ad esempio <b>Direct3D</b> o <b>OpenGL</b>). Vai a <b>Strumenti > Cambia motore...</b> oppure premi il tasto <b>F9</b> per selezionare il motore desiderato.

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti</b> <i>Booleano</i> | Inverte l’immagine di output. |
| <b>Scala</b> <i>Mobile</i> | Controlla la scala del disturbo frattale con dorso 3D. |
| <b>Dimensioni</b> <i>Float3</i> | Controlla la dimensione del disturbo frattale con dorso 3D negli assi <b>X</b>, <b>Y</b> e <b>Z</b>. I valori non uniformi producono un effetto <i>allungamento o schiacciamento</i>. |
| <b>Scostamento</b> <i>Float3</i> | Applica uno scostamento alla <i>posizione</i> del disturbo frattale con dorso 3D negli assi <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensità Distorsione</b> <i>Mobile</i> | Controlla l&#39;intensità di un <i>effetto di alterazione</i> applicato al disturbo frattale con dorso 3D. |
| <b>Moltiplicatore scala Distorsione</b> <i>Mobile</i> | Controlla la scala del <i>pattern di deformazione</i> utilizzato nell&#39;effetto di alterazione controllato dall&#39;<b>intensità della Distorsione</b>. |
| <b>Livello Min</b> <i>Numero intero</i> | Il <i>livello minimo di ripetizione</i> utilizzato nel pattern frattale. Un intervallo minimo/massimo più ampio genera un <i>modello più ricco</i> con variazione su più intervalli di frequenza. |
| <b>Livello massimo</b> <i>Numero intero</i> | Il <i>livello massimo di ripetizione</i> utilizzato nel pattern frattale. Un intervallo minimo/massimo più ampio genera un <i>modello più ricco</i> con variazione su più intervalli di frequenza. |
| <b>Rugosità</b> <i>Mobile</i> | Controlla l&#39;<i>equilibrio</i> tra <i>livelli di ripetizione</i> bassi e alti nel pattern frattale.<br><br><i>Nota</i>: un valore di <b>0</b> genera un output <i>non in linea</i> seguito da altri valori bassi. Questo è previsto. |
| <b>Lacunarità</b> <i>Mobile</i> | Controlla la modalità di riempimento dello spazio del pattern frattale applicato <i></i>. Un valore <i>maggiore</i> genera <i>meno spazi vuoti</i> nel pattern e un disturbo <i>più denso</i>. |
| <b>Opacità globale</b> <i>Mobile</i> | Controlla l&#39;<i>intervallo</i> dei valori di disturbo frattale con dorso 3D <i>attorno</i> al valore <b>Baseline</b>. |
| <b>Previsione</b> <i>Mobile</i> | Applica un <i>offset</i> al valore di <i>luminanza</i> della linea di base per la distribuzione del valore del disturbo con dorso 3D. |
| <b>Contrasto</b> <i>Mobile</i> | Regola il contrasto del disturbo con dorso 3D. |
| <b>Abilita Affiancamento</b> <i>Booleano</i> | Regola il disturbo con dorso 3D in modo che il relativo pattern <i>si ripeta</i> sugli assi X, Y e Z. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-ridged-noise-fractal.resources/3dridgednoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>
