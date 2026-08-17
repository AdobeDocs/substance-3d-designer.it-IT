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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# Affianca automatica avanzata

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## Affianca automatica avanzata

**Ingresso:** *Filtri materiale/Elaborazione analisi*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo trasforma un set non affiancato di mappe Colore di base, Normale e Altezza in una versione affiancata in base all&#39;analisi intelligente degli input. È simile a [Crea foto affiancata](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), ma molto più avanzato in quanto usa informazioni da tutti i canali per fondere gli elementi nel modo più intelligente (in modo simile a quello che fa [Toppa clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)). Ha anche una funzione [Ritaglia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) interna per determinare quale area usare durante la suddivisione in porzioni. Assicuratevi di [leggere ulteriori informazioni sul nodo Ritaglia](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) per comprendere correttamente questa funzione.

Per utilizzare questo nodo, iniziate definendo l&#39;area Ritagliata, quindi usate le impostazioni Bordo per determinare il modo in cui i bordi in porzioni vengono fusi al centro. I parametri di soglia sono fondamentali a tale scopo. Tieni presente che le aree grandi e uniformi non funzionano molto bene con questo effetto; più dettagli e forme ci sono, più deve lavorare con questo effetto.

## Parametri

### Input

* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivata/disattivata con il parametro &quot;Usa maschera&quot;.

### Parametri

* **Ritaglio**
  * **Dimensione input**: *0 - 8192* Risoluzione e proporzioni delle immagini di input. Molto importante per immagini non quadrate.
  * **Trasformazione**: *(Matrice Di Trasformazione)*\
    Ruota e ridimensiona il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
  * **Scostamento**: *0,0 - 1,0*\
    Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l’area di lavoro.
* **Edge**
  * **Rileva bordi**: *False/True* Attiva o disattiva la fusione rilevata dal bordo speciale.
  * **Usa soglia per canale**: *False/True* Consente di passare da un valore di soglia globale a uno per ogni canale.
  * **Soglia**: *0.0 - 1.0*
  * **Colore base soglia**: *0.0 - 1.0*
  * **Soglia normale**: *0,0 - 1,0*
  * **Height di soglie**: *0.0 - 1.0*
  * **Scostamento taglio**: *0.0 - 0.5* Controllo principale per lo spostamento del taglio. Gli assi X e Y sono separati.
  * **Sfocatura**: *0.0 - 2.0* Sfoca la transizione di fusione.
  * **Smoothness**: *0.0 - 2.0* Controlla l&#39;irregolarità dei risultati dell&#39;analisi dei bordi.
  * **Risoluzione griglia**: *1 - 11* Risoluzione di qualità dell&#39;analisi dei bordi.
  * **Usa colore di base**: *False/True* Attiva/disattiva l&#39;elaborazione del colore di base (entrata e uscita).
  * **Usa normale**: *False/True* Attiva/disattiva l&#39;elaborazione normale (in e out).
  * **Usa Height**: *False/True* Attiva/disattiva l&#39;elaborazione normale (in e out).
  * **Usa maschera**: *False/True*\
    Attiva o disattiva l’uso della mappa maschera per le forme maschera timbro personalizzate.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
