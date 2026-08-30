---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce forma per aggiungere sorgenti luminose a forma personalizzata agli ambienti HDRI per creare effetti di luce creativi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma luce
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# Forma luce

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/panorama-shape.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una forma rettangolare proiettata sfericamente. La trasformazione della forma è guidata da un gizmo di trasformazione.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input immagine di sfondo</b> <i>Input colore</i> | Sfondo opzionale su cui comporre la luce generata. |
| <b>Input immagine forma</b> <i>Input colore</i> | Immagine opzionale da mappare sulla luce sfera. Utilizzato solo quando Metodo colore forma è impostato su Input immagine. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Matrice forme</b> |  |
| <b>Matrice</b> <i>(Matrice di trasformazione)</i> | Controllo di trasformazione per il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro. |
| <b>Scostamento</b> <i>-2.0 - 2.0</i> | Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro. |
| <b>Forma</b> <i>Rettangolo, Disco</i> | Scegliete la forma da posizionare. |
| <b>Metodo colore forma</b> <i>RGB, Temperatura (Kelvin), Input Immagine</i> | Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso. |
| <b>Colore</b> <i>(valore colore)</i> | Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma. |
| <b>Temperatura forma</b> <i>800.0 - 20000.0</i> | Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma. |
| <b>Gamma input immagine forma</b> <i>sRGB, lineare</i> | Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma. |
| <b>Esposizione forma (EV)</b> <i>0.0 - 10.0</i> | Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo. |
| <b>Durezza forma</b> <i>0.0 - 1.0</i> | Impostate la durezza dei bordi della forma. |
| <b>Esposizione hotspot (EV)</b> <i>0.0 - 10.0</i> | Imposta Esposizione del punto attivo centrale. Si noti che questo non è molto visibile in modalità RGB. |
| <b>Dimensione hotspot</b> <i>0.0 - 1.0</i> | Dimensioni del punto attivo centrale. |
| <b>Falloff hotspot</b> <i>0.0 - 1.0</i> | Decadimento del punto caldo centrale. |
| <b>Posizione punto attivo</b> <i>0.0 - 1.0</i> | Posizione X e Y del punto attivo centrale. |
| <b>Abilita input in background</b> <i>Falso/Vero</i> | Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita. |
| <b>Gamma sfondo</b> <i>sRGB, lineare</i> | Se viene utilizzato Background Input, impostare la modalità di interpretazione dell&#39;input Background. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-ex.gif" />
        </td>
    </tr>
</table>
