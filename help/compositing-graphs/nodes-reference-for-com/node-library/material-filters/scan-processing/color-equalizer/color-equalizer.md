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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo funziona come un [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md) di alta qualità per le differenze di colore. Quando un passaggio normale rimuove la saturazione e può introdurre nitidezza indesiderata, Color Equalizer risolve le differenze di colore e rimuove le tinte indesiderate a una scala selezionabile dall&#39;utente.

Questa funzione è molto utile se si desidera rimuovere una foto o una scansione che presenta differenze di colore indesiderate. Se hai utilizzato [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), questo nodo dovrebbe avere familiarità.

Le opzioni di mascheratura consentono di rimuovere tinte molto specifiche o di operare solo in determinati intervalli di valori. Usateli se ritenete che l’effetto sia troppo ampio.

## Parametri

### Input

* **Input**: *Input colore*
* **Input maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Attivo solo quando Maschera è impostata su &quot;Input&quot;.

### Parametri

* **Affiancato a livello di input**: *False/True* Mantiene facoltativamente la suddivisione in porzioni sui bordi.
* **Raggio**: *0.0 - 50.0* Imposta il raggio di equalizzazione. Con un raggio più ampio vengono rimosse solo le differenze di colore maggiori. Questa operazione richiede l&#39;adattamento di ogni immagine.
* **Bilanciamento luminoso/scuro**: *0,0 - 1,0* Impostazione di polarizzazione per lasciare o rimuovere tinte più scure.
* **Variazione colore personalizzata**: *False/True* Consente di variare l&#39;effetto in base a un colore specificato dall&#39;utente.
* **Variazione colore**\
  Attivo solo se è abilitata l’opzione Variazione colore personalizzata. Le impostazioni consentono di selezionare uno scostamento della tinta verso il quale eseguire l’equalizzazione.
  * **Tonalità**: *0,0 - 360,0*
  * **Crominanza**: *0.0 - 1.0*
  * **Luma**: *0.0 - 1.0*
* **Origine maschera**: *Nessuna, Media immagine, Parametro colore, Input* Imposta se deve verificarsi un qualsiasi tipo di mascheratura. Color Parameter abilita le impostazioni aggiuntive seguenti, Input passa a un input maschera definito dall&#39;utente.
* **Maschera**\
  Questa opzione è attiva solo con la mascheratura dei parametri dei colori. Parametri di mascheratura aggiuntivi per determinare la maschera in base all’immagine stessa. I parametri riportati di seguito consentono di convertire con precisione una tinta in una maschera binaria su cui viene applicata l’equalizzazione. Tenete presente che gli effetti del parametro Raggio possono diventare molto meno pronunciati quando si utilizzano queste impostazioni.
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
