---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/exporting-bitmaps.html"
breadcrumb-title: ''
description: Scoprite come esportare texture e bitmap dai grafici di composizione Substance per utilizzarli in applicazioni e flussi di lavoro esterni.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting Bitmaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Esportazione di bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 2%

---


# Esportazione di bitmap

Questa pagina spiega come Substance 3D Designer può esportare in molti formati di file Bitmap diversi e come esportare più porzioni UV in batch.Se si desidera [esportare nei file PSD](../exporting-psd-files/exporting-psd-files.md), è disponibile una pagina dedicata separata.

![Esportazione semplificata](exporting-bitmaps.resources/exportflow.png "Esportazione semplificata")

## Esportazione di concetti

Quando esportate una bitmap, tenete presente quanto segue:

* L&#39;esportazione di <b> da un grafico</b> non è un pacchetto. Un pacchetto non genera di per sé il contenuto dell’immagine.
* Il numero (e la risoluzione) delle bitmap esportate è determinato dagli <b>Output</b> di un grafico.
* Tipo di file impostato per tutti gli output/bitmap.
* L&#39;esportazione è diversa dalla [pubblicazione](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md). Assicurati di aver compreso bene la differenza.

## Metodi di esportazione

Una volta che sei pronto per l’esportazione, puoi accedere alla finestra di dialogo Esporta in due modi:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Nella finestra [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), fare clic con il pulsante destro del mouse sul grafico da esportare e scegliere **&quot;Esporta output come bitmap&quot;**

![](exporting-bitmaps.resources/export-explorer.gif)

</td>
<td style="border: 0;" valign="top">

Nella [vista Grafico](../../interface/the-graph-view/the-graph-view.md), facendo clic sul pulsante Strumenti ![](exporting-bitmaps.resources/image2019-9-17-14-44-17.png) e scegliendo **&quot;Esporta output...&quot;**

![](exporting-bitmaps.resources/export-graph.gif)

</td>
</tr>
</table>

## Finestra di dialogo Esporta

La finestra di dialogo Esporta presenta alcune opzioni per personalizzare l’esportazione.

La versione mostrata a destra è la finestra di dialogo standard, la modifica della risoluzione avviene sul grafico, sugli output o impostando la risoluzione principale prima di aprire la finestra di dialogo.

1. <b>Destinazione: </b>percorso per tutti i file da salvare.
1. <b>Formato:</b> tipo di file utilizzato per tutti i file esportati.
1. <b>Pattern</b>: metodo generico per generare i tipi di file in base alle parole chiave dei metadati. Di seguito è riportato un esempio di nome file basato sul primo output, per la verifica.\
   Di seguito sono elencate tutte le opzioni disponibili:
   1. *$(grafico)* - nome del grafico corrente
   1. *$(identificatore)* - identificatore dell&#39;output corrente
   1. *$(descrizione)* - descrizione dell&#39;output corrente
   1. *$(etichetta)* - etichetta dell&#39;output corrente
   1. *$(utente\_dati)* - dati utente personalizzati dell&#39;output corrente
   1. *$(gruppo)* - Gruppo di output dell&#39;output corrente
   1. *$(spazio colore)* - spazio colore dell&#39;output corrente (disponibile solo per le modalità *OCIO* e *Adobe ACE* [gestione colore](../../color-management/color-management.md))
1. <b>Output:</b> attiva o disattiva output e gruppi di output specifici dal grafico. I pulsanti attivano o disattivano tutto. È utile quando viene modificata una sola bitmap.
1. <b>Esportazione automatica:</b> pulsante di attivazione/disattivazione per consentire la riesportazione automatica degli output del grafico non appena viene apportata una modifica. Solo per il grafico corrente. Può essere pesante e lento a seconda delle impostazioni.
1. <b>Pulsante Esporta:</b> Esporta con le impostazioni correnti o chiude la finestra di dialogo.

![Finestra di dialogo per l’esportazione degli output](exporting-bitmaps.resources/fromgraph-1.png "Finestra di dialogo per l’esportazione degli output")

## Finestra di dialogo Esporta (porzioni Batch/UV)

Quando si lavora con le trame con porzioni UV in Designer, la finestra di dialogo Esporta può essere utilizzata in un modo leggermente diverso che consente l&#39;esportazione batch di più porzioni UV contemporaneamente. Assicurati di aver compreso questo flusso di lavoro e di aver assegnato correttamente un [grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md) a uno o più riquadri UV.\
La scheda batch consente inoltre di esportare il grafico a una risoluzione diversa da quella di lavoro (principale).

Avvia la finestra di dialogo con gli stessi metodi descritti in precedenza, assicurandoti di fare clic con il pulsante destro del mouse su *sul grafico assegnato ai riquadri UV in Esplora risorse* o di avere *aperto il grafico assegnato ai riquadri UV* nella vista Grafico quando utilizzi il pulsante Strumenti.

1. <b>Scheda Batch</b>: assicuratevi di selezionare questa scheda invece del metodo <b>Dal grafico </b> standard, altrimenti le opzioni 2-3 non saranno disponibili.
1. <b>Porzioni UV:</b> come per gli output, consente di attivare o disattivare l&#39;esportazione di Porzioni UV specifiche.
1. <b>[Dimensioni output](../../compositing-graphs/output-size/output-size.md): </b>Ignora la risoluzione di esportazione, per lavorare in modo più piccolo ed efficiente, esportando al massimo.

![Finestra di dialogo Output esportazione batch](exporting-bitmaps.resources/batch.png "Finestra di dialogo Output esportazione batch")
