---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: Utilizza il nodo Smart Auto Tile per creare automaticamente porzioni uniformi dai materiali scansionati utilizzando il rilevamento intelligente dei pattern.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Affianca automatica avanzata
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# Affianca automatica avanzata

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile.png){width="128px"}

<b>Tra:</b> Filtri materiali > Elaborazione scansione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo trasforma un insieme non Affiancamento di mappe di colore di base, normali e di altezza in una versione di Affiancamento in base all&#39;analisi intelligente degli input. È simile a [Crea una foto affiancata](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), ma molto più avanzato in quanto usa informazioni da tutti i canali per fondere gli elementi nel modo più intelligente (in modo simile a quello che fa [Clona /Clone patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Ha anche una funzione [Ritaglia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) interna per determinare quale area utilizzare quando si esegue l&#39;Affiancamento. Per comprendere correttamente questa funzione, [assicuratevi di leggere ulteriori informazioni sul nodo Ritaglia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md).

Per utilizzare questo nodo, iniziate definendo l&#39;area Ritagliata, quindi usate le impostazioni Bordo per determinare il modo in cui i bordi in porzioni vengono fusi al centro. I parametri di soglia sono fondamentali a tale scopo. Tieni presente che le aree grandi e uniformi non funzionano molto bene con questo effetto; più dettagli e forme ci sono, più deve lavorare con questo effetto.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivata/disattivata con il parametro &quot;Usa maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Ritaglio</b> |  |
| <b>Dimensione input</b> <i>0 - 8192</i> | Immettere la risoluzione e le proporzioni delle immagini. Molto importante per immagini non quadrate. |
| <b>Trasforma</b> <i>(Matrice di trasformazione)</i> | Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro. |
| <b>Edge</b> |  |
| <b>Rileva bordi</b> <i>Falso/Vero</i> | Attiva o disattiva la fusione rilevata dal bordo speciale. |
| <b>Usa soglia per canale</b> <i>Falso/Vero</i> | Consente di passare da un valore di soglia globale a uno per ogni canale. |
| <b>Soglia</b> <i>0.0 - 1.0</i> |  |
| <b>Colore di base di soglie</b> <i>0.0 - 1.0</i> |  |
| <b>Soglia normale</b> <i>0.0 - 1.0</i> |  |
| <b>Height di soglie</b> <i>0.0 - 1.0</i> |  |
| <b>Scostamento taglio</b> <i>0.0 - 0.5</i> | Comando principale per lo spostamento del taglio, gli assi X e Y sono separati. |
| <b>Sfocatura</b> <i>0.0 - 2.0</i> | Sfoca la transizione di fusione. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Controlla lo sfasamento dei risultati dell&#39;analisi del bordo. |
| <b>Risoluzione griglia</b> <i>1 - 11</i> | Risoluzione di qualità dell&#39;analisi dei bordi. |
| <b>Usa Colore di base</b> <i>Falso/Vero</i> | Attiva/disattiva l’elaborazione del Colore di base (entrata e uscita). |
| <b>Usa normale</b> <i>Falso/Vero</i> | Attiva/disattiva l’elaborazione normale (entrata e uscita). |
| <b>Usa Height</b> <i>Falso/Vero</i> | Attiva/disattiva l’elaborazione normale (entrata e uscita). |
| <b>Usa maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera per le forme maschera timbro personalizzate. |
