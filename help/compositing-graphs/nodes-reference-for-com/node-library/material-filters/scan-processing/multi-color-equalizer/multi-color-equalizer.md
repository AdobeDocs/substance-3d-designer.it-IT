---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: Utilizza il nodo Multi Color Equalizer per equalizzare i colori su più canali di texture per un’elaborazione coerente del materiale scansionato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer multiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# Color Equalizer multiplo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questa è la versione con più input di [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Uniforma le differenze di colore e rimuove le tinte indesiderate in una scala selezionabile dall’utente. È destinato principalmente all&#39;uso con foto con più angoli, che vengono quindi combinate con [Da multi-angolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multi-angolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Per ulteriori informazioni, vedere il [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) originale.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input 1-8</b> <i>Input colore</i> | Più input da elaborare. |
| <b>Input maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Conteggio input</b> <i>1 - 8</i> | Imposta il numero di input da elaborare in parallelo. |
| <b>Affiancato input</b> <i>Falso/Vero</i> | Mantiene facoltativamente l’Affiancamento sui bordi. |
| <b>Raggio</b> <i>0.0 - 50.0</i> | Imposta il raggio di equalizzazione. Con un raggio più ampio vengono rimosse solo le differenze di colore maggiori. Questa operazione richiede l&#39;adattamento di ogni immagine. |
| <b>Bilanciamento luminoso/scuro</b> <i>0.0 - 1.0</i> | Impostate la distorsione per lasciare o rimuovere le tinte più scure. |
| <b>Variazione colore personalizzata</b> <i>Falso/Vero</i> | Consente di variare l’effetto in base a un colore specificato dall’utente. |
| <b>Variazione colore</b> | Attivo solo se è abilitata l’opzione Variazione colore personalizzata. Le impostazioni consentono di selezionare uno scostamento della tinta verso il quale eseguire l’equalizzazione. |
| <b>Tonalità</b> <i>0.0 - 360.0</i> |  |
| <b>Crominanza</b> <i>0.0 - 1.0</i> |  |
| <b>Luma</b> <i>0.0 - 1.0</i> |  |
| <b>Origine maschera</b> <i>Nessuno, Media Immagine, Parametro Colore, Input</i> | Consente di impostare l’eventuale applicazione di una maschera. Color Parameter abilita le impostazioni aggiuntive di seguito. Input passa a un input maschera definito dall&#39;utente. |
| <b>Maschera</b> | Attivo solo con la mascheratura dei parametri dei colori. Contiene parametri di mascheratura aggiuntivi per determinare la maschera in base all’immagine stessa. I parametri seguenti consentono di convertire con precisione una tinta in una maschera binaria su cui viene applicata l’equalizzazione. Tenete presente che gli effetti del parametro Raggio possono diventare molto meno pronunciati quando si utilizzano queste impostazioni. |
| <b>Colore</b> <i>(valore colore)</i> |  |
| <b>Intervallo tonalità</b> <i>0.0 - 360.0</i> |  |
| <b>Intervallo crominanza</b> <i>0.0 - 1.0</i> |  |
| <b>Intervallo luminanza</b> <i>0.0 - 1.0</i> |  |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
