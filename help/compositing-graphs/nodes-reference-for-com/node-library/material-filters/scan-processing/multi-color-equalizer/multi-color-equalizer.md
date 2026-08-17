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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# Color Equalizer multiplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## Color Equalizer multiplo

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questa è la versione con più input di [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md). Uniforma le differenze di colore e rimuove le tinte indesiderate in una scala selezionabile dall’utente. È destinato principalmente all&#39;uso con foto con più angoli, che vengono quindi combinate con [Da multi-angolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multi-angolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Per ulteriori informazioni, vedere il [Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md) originale.

## Parametri

### Input

* **Input 1-8**: *Input colore* Input multipli da elaborare.
* **Input maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Numero di input**: *1 - 8* Imposta il numero di input da elaborare in parallelo.
* **Affiancato a livello di input**: *False/True* Mantiene facoltativamente la suddivisione in porzioni sui bordi.
* **Raggio**: *0.0 - 50.0* Imposta il raggio di equalizzazione. Con un raggio più ampio vengono rimosse solo le differenze di colore maggiori. Questa operazione richiede l&#39;adattamento di ogni immagine.
* **Bilanciamento luminoso/scuro**: *0,0 - 1,0* Impostazione di polarizzazione per lasciare o rimuovere tinte più scure.
* **Variazione colore personalizzata**: *False/True* Consente di variare l&#39;effetto in base a un colore specificato dall&#39;utente.
* **Variazione colore**\
  Attivo solo se è abilitata l’opzione Variazione colore personalizzata. Le impostazioni consentono di selezionare uno scostamento della tinta verso il quale eseguire l’equalizzazione.
  * **Tonalità**: *0,0 - 360,0*
  * **Crominanza**: *0.0 - 1.0*
  * **Luma**: *0.0 - 1.0*
* **Origine maschera**: *Nessuna, Media immagine, Parametro colore, Input* Imposta se deve essere applicata una maschera. Color Parameter abilita le impostazioni aggiuntive di seguito. Input passa a un input maschera definito dall&#39;utente.
* **Maschera**\
  Attivo solo con la mascheratura dei parametri dei colori. Contiene parametri di mascheratura aggiuntivi per determinare la maschera in base all’immagine stessa. I parametri seguenti consentono di convertire con precisione una tinta in una maschera binaria su cui viene applicata l’equalizzazione. Tenete presente che gli effetti del parametro Raggio possono diventare molto meno pronunciati quando si utilizzano queste impostazioni.
  * **Colore**: *(valore colore)*
  * **Intervallo tonalità**: *0,0 - 360,0*
  * **Intervallo crominanza**: *0.0 - 1.0*
  * **Intervallo Luma**: *0,0 - 1,0*
  * **Sfocatura**: *0.0 - 2.0*
  * **Smoothness**: *0.0 - 2.0*

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
