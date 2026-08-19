---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Utilizza il nodo Toppa con più cloni per clonare e riparare più canali di texture per correggere gli artefatti del materiale scansionato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch per più cloni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Patch per più cloni

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## Toppa per più cloni (scala di grigi)

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo è la versione di input multiplo di [Patch clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Collega fino a otto input ed esegue esattamente la stessa operazione Patch clone su tutti gli input. È destinato principalmente all&#39;uso con foto con più angoli, che vengono quindi combinate con [Da multi-angolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multi-angolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consultate [Patch clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) per ulteriori informazioni, consultate [Patch clone materiale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) per la versione del materiale.

## Parametri

### Parametri

* **Numero di input**: *1 - 8* Imposta la quantità di input che riceverà la stessa operazione di patch.
* **Normale (solo per il colore)**: **False/True** Imposta se l&#39;input è una mappa normale e se la fusione deve essere trattata come tale.
* **Forma**: **Quadrato, Disco** Imposta La Forma Del Timbro. Utilizzato solo come base.
* **Edge**
  * **Soglia**: *0.0 - 1.0* Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. Si sviluppa gradualmente lungo le forme nell’area di destinazione; ha un effetto molto scarso con sfondi uniformi*.*
  * **Sfocatura**: *0.0 - 2.0* Sfoca i bordi dell&#39;area del timbro, nel caso in cui sia necessaria una transizione più morbida.
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
