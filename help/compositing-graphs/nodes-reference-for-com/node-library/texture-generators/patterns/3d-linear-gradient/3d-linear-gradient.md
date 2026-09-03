---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Usa il nodo del 3D linear gradient per creare sfumature lineari basate sulla posizione del mondo 3D per effetti spaziali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-linear-gradient.resources/3d-linear-gradient-01.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Crea una sfumatura volumetrica in base alla mappa Posizione di input. Genera efficacemente una transizione dal nero al bianco tra 2 punti nello spazio 3D. Destinato all’uso esclusivo con il motore GPU.

Consultate anche [Maschera volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) per un effetto simile.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità posizione punti</b> <i>Posizioni UV, Posizioni Spazio Mondiale</i> | Scegli se i punti sfumatura funzionano nello spazio UV (funziona meglio quando li imposti in Vista 2D) o nelle coordinate 3D, se desideri inserire manualmente una posizione esatta. |
| <b>Punto 1</b> | Punto iniziale della sfumatura. Può essere 2D o 3D Coordinate in base alla Modalità posizione. |
| <b>Punto 2</b> | Punto finale della sfumatura. Può essere 2D o 3D Coordinate in base alla Modalità posizione. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-linear-gradient.resources/3d-linear-gradient-02.gif" />
        </td>
    </tr>
</table>
