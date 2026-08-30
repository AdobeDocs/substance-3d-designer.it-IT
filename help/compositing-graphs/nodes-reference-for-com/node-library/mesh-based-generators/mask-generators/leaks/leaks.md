---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Utilizzate il nodo Perdite (Leaks) per generare pattern di perdita basati sulla geometria della trama per creare macchie d'acqua ed effetti fluidi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Perdite
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# Perdite

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leaks.resources/leaks.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Simile a [Maschere avanzate](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) in [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Questo nodo rappresenta le striature di dirt e sporcizia che fuoriescono dagli spigoli vivi. Quando vengono generate con Posizione eseguita i baking, le striature scorrono sempre verso il basso.

Assicuratevi di provare a modificare la maschera di variazione: poiché guida il posizionamento delle striature, può avere un&#39;influenza molto maggiore rispetto ad altri Generatori di maschere.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Posizione</b> <i>Input scala di grigi</i> | Mappa posizione eseguita i baking, utilizzata per le direzioni di striscia. Obbligatorio! |
| <b>Curvatura</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per il posizionamento della striscia. Obbligatorio! |
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. Consigliato, ma potrebbe usare bianco piatto. |
| <b>Spazio mondo normale</b> <i>Input colore</i> | World Space Normalmap eseguita i baking, usata per la direzione della striscia. Obbligatorio! |
| <b>Maschera variante</b> <i>Input scala di grigi</i> | Maschera di variazione facoltativa, attivare impostando l&#39;override su True. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Livello totale del risultato. Progressivamente rivela l&#39;effetto, influisce anche sulla lunghezza. Dovrebbe essere abbastanza alto per ottenere gocce lunghe. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Variazione</b> <i>0.0 - 1.0</i> | Imposta la quantità di variazione su larga scala utilizzata per mascherare le striature. Impostando questo valore su 0 si ottengono striature uniformi complete, quindi evitate che ciò si verifichi. |
| <b>Durata</b> <i>0.0 - 8.0</i> | La lunghezza della striscia gocciola. Se si imposta questo valore su una scala ridotta, i passaggi risulteranno visibili. Gioca anche con Level. |
| <b>Occlude</b> <i>X, Y, Z, Nessuno</i> | Consente di impostare la direzione che deve essere interessata dall’oggetto AO. |
| <b>Ignora maschera variante</b> <i>Falso/Vero</i> | Consente di sostituire la maschera di variazione con uno slot di input personalizzato. L&#39;uso di maschere più sparse o più dense può essere interessante ed è un buon modo per controllare le gocce. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leaks.resources/leaks-ex.gif" />
        </td>
    </tr>
</table>
