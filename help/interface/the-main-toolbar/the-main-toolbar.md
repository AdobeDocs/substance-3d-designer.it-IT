---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-main-toolbar.html"
breadcrumb-title: ''
description: Scopri la barra degli strumenti principale di Substance 3D Designer per accedere a strumenti e comandi comuni per il tuo flusso di lavoro.
helpx_creative_field: ""
helpx_description: Designer > Interface > Main toolbar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Barra degli strumenti principale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# Barra degli strumenti principale

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Questa pagina descrive la barra degli strumenti principale e il menu di [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html), visualizzati in alto a sinistra nella finestra principale.È costituito da due parti: i menu principali a discesa e i pulsanti di accesso rapido. È possibile accedere a tutte le funzioni dei pulsanti di accesso rapido anche dai menu <b>File</b> e <b>Modifica</b>.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Barra degli strumenti principale](the-main-toolbar.resources/mainmenu.png "Barra degli strumenti principale")

</td>
</tr>
</table>

## Pulsanti di accesso rapido

![](the-main-toolbar.resources/newsubstance.png) <b>Nuovo grafico Substance...:</b> (Ctrl+N)Visualizza la finestra [Nuovo grafico](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md), quindi crea un nuovo pacchetto con un [grafico Substance](../../compositing-graphs/substance-compositing-graphs.md).

