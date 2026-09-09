---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce piano per aggiungere sorgenti planari di luce agli ambienti HDRI per il controllo direzionale dell’illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce piano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Luce piano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plane-light.resources/panorama-plane-light.png){width="200px"}

<b>Ingresso:</b> vista 3D > Strumenti HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una forma piano proiettata sfericamente. Il piano può essere posizionato e orientato in 3D utilizzando i parametri di input.

Si distingue dalla [Luce forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) più semplice in quanto ha più opzioni di posizionamento avanzate al di fuori di una proiezione Distanza dall&#39;origine più semplice e consente di applicare più pattern e maschere, simili a [Luce linea](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input immagine di sfondo</b> <i>Input colore</i> | Sfondo opzionale su cui comporre la luce generata. |
| <b>Input immagine forma</b> <i>Input colore</i> | Immagine opzionale da mappare su luce di linea. Utilizzato solo quando Metodo colore forma è impostato su Input immagine. |
| <b>Input immagine modello</b> <i>Input scala di grigi</i> | Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità posizione</b> <i>Terra/Soffitto, Distanza dall&#39;origine, Posizioni nel mondo</i> | Selezionate tre diverse modalità di posizionamento. Le opzioni di manipolazione per il supporto di Distanza dall&#39;origine/Soffitto e Terra nella vista 2D consentono di modificare le posizioni di World solo mediante le proprietà, ma supportano anche un posizionamento più preciso. |
| <b>Mostra griglia terreno</b> <i>Falso/Vero</i> | Funzione di supporto per consentire la creazione di una griglia di terra di debug. Consente di stimare la posizione delle linee nello spazio. |
| <b>Coordinate posizione</b> |  |
| <b>Vettore Su</b> <i>Z Su, Y Su</i> | Solo con la modalità Posizione mondo (World Position), determinate l&#39;orientamento del sistema di coordinate. |
| <b>Posizione UV piano</b> | Solo con messa a terra/a soffitto e Distanza dall&#39;origine. Imposta la posizione del piano nello spazio UV. |
| <b>Posizione Plane World</b> <i>-2.0 - 2.0</i> | Solo con la modalità Posizioni mondiali. Imposta lo spazio del mondo della posizione piana. Nessuna interazione di visualizzazione 2D supportata. |
| <b>Height assoluto piano</b> <i>0.0 - 1.0</i> | Solo con la modalità di posizione Terra/Soffitto, imposta il height assoluto dal soffitto. Utilizzate Mostra griglia terreno per stimare meglio la posizione. |
| <b>Distanza dall&#39;origine</b> <i>0.0 - 1.0</i> | Solo con la modalità Posizione Distanza dall&#39;origine. Imposta la distanza dal centro del panorama per entrambi i punti. |
| <b>Metodo colore forma</b> <i>RGB, Temperatura (Kelvin), Input Immagine</i> | Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso. |
| <b>Colore</b> <i>(valore colore)</i> | Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma. |
| <b>Temperatura</b> <i>800.0 - 20000.0</i> | Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma. |
| <b>Modalità UV immagine forma</b> <i>Allungamento, Allungamento solo al centro, Ripeti + Spaziatura</i> | Solo con Metodo colore forma impostato su Input immagine. Consente di impostare il modo in cui l&#39;immagine viene applicata alla forma della linea e determina il comportamento di ripetizione UV. |
| <b>Spaziatura ripetuta immagine forma</b> <i>0.0 - 1.0</i> | Solo con Metodo colore forma impostato su Input immagine e con Metodo UV impostato su Ripeti + Spaziatura. Imposta la spaziatura quando l’immagine si ripete lungo la linea. |
| <b>Gamma immagine forma</b> <i>sRGB, lineare</i> | Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma. |
| <b>Esposizione (EV)</b> <i>0.0 - 10.0</i> | Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo. |
| <b>Scala piano</b> <i>0.0 - 1.0</i> | Impostate la scala uniforme della forma Piano. |
| <b>Dimensione piano</b> <i>0.0 - 1.0</i> | Impostate le dimensioni non uniformi della forma Piano. |
| <b>Rotazione piano</b> <i>0.0 - 1.0</i> | Ruota piano lungo l&#39;asse centrale. |
| <b>Pattern</b> <i>Quadrato uniforme, Quadrato nitido, Cono, Emisfero, Input immagine</i> | Selezionare la forma del motivo da utilizzare. |
| <b>Durezza pattern</b> <i>0.0 - 1.0</i> | Impostate la durezza/il contrasto per il pattern. |
| <b>Modalità UV pattern</b> <i>Allungamento, Allungamento solo al centro</i> | Imposta come utilizzare la maschera di pattern secondaria, applicata sopra l’immagine della forma. |
| <b>Abilita ritaglio terreno</b> <i>Falso/Vero</i> | Attiva questa opzione se il piano può essere ritagliato da un piano terreno o se viene ancora visualizzato quando si va al di sotto di esso. Usate Mostra griglia terreno per una migliore stima. |
| <b>Height terreno</b> <i>-2.0 - 0.0</i> | Regolate il height terra per il ritaglio. |
| <b>Abilita input in background</b> <i>Falso/Vero</i> | Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita. |
| <b>Gamma sfondo</b> <i>sRGB, lineare</i> | Se viene utilizzato Background Input, impostare la modalità di interpretazione dell&#39;input Background. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plane-light.resources/plane-light-ex.gif" />
        </td>
    </tr>
</table>
