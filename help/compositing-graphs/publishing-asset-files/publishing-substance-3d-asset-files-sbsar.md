---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/publishing-substance-3d-asset-files-sbsar.html"
breadcrumb-title: ''
description: Scopri come pubblicare i file delle risorse Substance 3D (SBSAR) da Designer per utilizzarli in altre applicazioni e motori.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Publishing Substance 3D asset files (SBSAR)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pubblicazione di file di risorse Substance 3D (SBSAR)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 2%

---


# Pubblicazione di file di risorse Substance 3D (SBSAR)

Questa pagina spiega come Substance 3D Designer può pubblicare pacchetti come file <b>Substance 3D asset</b>, un formato di file speciale con estensione <b>SBSAR</b>, utilizzato sia nell&#39;ecosistema Substance che in altre applicazioni che lo supportano.

In genere è preferibile utilizzare una risorsa di Substance 3D anziché le bitmap, poiché è molto più flessibile e leggera. Se li utilizzi in Substance 3D [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home), [Sampler](https://experienceleague.adobe.com/en/docs/substance-3d-sampler/using/home) o [Player](https://helpx.adobe.com/substance-3d-player/home.html), è più veloce utilizzare la funzionalità [&#39;Invia a...&#39;](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md).

![Pubblicazione dei file SBSAR semplificata](publishing-substance-3d-asset-files-sbsar.resources/exportflow.png "Pubblicazione dei file SBSAR semplificata")

## Concetti di pubblicazione

quando pubblicate un grafico a Substance, è bene tenere presente quanto segue:

* L&#39;utente <b> pubblica un pacchetto</b>, con tutto il relativo contenuto, non un [grafico Substance](../../compositing-graphs/substance-compositing-graphs.md) singolo. Una risorsa Substance 3D consente quindi di generare contenuti da tutti i grafici Substance all&#39;interno di questo pacchetto.
* I pacchetti pubblicati sono <b>completamente autonomi</b>: tutte le risorse necessarie sono incorporate nel file. Questo significa che sono molto più facili da condividere rispetto ai file SBS.
* L&#39;output delle risorse Substance 3D può essere <b>completamente dinamico</b>. [Risoluzione non impostata. È possibile modificare i parametri esposti.](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) Tuttavia, la modifica del grafico non è più possibile.
* Le risorse Substance 3D possono essere utilizzate al di fuori di Designer, in tutti i prodotti Substance 3D di Adobe, Adobe Dimension e in qualsiasi altra applicazione con [integrazione Substance](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home).
* La pubblicazione è diversa dall&#39;[esportazione](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Assicurati di aver compreso bene la differenza.

## Preparazione alla pubblicazione

La pubblicazione richiede più preparazione dell&#39;esportazione delle bitmap. Questo perché le risorse Substance 3D pubblicate sono strumenti dinamici, non solo un&#39;istantanea statica dello stato corrente delle tue texture. In particolare, tenete presente quanto segue:

* Assicuratevi che le risoluzioni dei grafici ([Dimensioni output](../../compositing-graphs/output-size/output-size.md)) siano impostate sul *Metodo relativo all&#39;elemento padre* [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), il che significa che sono dinamiche e possono essere modificate al volo.
* Assicurati che [gli output del grafico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) siano impostati correttamente con nomi, etichette e tag di utilizzo.
* Assicurarsi che [i parametri, se necessari, siano organizzati e denominati correttamente](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
* Se un grafico descrive un materiale, impostate l&#39;attributo [modello di materiale](../graph-parameters/graph-parameters.md) sul modello di tale materiale.
* Assicuratevi che la proprietà [Dimensione output](../../compositing-graphs/output-size/output-size.md) di tutti i nodi [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) sia impostata sul metodo *Assoluto* [di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). In caso contrario, la [risorsa bitmap](../../resources/bitmap-resource/bitmap-resource.md) a cui si fa riferimento verrà salvata con la risoluzione predefinita <b>256\*256</b> nel file di risorse Substance 3D pubblicato, che* influirà sulla qualità* di uno o più output.
* Se nel pacchetto sono presenti dei grafici che non dovrebbero essere disponibili al di fuori di Designer (ad esempio i sottografi helper o &quot;tool&quot; che funzionano solo in un contesto specifico), impostateli in modo che siano nascosti nelle loro proprietà. Vedere più avanti.

## Metodi di pubblicazione

Una volta che si è pronti per la pubblicazione, è possibile accedere alla finestra di dialogo di pubblicazione in due modi, entrambi tramite [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In Esplora risorse, fare clic con il pulsante destro del mouse sul pacchetto e scegliere ![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-9-39-58.png) **file Publish .sbsar...**, tasto di scelta rapida alternativo Ctrl + P.

Dopo aver pubblicato con la finestra di dialogo una volta, puoi anche utilizzare il file ![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-11-15-35.png) **Publish .sbsar come precedente** per ripetere il processo di pubblicazione senza visualizzare le finestre di dialogo, pubblicando immediatamente con le stesse impostazioni.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publish-rightclick.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

In Esplora risorse, facendo clic sul pulsante Publish ![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-9-39-58.png) nella barra degli strumenti superiore.

Dopo aver pubblicato con la finestra di dialogo una volta, è anche possibile utilizzare il pulsante Publish come precedente ![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-11-15-35.png) per ripetere il processo di pubblicazione senza visualizzare le finestre di dialogo, pubblicando immediatamente con le stesse impostazioni.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/publish-toolbutton.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Opzioni di pubblicazione delle risorse

Prima che venga visualizzata la finestra Opzioni Asset Publish, ti verrà chiesto di salvare il file Substance 3D (SBS) se questo non è stato fatto e ti verrà chiesto dove salvare la risorsa Substance 3D. Per evitare di visualizzare le richieste di file e la finestra di dialogo e di scaricare il file più rapidamente, utilizza <b>Publish come metodo</b> descritto in precedenza.

</td>
<td style="border: 0;" valign="top">

![Opzioni di pubblicazione delle risorse](publishing-substance-3d-asset-files-sbsar.resources/publish-dialog.png "Opzioni di pubblicazione delle risorse")

</td>
</tr>
</table>

Sono disponibili le seguenti opzioni:

<b>Percorso file</b> apre una finestra di dialogo per scegliere dove salvare il file della risorsa di Substance 3D. Il percorso predefinito corrisponde ai documenti utente del sistema. Se il pacchetto è stato salvato, il percorso corrisponde al percorso del pacchetto. Se il pacchetto è stato pubblicato durante la sessione, il percorso corrisponde all&#39;ultima posizione di pubblicazione.

<b>La compressione dell&#39;archivio</b> imposta le opzioni di compressione per l&#39;archivio e influisce sulla dimensione dei file.

<b>La generazione di icone mancanti</b> utilizza tecniche incorporate[PBR render](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) per creare miniature per l&#39;attributo di ogni grafico.

<b>I grafici esposti </b>elencano tutti i grafici che saranno esposti in questo pacchetto, vedere di seguito per l&#39;esclusione dei grafici.

>[!NOTE]
>
> **Esposizione Numero Casuale**
> 
> Le impostazioni di esposizione Numero casuale non sono più disponibili nella finestra di dialogo di Publish. Impostare invece l&#39;attributo di inizializzazione casuale del [grafico su Assoluto anziché relativo per evitare che diventi disponibile.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Esclusione di grafici dalla risorsa pubblicata

Alcuni grafici nel pacchetto potrebbero non essere destinati all’uso all’esterno. Questi sottografi sono solitamente intesi come parte di un insieme più grande, una subroutine di un materiale principale.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Per impedire che un grafico diventi visibile o utilizzabile all&#39;interno di un file di risorse di Substance 3D, accedete alle proprietà di tale grafico (fate doppio clic sull&#39;area vuota nella Vista grafico o fate un solo clic sul grafico in Esplora risorse), quindi aprite il rollout <b>Attributi</b>. Imposta <b>Esposto in SBSAR</b> su <b>No</b> per nasconderlo al momento della pubblicazione.

</td>
<td style="border: 0;" valign="top">

![](publishing-substance-3d-asset-files-sbsar.resources/image2020-9-23-10-40-21.png)

</td>
</tr>
</table>

### Avvisi della finestra di dialogo di Publish

La finestra di dialogo Publish a volte presenta delle avvertenze in giallo. Quelle comuni sono elencate di seguito, con una spiegazione e una soluzione.

* Uno o più grafici non dispongono di output\
  Questo messaggio indica che si sta tentando di pubblicare un pacchetto con uno o più grafici che non hanno nodi di output. La soluzione consiste nell&#39;aggiungere [nodi di output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ai grafici con un triangolo giallo di avvertenza.
* Uno o più grafici hanno un parametro di dimensione di output non relativo all&#39;elemento principale\
  Questo messaggio indica che uno o più grafici sono stati impostati su dimensioni di output errate. Di solito sono le proprietà di un grafico stesso. L’avviso indica che non avrai il controllo dinamico della risoluzione su questo grafico quando verrà pubblicato. La soluzione consiste nell&#39;accedere alle proprietà del grafico per quelle con un triangolo giallo e impostare il [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) della dimensione dell&#39;output su *Rispetto al principale*.

## Limitazioni delle risorse Substance 3D

Sebbene la risorsa Substance 3D sia il formato più potente e più dinamico nell&#39;ecosistema Substance, ci sono alcune piccole limitazioni tecniche di cui essere consapevoli.

* I pacchetti di risorse Substance 3D pubblicati sono un formato di file unidirezionale. Non è possibile &quot;decompilare&quot; una risorsa Substance 3D in un file Substance 3D (SBS). L&#39;unico modo per &quot;modificare&quot; una risorsa Substance 3D è modificare il file Substance 3D originale. Puoi comunque utilizzare il contenuto del pacchetto di risorse Substance 3D come nodi all&#39;interno di nuovi grafici Substance (aperti e trascinati), quindi questa non è una limitazione enorme.
* I file delle risorse di Substance 3D hanno versioni che derivano la compatibilità. La Substance Engine principale viene aggiornata periodicamente con nuove funzioni. i pacchetti che utilizzano queste funzioni devono essere letti dalle applicazioni che supportano queste nuove funzioni. Non si tratta di un problema per tutte le applicazioni Substance, in quanto vengono tutte aggiornate contemporaneamente, ma i plug-in e le integrazioni potrebbero presentare ritardi di compatibilità più lunghi.\
  Utilizza le opzioni di visualizzazione Substance Engine compatibilità in [Preferenze progetto](../../interface/preferences-window/project-settings/project-settings.md)per individuare eventuali problemi.
* Alcuni parametri esposti, ad esempio *parametri statici*, sono *nascosti* dopo la pubblicazione di un grafico come parte di una risorsa di Substance 3D. Per un elenco di questi parametri e per ulteriori informazioni sui parametri statici in generale, vedere la sezione [Limitazioni](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) della pagina [Esposizione di un parametro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).
