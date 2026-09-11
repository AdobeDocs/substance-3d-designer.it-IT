---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: Utilizza il nodo Patch clone per clonare e applicare patch alle aree nei materiali scansionati per rimuovere artefatti e imperfezioni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch clone
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# Patch clone

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-patch.resources/clone-patch.png){width="128px"}

![](clone-patch.resources/clone-patch-grayscale.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Patch clone è un nodo procedurale e parametrico &quot;Timbro clone&quot;. Clona un&#39;area di un input a un&#39;altra, nascondendo i dettagli potenzialmente indesiderati. Anche se non è facile e veloce come l’uso di uno strumento già noto in un’applicazione basata su pennelli, offre il vantaggio principale di non essere distruttivo e di lavorare nell’ambito di un flusso di lavoro basato su nodi. Inoltre, questo nodo esegue un&#39;analisi intelligente sia dell&#39;area di destinazione che dell&#39;area di origine e tenta di fondere gli elementi nel modo più efficace possibile in base al contrasto, ai valori e alle forme.

Questo è principalmente destinato a quei rari momenti in cui si desidera eseguire una correzione manuale di un&#39;area specifica, nel caso in cui vi sia un dettaglio indesiderato da qualche parte.

Tieni presente che questo non funziona come un semplice pennello &quot;Timbro&quot; standard. La forma dell&#39;area di fusione si basa sulle forme e sui valori delle aree su cui state lavorando, il che significa che si tratta di un nodo piuttosto pesante che richiede pazienza, ma che offre risultati eccellenti.

È importante capire anche che puoi spostare l&#39;area di destinazione con un gizmo, ma l&#39;area di origine deve essere impostata modificando i parametri della &quot;matrice sorgente&quot;.

>[!NOTE]
>
> Se desideri che questo sia un materiale completo (come avviene il più delle volte), consulta [Toppa clone materiale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md).
> 
> Per i casi in cui si desidera eseguire questa operazione su più input contemporaneamente (senza che sia un materiale), vedere [Patch per più cloni](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Normale (solo per il colore)</b> <i>Falso/Vero</i> | Imposta se l&#39;input è una mappa normale e se la fusione deve essere trattata come tale. |
| <b>Forma</b> <i>Quadrato, Disco</i> | Imposta la forma del timbro. Utilizzato solo come base. |
| <b>Edge</b> |  |
| <b>Soglia</b> <i>0.0 - 1.0</i> | Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. L&#39;effetto aumenta gradualmente lungo le forme nell&#39;area di destinazione e ha un effetto molto ridotto con sfondi uniformi<i>.</i> |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> | Sfoca i bordi dell’area del timbro nel caso sia necessaria una transizione più morbida. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrotonda i bordi della forma del timbro per ottenere contorni più fluidi. |
| <b>Risoluzione griglia</b> <i>1 - 11</i> | Consente di impostare la risoluzione di qualità dell&#39;analisi di fusione. Un valore più elevato indica una fusione più accurata. |
| <b>Trasformazioni</b> |  |
| <b>Matrice origine</b> <i>(Matrice di trasformazione)</i> | Trasforma la sorgente (Scala e Rotazione). Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. |
| <b>Scostamento origine</b> <i>-0.5 - 0.5</i> | Traduce la posizione di origine. Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. <i>Questo parametro è probabilmente quello principale che si desidera modificare.</i> |
| <b>Matrice di destinazione</b> <i>(Matrice di trasformazione)</i> | Trasforma la posizione di destinazione (Scala e Rotazione). Può essere fatto anche tramite gizmo su tela. |
| <b>Scostamento destinazione</b> <i>-0.5 - 0.5</i> | Traduce la posizione di destinazione. Può essere fatto anche tramite gizmo su tela. |
