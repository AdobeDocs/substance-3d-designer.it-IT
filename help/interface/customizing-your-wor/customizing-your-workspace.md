---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/customizing-your-workspace.html"
breadcrumb-title: ''
description: Scoprite come personalizzare il vostro spazio di lavoro in Substance 3D Designer per ottimizzare il flusso di lavoro e le preferenze di layout.
helpx_creative_field: ""
helpx_description: Designer > Interface > Customizing your workspace
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Personalizzazione dell’area di lavoro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---


# Personalizzazione dell’area di lavoro

In questa pagina sono illustrati i modi per disporre i pannelli nell&#39;interfaccia utente di [Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) e sfruttarne le funzionalità per migliorare i flussi di lavoro.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Menu Windows

Questo menu consente di gestire i principali elementi dell’interfaccia utente di Designer. Ciascuna opzione è descritta nella sezione <b>Windows</b> di [questa pagina](../the-main-toolbar/the-main-toolbar.md) sulla barra degli strumenti principale. Qui forniremo ulteriori concetti relativi a questo menu.

### Visualizzare/nascondere una vista

Per visualizzare o nascondere un elemento specifico dell&#39;interfaccia, fare clic sul relativo nome nel menu *Windows*. Gli elementi visualizzati hanno un segno di spunta ![](../../assets/image2015-12-17-10-43-24.png).

### Popolare un’area di ancoraggio con una vista

In Designer, un ancoraggio è un *contenitore separato dal relativo contenuto*. Ciò significa che un ancoraggio <b>Libreria</b> può esistere ed essere vuoto poiché non contiene alcuna libreria *visualizzazione*.

Le opzioni <b>Nuovo Explorer</b>, <b>Nuova visualizzazione 3D</b> e <b>Nuova visualizzazione Libreria</b> creano visualizzazioni che verranno posizionate in base allo stato corrente dell&#39;interfaccia utente:

* Se è disponibile un ancoraggio vuoto, la nuova visualizzazione viene creata *al suo interno*
* Se i dock vuoti sono *non* disponibili, viene creato un *nuovo dock* per contenere la nuova visualizzazione

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Menu Windows](../../assets/windows-menu-1.png "Menu Windows")

</td>
</tr>
</table>

## Ridimensionamento dei dock

È possibile ridimensionare i banchi spostandone i bordi. Gli altri dock verranno ridimensionati dinamicamente per adattarsi.

![Ridimensionamento dei dock](../../assets/interface-customisation-resize.gif "Ridimensionamento dei dock")

## Spostamento dei dock

È possibile spostare qualsiasi ancoraggio nella finestra principale utilizzando la relativa *barra del titolo*. A seconda della posizione in cui viene spostato l’ancoraggio, verrà ridimensionato per adattarlo.

![Spostamento dei dock](../../assets/interface-customisation-move.gif "Spostamento dei dock")

## Ancoraggi a schede

I dock possono essere impilati in schede. Questo è utile per salvare la visualizzazione di immobili o aggregare le visualizzazioni che sono in qualche modo correlate tra loro.

È possibile spostare un ancoraggio mediante la barra del titolo *su un ancoraggio esistente*, ad esempio i punti di ancoraggio non vengono ridimensionati né spostati, ma attorno all&#39;ancoraggio di destinazione viene visualizzato un *fotogramma*.

![Ancoraggi di tabulazione](../../assets/interface-customisation-tab.gif "Ancoraggi di tabulazione")

## Disancoraggio

Un ancoraggio può essere disancorato in una *finestra mobile* che può essere ridimensionata e spostata fuori dalla finestra principale, anche in un altro schermo.

Questo può essere fatto in due modi:

* Spostamento dell&#39;ancoraggio utilizzando la relativa *barra del titolo* e posizionandolo *fuori dalla finestra principale* o su un&#39;area della finestra principale che è *non un ancoraggio*. Puoi ancorare nuovamente questo ancoraggio spostandolo su un altro ancoraggio *nella finestra principale* o facendo clic sul pulsante <b>![](../../assets/dock-icons-redock.png) Riancoraggio</b>;
* Fare clic sul pulsante <b>![](../../assets/dock-icons-undock.png) Disancora</b>. Un ancoraggio disancorato con questo metodo può essere riancorato *solo* facendo clic sul pulsante <b>![](../../assets/dock-icons-redock.png) Riancoraggio</b>.

