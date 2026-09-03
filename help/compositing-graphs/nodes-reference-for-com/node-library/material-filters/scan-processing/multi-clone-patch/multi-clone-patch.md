---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Utilizza il nodo Toppa per più Clona /Clone per clonare e applicare patch a più canali texture per correggere gli artefatti del materiale scansionato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Toppa per più Clona /Clone
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# Toppa per più Clona /Clone

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/multi-clone-patch-01.png){width="128px"}

![](multi-clone-patch.resources/multi-clone-patch-02.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo è la versione di input multiplo di [Clona /Clone patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Collega fino a otto ingressi ed esegue esattamente su tutti gli ingressi la stessa operazione Clona /Clone Patch. È destinato principalmente all&#39;uso con foto con più angoli, che vengono quindi combinate con [Da multi-angolo a Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) o [Da multi-angolo a normale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Per ulteriori informazioni, vedere [Clona /Clone patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Per la versione del materiale, vedere [Materiale Clona /Clone patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Conteggio input</b> <i>1 - 8</i> | Imposta la quantità di input che riceverà la stessa operazione Patch. |
| <b>Normale (solo per il colore)</b> <i>Falso/Vero</i> | Imposta se l&#39;input è una mappa normale e se la fusione deve essere trattata come tale. |
| <b>Forma</b> <i>Quadrato, Disco</i> | Imposta la forma del timbro. Utilizzato solo come base. |
| <b>Edge</b> |  |
| <b>Soglia</b> <i>0.0 - 1.0</i> | Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. Si sviluppa gradualmente lungo le forme nell’area di destinazione; ha un effetto molto scarso con sfondi uniformi. |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> | Sfoca i bordi dell’area del timbro, nel caso sia necessaria una transizione più morbida. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrotonda i bordi della forma del timbro per ottenere contorni più fluidi. |
| <b>Risoluzione griglia</b> <i>1 - 11</i> | Imposta la risoluzione di qualità dell&#39;analisi di fusione. Un valore più elevato indica una fusione più accurata. |
| <b>Trasformazioni</b> |  |
| <b>Matrice origine</b> <i>(Matrice di trasformazione)</i> | Trasforma la sorgente (Scala e Rotazione). Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. |
| <b>Scostamento origine</b> <i>-0.5 - 0.5</i> | Traduce la posizione di origine. Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. *Questo parametro è probabilmente quello principale che si desidera modificare.* |
| <b>Matrice di destinazione</b> <i>(Matrice di trasformazione)</i> | Trasforma la posizione di destinazione (Scala e Rotazione). Può essere fatto anche tramite gizmo su tela. |
| <b>Scostamento destinazione</b> <i>-0.5 - 0.5</i> | Traduce la posizione di destinazione. Può essere fatto anche tramite gizmo su tela. |
