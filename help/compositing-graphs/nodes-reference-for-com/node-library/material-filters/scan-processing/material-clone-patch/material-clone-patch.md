---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Utilizzare il nodo Patch Clona /Clone materiale per clonare e applicare patch alle aree della texture per la riparazione degli artefatti nei materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch Clona /Clone materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# Patch Clona /Clone materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione completa del materiale multicanale di [patch Clona /Clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Esegue una patch Clona /Clone su tutti i canali di un materiale. [Per ulteriori informazioni, vedere la versione originale.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Ciò è molto utile se desiderate rimuovere un dettaglio da tutti i canali di un materiale. Esegue l’output del debug delle immagini per più canali per vedere esattamente come si presenta l’area delle patch avanzate.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Forma</b> <i>Quadrato, Disco</i> | Imposta la forma del timbro. Utilizzato solo come base. |
| <b>Edge</b> |  |
| <b>Soglia (per più canali)</b> <i>0.0 - 1.0</i> | Imposta la distanza che deve essere raggiunta dall&#39;area di fusione. Cresce gradualmente lungo le forme nell&#39;area di destinazione, quindi ha un effetto molto ridotto con sfondi uniformi. Fai attenzione a cambiare troppo questa impostazione tra i canali, perché potrebbe causare discrepanze visive. |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> | Sfoca i bordi dell’area del timbro nel caso sia necessaria una transizione più morbida. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arrotonda i bordi della forma del timbro per ottenere contorni più fluidi. |
| <b>Risoluzione griglia</b> <i>1 - 11</i> | Consente di impostare la risoluzione di qualità dell&#39;analisi di fusione. Un valore più elevato indica una fusione più accurata. |
| <b>Trasformazioni</b> |  |
| <b>Matrice origine</b> <i>(Matrice di trasformazione)</i> | Trasforma la sorgente (Scala e Rotazione). Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. |
| <b>Scostamento origine</b> <i>-0.5 - 0.5</i> | Traduce la posizione di origine. Impossibile eseguire l&#39;operazione sull&#39;area di lavoro. Modificare solo questi parametri. *Questo parametro è probabilmente quello principale che si desidera modificare.* |
| <b>Matrice di destinazione</b> <i>(Matrice di trasformazione)</i> | Trasforma la posizione di destinazione (Scala e Rotazione). Può essere fatto anche tramite gizmo su tela. |
| <b>Scostamento destinazione</b> <i>-0.5 - 0.5</i> | Traduce la posizione di destinazione. Può essere fatto anche tramite gizmo su tela. |