![Disancoraggio](../../assets/interface-customisation-undock.gif "Disancoraggio")

## Ingrandimento dei dock

È possibile ingrandire qualsiasi ancoraggio per adattarlo all&#39;area o alla *finestra padre*:

* I dock ancorati si estenderanno sull&#39;intera area della *finestra principale*, escluse la barra del titolo, la barra degli strumenti principale e la barra di stato
* I dock non ancorati si estenderanno sull&#39;*intero schermo*

I dock possono essere ingranditi in due modi:

* Posizionare il *cursore sull&#39;ancoraggio* e premere il tasto <b>Maiusc+Barra spaziatrice</b>
* Fare clic sul pulsante Ingrandisci <b>![](../../assets/dock-icons-maximise.png)</b>

I dock ingranditi possono essere ridotti al minimo nelle dimensioni e nella posizione in cui si trovavano *prima di essere ingranditi*. Questo può essere fatto in tre modi:

* Posizionare il *cursore sull&#39;ancoraggio* e premere il tasto <b>Maiusc+Barra spaziatrice</b>
* Fare clic sul pulsante Riduci a icona <b>![](../../assets/dock-icons-minimise.png)</b>
* Apertura del menu <b>Windows</b> e selezione dell&#39;opzione <b>Annulla ingrandimento finestra</b>

>[!NOTE]
>
> È possibile ingrandire solo *un* ancoraggio alla volta.

>[!IMPORTANT]
>
> Quando un dock è ingrandito, alcuni comportamenti dell’interfaccia possono differire:
> 
> * I dock che appaiono o si aggiornano automaticamente lo fanno in background (ad esempio Proprietà, vista 2D)
> * Le voci di menu sono *disabilitate* nel menu **Windows**
> * I pulsanti sono *disabilitati* nella barra del titolo del dock
> * Un ancoraggio ingrandito nella finestra principale *non può essere spostato* utilizzando la barra del titolo

![Ingrandimento dei dock](../../assets/interface-customisation-maximise.gif "Ingrandimento dei dock")

## Blocco dei dock

L&#39;aggiunta di un ancoraggio *impedisce che venga popolato* con altro contenuto o una visualizzazione diversa.

Quando un ancoraggio è bloccato, qualsiasi contenuto futuro che dovrebbe essere visualizzato nel relativo verrà invece *creato un nuovo ancoraggio* per ospitarlo. Questo nuovo dock non verrà bloccato e quindi può aggiornare e ospitare nuovi contenuti.

Per bloccare un ancoraggio, fai clic sul relativo pulsante ![](../../assets/dock-icons-pin.png) <b>Pin</b>. Puoi quindi *sbloccarlo* utilizzando il pulsante ![](../../assets/dock-icons-pinned.png) <b>Sblocca</b> per renderlo nuovamente *disponibile* per ospitare nuovi contenuti.

*È possibile bloccare più ancoraggi* alla volta, inclusi più ancoraggi dello *stesso tipo*.

L’aggiunta di dock consente di avere le seguenti capacità:

* Visualizzazione e modifica delle proprietà di più nodi contemporaneamente
* Visualizzazione simultanea di due o più bitmap
* Lavorare su più grafici contemporaneamente

![Blocco dei dock](../../assets/interface-customisation-pin.gif "Blocco dei dock")

## Chiusura dei bacini

È possibile chiudere qualsiasi ancoraggio facendo clic sul relativo pulsante ![](../../assets/dock-icons-close.png) <b>Chiudi</b>.

## Reimpostazione del layout dell&#39;interfaccia

È possibile ripristinare l&#39;intera interfaccia utente nel layout predefinito aprendo il menu <b>Windows</b> e selezionando l&#39;opzione <b>Ripristina layout</b>.

Anche lo stato di visualizzazione verrà reimpostato, ovvero i dock chiusi potrebbero essere *riaperti* (ad esempio, vista 3D) e quelli visualizzati potrebbero essere *chiusi* (ad esempio, console, gestione dipendenze, dock creati da plug-in).

![Ripristina layout](../../assets/interface-customisation-reset.gif "Ripristina layout")
