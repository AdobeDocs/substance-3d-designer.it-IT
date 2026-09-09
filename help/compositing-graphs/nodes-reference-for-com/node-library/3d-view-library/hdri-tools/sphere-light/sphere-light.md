---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce sfera per aggiungere sorgenti di luce sferica agli ambienti HDRI per un migliore controllo dell’illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce sfera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# Luce sfera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sphere-light.resources/panorama-sphere-light.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una forma sferica proiettata. La trasformazione della sfera è guidata da un gizmo di trasformazione.

La Sfera Light è abbastanza versatile e ha opzioni che gli permettono non solo di generare semplici luci rotonde, ma anche pianeti o altri corpi celesti. Se non avete bisogno delle opzioni di illuminazione e rotazione più avanzate, date un&#39;occhiata a [Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md).

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
| <b>Modalità posizione</b> <i>Distanza dall&#39;origine, Posizione nel mondo</i> | Scegliete tra due modalità di posizionamento. La distanza dall&#39;origine è simile alle coordinate polari, la sfera è impostata rispetto al centro del panorama, la posizione del mondo funziona come le coordinate 3D standard. |
| <b>Coordinate posizione</b> |  |
| <b>Vettore Su</b> <i>Z Su, Y Su</i> | Solo con la modalità Posizione mondo (World Position), determinate l&#39;orientamento del sistema di coordinate. |
| <b>Posizione Sphere World</b> <i>-2.0 - 2.0</i> | Solo con la modalità Posizione mondo, imposta la posizione della sfera nello spazio mondo. |
| <b>Posizione</b> | Solo in modalità Distanza dall&#39;origine. Imposta la posizione rispetto al centro. Può essere manipolato nella vista 2D. |
| <b>Distanza dall&#39;origine</b> <i>0.0 - 20.0</i> | Solo in modalità Distanza dall&#39;origine. Imposta la distanza dall&#39;origine e influisce sulle dimensioni visibili della sfera. |
| <b>Metodo colore forma</b> <i>RGB, Temperatura (Kelvin), Input Immagine</i> | Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso. |
| <b>Colore</b> <i>(valore colore)</i> | Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma. |
| <b>Temperatura forma</b> <i>800.0 - 20000.0</i> | Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma. |
| <b>Gamma di input immagine Sphere</b> <i>sRGB, lineare</i> | Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma. |
| <b>Rotazione sfera</b> <i>0.0 - 1.0</i> | Solo con Metodo colore forma impostato su Input immagine. Ruota la sfera attorno al centro per orientare l&#39;immagine mappata. |
| <b>Esposizione (EV)</b> <i>0.0 - 10.0</i> | Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo. |
| <b>Raggio sfera</b> <i>0.0 - 1.0</i> | Imposta raggio/dimensione della sfera. |
| <b>Durezza sfera</b> <i>0.0 - 1.0</i> | Imposta la durezza/decadimento della sfera. |
| <b>Ombreggiatura</b> <i>Nessuno, Scurire Gli Arti, Ombreggiatura Luce</i> | Impostare se una qualsiasi ombreggiatura deve essere applicata alla sfera. Consente di non visualizzare la sfera come oggetto solido e non illuminato. Scurire gli arti significa scurire leggermente i bordi; Ombreggiatura Luce significa illuminare la sfera con un’Ombreggiatura opzionale Luce. |
| <b>Ombreggiatura posizione mondo chiaro</b> <i>-1.0 - 1.0</i> | Se l’Ombreggiatura è impostata su Luce Ombreggiatura, la posizione della luce sulla sfera è controllata qui. |
| <b>Trasparenza Penombra</b> <i>0.0 - 1.0</i> | Se Ombreggiatura è impostato su Luce Ombreggiatura, controlla la fine dell’ombreggiatura. |
| <b>Abilita input in background</b> <i>Falso/Vero</i> | Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita. |
| <b>Gamma sfondo</b> <i>sRGB, lineare</i> | Se viene utilizzato Background Input, impostare la modalità di interpretazione dell&#39;input Background. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/spherelight-ex1.png" />
        </td>
    </tr>
</table>
