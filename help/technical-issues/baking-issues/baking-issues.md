---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Scoprite i passaggi per la risoluzione dei problemi tecnici relativi alle texture di cottura in Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemi di cottura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# Problemi di cottura

In questa pagina sono elencati i problemi tecnici relativi a [texture di cottura](../../bakers/bakers.md) in Substance 3D Designer e sono disponibili vari passaggi per la risoluzione dei problemi.

## In questa pagina

L’opzione &quot;Corrispondenza per nome&quot; non funziona

## L’opzione &quot;Corrispondenza per nome&quot; non funziona

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![(errore)](baking-issues.resources/error.svg) Problema</b>

Quando l’opzione &quot;Corrispondenza&quot; è impostata su &quot;Per nome trama&quot;, la corrispondenza non sembra essere applicata o non è coerente in tutti gli oggetti della scena.

<b>![(tick)](baking-issues.resources/check.svg) Passaggi consigliati</b>

Nelle versioni di Designer 14.1 e precedenti, gli oggetti low poly e high poly venivano abbinati utilizzando il nome dei rispettivi oggetti *parent*, nella maggior parte dei casi la trasformazione principale.

A partire da Designer 15.0, il nome degli oggetti *geometry* viene utilizzato direttamente.

</td>
<td style="border: 0;" valign="top">

![Oggetto Geometry e relativo elemento padre nell&#39;albero della scena](baking-issues.resources/sceneTree_objectsName.png "Oggetto Geometry e relativo elemento padre nell&#39;albero della scena"){zoomable="yes"}

</td>
</tr>
</table>

Ci sono due percorsi che puoi seguire per ottenere la corrispondenza prevista:

* Regolate il nome degli oggetti geometria per applicare nomi corrispondenti.
* Ripristina il comportamento o le versioni precedenti di Designer, modificando l&#39;opzione [&#39;Modalità filtro nomi&#39;](../../interface/preferences-window/project-settings/project-settings.md) nelle impostazioni del progetto:
  1. Seleziona Modifica > Preferenze > Progetti.
  1. Seleziona l’ultimo file di progetto nell’elenco
  1. Sotto l’elenco dei file di progetto, seleziona la scheda &quot;Panettieri&quot;
  1. Imposta la modalità di filtro Nome su Nome principale (legacy)