![](the-main-toolbar.resources/open.png) <b>Apri...:</b> (Ctrl+O) Apri un [pacchetto di Substance esistente (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

![](the-main-toolbar.resources/saveall.png) <b>Salva tutto:</b> (Ctrl+⇧+S) Salva tutti i pacchetti elencati in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md).

![](the-main-toolbar.resources/undo.png) <b>Annulla:</b> (CTRL+Z) Annulla l&#39;ultima operazione.

![](the-main-toolbar.resources/redo.png) <b>Ripeti:</b> (CTRL+Y) Ripeti l&#39;ultima operazione annullata.

## File

<b>Nuovo:</b> apre un sottomenu per creare un grafico o un pacchetto:

* <b>Nuovo grafico Substance...:</b>(Ctrl+N) Visualizza la finestra [Nuovo grafico](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md) che consente di impostare un nuovo [grafico Substance](../../compositing-graphs/substance-compositing-graphs.md);
* <b>Nuovo grafico della funzione Substance:</b> Crea un nuovo pacchetto con [grafico della funzione Substance](../../function-graphs/function-graphs.md);
* <b>Vuoto:</b> crea un pacchetto vuoto.

<b>Apri...:</b> (Ctrl+O) Apri un [pacchetto Substance esistente (.SBS, .SBSAR, .SBSASM)](../../getting-started/overview/overview.md).

<b>Pacchetti recenti:</b> Visualizza un elenco dei pacchetti aperti di recente. Fare clic su una voce per aprirla.

<b>Apri pacchetti dell&#39;ultima sessione (#)</b>: apre tutti i pacchetti aperti alla chiusura o al termine dell&#39;ultima sessione.

<b>Salva tutto:</b> (Ctrl+⇧+S) Salva tutti i pacchetti aperti, inclusi quelli caricati in background.

<b>Chiudi tutti:</b> chiude tutti i pacchetti aperti.

<b>Ricarica risorse:</b> impone a Designer di ricaricare [tutte le risorse, incluse bitmap e dati SVG](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

<b>Esci:</b> (Ctrl+Q) - Chiudi Substance 3D Designer.

## Modifica

<b>Annulla:</b> (CTRL+Z) Annulla l&#39;ultima operazione.

<b>Ripeti:</b> (CTRL+Y) Ripeti l&#39;ultima operazione annullata.

<b>Preferenze...:</b> Apre la finestra Preferenze.

>[!NOTE]
>
> Questa finestra di dialogo è accessibile dal menu Substance 3D Designer nella barra delle applicazioni di macOS.

## Strumenti

<b>Annulla rendering:</b> (Esc) interrompe l&#39;operazione corrente per la Substance Engine. Può essere utilizzato per interrompere un&#39;operazione indesiderata e pesante.

<b>Il motore di sospensione:</b> (⇧+Esc) sospende il motore di rendering. Ciò consente di velocizzare la modifica di [grafici Substance](../../compositing-graphs/substance-compositing-graphs.md) complessi.

<b>Cambia motore...: </b>(F9) offre una scelta di motori di rendering, tra cui motori GPU (&#39;DirectX&#39; su Windows, &#39;OpenGL&#39; su macOS) e motore CPU (&#39;NEON&#39; su Apple Silicon, &#39;SSE&#39; su tutti gli altri).

<b>Substance Player:</b> Gestire l&#39;integrazione di Designer con Substance Player:

* <b>Individuazione lettore...:</b> Indicare a Designer la posizione di installazione di Windows Media Player.
* <b>Scarica lettore...:</b> Apre la [pagina di destinazione](https://helpx.adobe.com/substance-3d-player/home.html) della documentazione della Substance Player, in cui è possibile scaricare il lettore.

<b>Gestione plug-in...</b>: apre la finestra Gestione plug-in, in cui è possibile installare, caricare e scaricare [Plug-in Python per Substance 3D Designer.](../../scripting/scripting.md)

## Windows

<b>Nuovo Esplora risorse:</b> apre un nuovo ancoraggio Esplora risorse. È possibile aprire più dock di Esplora risorse.

<b>Nuova vista 3D:</b> apre un nuovo ancoraggio vista 3D. È possibile aprire più ancoraggi di Vista 3D.

<b>Nuova visualizzazione libreria:</b> apre un nuovo ancoraggio libreria. È possibile aprire più ancoraggi libreria.

<b>Python Editor:</b> Apre l&#39;editor Python utilizzato per [valutare e creare script](../../scripting/scripting.md).

<b>Ripristina layout:</b> ripristina il layout predefinito dell&#39;area di lavoro. Tutte le finestre verranno riorganizzate e alcune potrebbero essere nuovamente nascoste. Utilizzare in caso di problemi con il layout del programma.

<b>Ingrandisci finestra:</b> Quando un pannello è *ingrandito*, questa opzione lo ingrandisce e ripristina il layout come era *prima* che la finestra fosse ingrandita

<b>Esplora risorse:</b> Mostra/Nascondi [Esplora risorse](../the-explorer-window/the-explorer-window.md).

<b>Grafico:</b> mostra/nasconde le [finestre del grafico](../../interface/the-graph-view/the-graph-view.md).

<b>Parametri:</b> Mostra/Nascondi le [Proprietà](../properties/properties.md).

<b>Console:</b> mostrare/nascondere la finestra della console.

<b>vista 3D:</b> Mostra/Nascondi [vista 3D](../../interface/3d-view/3d-view.md).

<b>Gestione dipendenze:</b> mostrare/nascondere [Gestione dipendenze](../../interface/dependency-manager/dependency-manager.md).

<b>Visualizzazioni 2D:</b> Mostra/Nascondi [vista 2D](../2d-view/2d-view.md).

<b>Libreria:</b> Mostra/Nascondi la [finestra Libreria.](../../interface/the-library/the-library.md)

<b>Barra degli strumenti principale:</b> Mostrare/nascondere la barra degli strumenti principale (solo pulsanti di accesso rapido).

>[!NOTE]
>
> Per ulteriori informazioni sulla gestione dei pannelli di Designer e sulle sue funzioni di personalizzazione e ottimizzazione dei flussi di lavoro, visitate la pagina [Personalizzazione dell&#39;area di lavoro](../../interface/customizing-your-wor/customizing-your-workspace.md) di questa documentazione.

## Aiuto

<b>Tutorials:</b> apre il sito Web [Esercitazioni per Substance 3D](https://substance3d.adobe.com/tutorials/) (precedentemente Substance Academy).<b>\
</b>

<b>Note sulla versione:</b> apre una finestra con il registro delle modifiche della versione più recente.

<b>Requisiti tecnici:</b> mostra i requisiti tecnici per eseguire l&#39;applicazione.

<b>Documentazione:</b> Apre il browser Web predefinito in [questa documentazione](https://www.adobe.com/go/Substance-3D-doc-Designer_it).

<b>Documentazione di scripting:</b> apre il browser Web nei documenti API Python locali.

<b>Forum...:</b> Apre il browser Web nel forum della [community di supporto](https://forum.substance3d.com/) per mettersi in contatto con la community e porre domande.

<b>Segnala un bug...:</b> Apri finestra di segnalazione bug.

<b>Esporta registro...:</b> Esporta i file di registro correnti in un file compresso (.zip) da fornire al supporto tecnico.

<b>Invia feedback...:</b> Apre il browser Web nella home page della [community di supporto](https://www.adobe.com/go/Substance-3D-feedback-Designer_it) di Adobe.

<b>Risorse Substance 3D:</b> sfoglia [contenuti 3D premium](https://substance3d.adobe.com/assets) per gli abbonati (in precedenza Substance Source).

<b>Risorse della community di Substance 3D:</b> ti consente di sfogliare [risorse della community gratuite](https://substance3d.adobe.com/community-assets/) (in precedenza Substance share).

<b>Gestisci il mio account\*:</b> apre la pagina Web per il tuo account Adobe.

<b>Accedi/Esci...\*:</b> Consente di accedere/uscire dal proprio account Adobe.

<b>Schermata Home...:</b> Visualizza la finestra di dialogo [Schermata Home](../../interface/home-screen/home-screen.md).

<b>Novità...:</b> Visualizza una schermata che evidenzia le funzionalità aggiunte all&#39;ultima versione di Designer

<b>Schermata introduttiva...\*:</b> Visualizza la schermata iniziale che guida i nuovi utenti attraverso lo scopo di Designer e la sua posizione nell&#39;[ecosistema Substance 3D](https://helpx.adobe.com/substance-3d.html)

<b>Partner:</b> consente di accedere alle esclusioni di garanzia e agli avvisi per le integrazioni di terze parti dei nostri partner in Designer.

<b>Informazioni su Substance 3D Designer...:</b> Visualizza informazioni sull&#39;applicazione e i relativi componenti, ad esempio il numero di versione.

\*: queste opzioni sono disponibili solo nella versione di Designer installata tramite [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud), che richiede un abbonamento a [Substance 3D](https://www.adobe.com/creativecloud/plans.html?amp%3Bplan=individual#filter=3dar).
