---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Usa il nodo di Atlas splitter per dividere gli atlanti delle texture in singole texture per l'elaborazione dei materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](atlas-splitter.resources/atlas-splitter-01.png "Icona nodo")

<b>In:</b> Filtri di materiale/Analisi elaborazione

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Accetta l&#39;input di un&#39;immagine atlas e suddivide tutti gli elementi separati come *singoli materiali*.

Può anche essere utilizzato per riorganizzare e spostare tutti gli elementi in una griglia.

Il nodo funziona come applicazione avanzata del nodo [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Visualizzazione griglia</b> <i>Booleano</i> | Visualizza tutte le forme rilevate in una griglia. |
| <b>Opacità griglia</b> <i>Virgola mobile</i> | Imposta l&#39;opacità delle linee della griglia quando Grid View è True. Opzione di debug |
| <b>Opacità selezione griglia</b> <i>Virgola mobile</i> | Imposta l&#39;opacità dell&#39;evidenziazione Selezione griglia se la proprietà Visualizzazione griglia è impostata su True. Opzione di debug |
| <b>Scala automatica</b> <i>Booleano</i> | Ridimensiona automaticamente le forme per adattarle alla cella della griglia. |
| <b>Ritaglio automatico</b> <i>Booleano</i> | Ritaglia automaticamente la dimensione di output in base alla forma più grande per ridurre al minimo lo spazio vuoto. |
| <b>Selezione forma</b> <i>Numero intero</i> | In vista Griglia consente di impostare la cella evidenziata, al di fuori di Vista Griglia consente di impostare la cella restituita. |
| <b>Ignora forma più piccola di</b> <i>Mobile</i> | Ignora le forme le cui diagonali sono inferiori al valore specificato. |
| <b>Rotazione automatica</b> <i>Booleano</i> | Ruota automaticamente la forma in base alle proporzioni del rettangolo di selezione. |
| <b>Rotazione</b> <i>Mobile</i> | Angolo di rotazione della forma globale |
| <b>Formato Normale Di Input</b> <i>Numero intero</i> | Imposta il formato della normale di input. L’impostazione del formato errato produrrà risultati errati. |
| <b>Riduci maschera di opacità</b> <i>Numero intero</i> | Riduce la maschera di opacità per rimuovere potenziali disturbi o pixel isolati. Impedisce il rilevamento di forme indesiderate e migliora le prestazioni. |
| <b>Larghezza dilatazione</b> <i>Mobile</i> | Applica un effetto di dilatazione basato sulla maschera Opacità a tutti i canali tranne Normale e Height. |
| <b>Abilita input aggiuntivi</b> <i>Booleano</i> | Rende disponibili le impostazioni e gli ingressi per USer 1 e User 2 per qualsiasi mappa aggiuntiva non coperta. |
| <b>Colore di sfondo personalizzato</b> <i>Booleano</i> | Consente di scegliere un colore di sfondo personalizzato, anziché una dilatazione del contenuto di quel livello. |
| <b>Colore base sfondo</b> <i>Float3</i> | Colore BG personalizzato per Colore base. |
| <b>Colore sfondo normale</b> <i>Float3</i> | Colore BG personalizzato per Mappa normale. |
| <b>Colore sfondo metallico</b> <i>Mobile</i> | Colore BG personalizzato per Metallico. |
| <b>Colore sfondo rugosità</b> <i>Mobile</i> | Colore BG personalizzato per rugosità |
| <b>Colore sfondo Height</b> <i>Mobile</i> | Colore BG personalizzato per il Height |
| <b>Utente 1 Colore Bg</b> <i>Mobile</i> | Colore BG personalizzato per la mappa utente 1 personalizzata |
| <b>Utente 2 Colore Bg</b> <i>Mobile</i> | Colore BG personalizzato per la mappa utente 1 personalizzata |
