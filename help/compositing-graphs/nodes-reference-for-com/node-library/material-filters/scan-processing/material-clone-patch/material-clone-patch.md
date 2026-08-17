---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Utilizzate il nodo Patch clone materiale per clonare e applicare patch alle aree della texture per correggere gli artefatti nei materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch clone materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# Patch clone materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## Patch clone materiale

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questa è la versione completa multicanale del materiale di [Patch clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Esegue una patch clone su tutti i canali di un materiale. [Per ulteriori informazioni, vedere la versione originale.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Ciò è molto utile se desiderate rimuovere un dettaglio da tutti i canali di un materiale. Esegue l’output del debug delle immagini per più canali per vedere esattamente come si presenta l’area delle patch avanzate.

## Parametri

### Input

* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;.

### Parametri

* **Canali**
  * Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Forma**: *Quadrato, Disco* Imposta La Forma Del Timbro. Utilizzato solo come base.
* **Edge**
  * **Soglia (per più canali)**: *0.0 - 1.0* Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. Si sviluppa in passaggi, lungo le forme nell&#39;area di destinazione, quindi ha pochissimo effetto con sfondi uniformi*.*Presta attenzione a cambiare troppo questa impostazione tra i canali, poiché potrebbe causare discrepanze visive!
  * **Sfocatura**: *0.0 - 2.0* Sfoca i bordi dell&#39;area del timbro nel caso in cui sia necessaria una transizione più morbida.
  * **Smoothness**: *0.0 - 2.0* Arrotonda i bordi della forma del timbro, per rendere i contorni più fluidi.
  * **Risoluzione griglia**: *1 - 11* Imposta la risoluzione di qualità dell&#39;analisi di fusione. Un valore più elevato indica una fusione più accurata.
* **Trasformazioni**
  * **Matrice origine**: *(Matrice trasformazione)*Trasforma l&#39;origine (Scala e Rotazione). Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri.
  * **Scostamento origine**: *-0,5 - 0,5* Traduce il percorso di origine. Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. *Questo parametro è probabilmente quello principale che si desidera modificare.*
  * **Matrice destinazione**: *(Matrice trasformazione)*Trasforma la posizione di destinazione (Scala e Rotazione). Può essere fatto anche tramite gizmo su tela.
  * **Offset destinazione**: *-0,5 - 0,5* Traduce il percorso di destinazione. Può essere fatto anche tramite gizmo su tela.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
