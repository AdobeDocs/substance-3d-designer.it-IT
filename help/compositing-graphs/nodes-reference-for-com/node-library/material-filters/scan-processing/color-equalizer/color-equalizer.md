---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Utilizza il nodo Color Equalizer per bilanciare le variazioni di colore nei materiali scansionati per ottenere un aspetto della texture uniforme.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo funziona come un [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) di alta qualità per le differenze di colore. Quando un passaggio normale rimuove la saturazione e può introdurre nitidezza indesiderata, Color Equalizer risolve le differenze di colore e rimuove le tinte indesiderate a una scala selezionabile dall&#39;utente.

Questa funzione è molto utile se si desidera rimuovere una foto o una scansione che presenta differenze di colore indesiderate. Se hai utilizzato [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), questo nodo dovrebbe avere familiarità.

Le opzioni di mascheratura consentono di rimuovere tinte molto specifiche o di operare solo in determinati intervalli di valori. Usateli se ritenete che l’effetto sia troppo ampio.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Input colore</i> |  |
| <b>Input maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Attivo solo quando Maschera è impostata su &quot;Input&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Affiancato input</b> <i>Falso/Vero</i> | Mantiene facoltativamente l’Affiancamento sui bordi. |
| <b>Raggio</b> <i>0.0 - 50.0</i> | Imposta il raggio di equalizzazione. Con un raggio più ampio vengono rimosse solo le differenze di colore maggiori. Questa operazione richiede l&#39;adattamento di ogni immagine. |
| <b>Bilanciamento luminoso/scuro</b> <i>0.0 - 1.0</i> | Impostate la distorsione per lasciare o rimuovere le tinte più scure. |
| <b>Variazione colore personalizzata</b> <i>Falso/Vero</i> | Consente di variare l’effetto in base a un colore specificato dall’utente. |
| <b>Variazione colore</b> | Attivo solo se è abilitata l’opzione Variazione colore personalizzata. Le impostazioni consentono di selezionare uno scostamento della tinta verso il quale eseguire l’equalizzazione. |
| <b>Tonalità</b> <i>0.0 - 360.0</i> |  |
| <b>Crominanza</b> <i>0.0 - 1.0</i> |  |
| <b>Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Origine maschera</b> <i>Nessuno, Media Immagine, Parametro Colore, Input</i> | Stabilite se deve verificarsi un qualsiasi tipo di mascheratura. Color Parameter abilita le impostazioni aggiuntive seguenti, Input passa a un input maschera definito dall&#39;utente. |
| <b>Maschera</b> | Questa opzione è attiva solo con la mascheratura dei parametri dei colori. Parametri di mascheratura aggiuntivi per determinare la maschera in base all’immagine stessa. I parametri riportati di seguito consentono di convertire con precisione una tinta in una maschera binaria su cui viene applicata l’equalizzazione. Tenete presente che gli effetti del parametro Raggio possono diventare molto meno pronunciati quando si utilizzano queste impostazioni. |
| <b>Colore</b> <i>(valore colore)</i> |  |
| <b>Intervallo tonalità</b> <i>0.0 - 360.0</i> |  |
| <b>Intervallo crominanza</b> <i>0.0 - 1.0</i> |  |
| <b>Intervallo luminanza</b> <i>0.0 - 1.0</i> |  |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
