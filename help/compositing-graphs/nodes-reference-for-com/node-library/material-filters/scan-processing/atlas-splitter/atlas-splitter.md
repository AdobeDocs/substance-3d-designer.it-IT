---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Usa il nodo di Atlas splitter per dividere gli atlanti delle texture in singole texture per l’elaborazione dei materiali scansionati.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/atlas-splitter.png "Icona nodo")

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

## Parametri

<b>Visualizzazione griglia</b> *Booleano*\
Visualizza tutte le forme rilevate in una griglia.

<b>Opacità griglia</b> *Mobile*\
Imposta l&#39;opacità delle linee della griglia quando Grid View è True. Opzione di debug

<b>Opacità selezione griglia</b> *Mobile*\
Imposta l&#39;opacità dell&#39;evidenziazione Selezione griglia se la proprietà Visualizzazione griglia è impostata su True. Opzione di debug

<b>Scala automatica</b> *Booleano*\
Ridimensiona automaticamente le forme per adattarle alla cella della griglia.

<b>Ritaglio automatico</b> *Booleano*\
Ritaglia automaticamente la dimensione di output in base alla forma più grande per ridurre al minimo lo spazio vuoto.

<b>Selezione forma</b> *Numero intero*\
In vista Griglia consente di impostare la cella evidenziata, al di fuori di Vista Griglia consente di impostare la cella restituita.

<b>Ignora forma più piccola di</b> *Mobile*\
Ignora le forme le cui diagonali sono inferiori al valore specificato.

<b>Rotazione automatica</b> *Booleano*\
Ruota automaticamente la forma in base alle proporzioni del rettangolo di selezione.

<b>Rotazione</b> *Mobile*\
Angolo di rotazione della forma globale

<b>Formato Normale Di Input</b> *Numero intero*\
Imposta il formato della normale di input. L’impostazione del formato errato produrrà risultati errati.

<b>Riduci maschera di opacità</b> *Numero intero*\
Riduce la maschera di opacità per rimuovere potenziali disturbi o pixel isolati. Impedisce il rilevamento di forme indesiderate e migliora le prestazioni.

<b>Larghezza dilatazione</b> *Mobile*\
Applica un effetto di dilatazione basato sulla maschera Opacità a tutti i canali tranne Normale e Height.

<b>Abilita input aggiuntivi</b> *Booleano*\
Rende disponibili le impostazioni e gli ingressi per USer 1 e User 2 per qualsiasi mappa aggiuntiva non coperta.

<b>Colore di sfondo personalizzato</b> *Booleano*\
Consente di scegliere un colore di sfondo personalizzato, anziché una dilatazione del contenuto di quel livello.

<b>Colore base sfondo</b> *Float3*\
Colore BG personalizzato per Colore base.

<b>Colore sfondo normale</b> *Float3*\
Colore BG personalizzato per Mappa normale.

<b>Colore sfondo metallico</b> *Mobile*\
Colore BG personalizzato per Metallico.

<b>Colore sfondo rugosità</b> *Mobile*\
Colore BG personalizzato per rugosità

<b>Colore sfondo Height</b> *Mobile*\
Colore BG personalizzato per il Height

<b>Utente 1 Colore Bg</b> *Mobile*\
Colore BG personalizzato per la mappa utente 1 personalizzata

<b>Utente 2 Colore Bg</b> *Mobile* Colore BG personalizzato per la mappa utente 1 personalizzata

## Esempi
