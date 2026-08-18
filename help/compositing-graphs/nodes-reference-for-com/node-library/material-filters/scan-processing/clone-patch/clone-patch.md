---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Patch clone

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## Patch clone/Patch clone in scala di grigi

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

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

## Parametri

* **Normale (solo per il colore)**: *Falso/Vero*\
  Imposta se l&#39;input è una mappa normale e se la fusione deve essere trattata come tale.
* **Forma**: *Quadrato, Disco* Imposta La Forma Del Timbro. Utilizzato solo come base.
* **Edge**
  * **Soglia**: *0.0 - 1.0* Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. Si sviluppa gradualmente lungo le forme nell&#39;area di destinazione e ha un effetto minimo con sfondi uniformi*.*
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
