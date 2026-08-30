---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Scoprite come esportare i grafici di composizione Substance come file PSD da utilizzare in Adobe Photoshop e in altri flussi di lavoro di modifica delle immagini.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Esportazione di file PSD
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# Esportazione di file PSD

Substance 3D Designer consente di esportare le texture in un documento Adobe Photoshop o in un file PSD.Questa pagina spiega l’interfaccia speciale utilizzata per convertire i nodi di un grafico in livelli.**Questo processo non è automatico: hai molto controllo, ma è limitato e spesso non è possibile ottenere una corrispondenza precisa tra nodi e livelli.** Inoltre, non vi è alcuna garanzia che il PSD contenga gli stessi output del grafico, a meno che non sia stato esplicitamente impostato per farlo. In genere, più accurati e corretti sono i risultati che si desidera ottenere, maggiore è l&#39;impegno richiesto dall&#39;utente. In generale, l&#39;unica cosa che può essere replicata strettamente in modo non distruttivo è [Blend Nodes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). I livelli di regolazione non sono supportati, così come gli stili di livello o qualsiasi altra cosa oltre i metodi di fusione del livello.

[Substance 3D Designer può anche esportare in file bitmap.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## Finestra di dialogo Esportazione PSD

La finestra di dialogo Esportazione PSD può essere aperta solo con un metodo. Nella [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) del grafico che si desidera esportare in PSD, fare clic sul pulsante ![](exporting-psd-files.resources/image2019-9-17-14-44-17.png) <b>Strumenti</b> e selezionare <b>Esportazione PSD</b>. L&#39;interfaccia diventa visibile nella <b>visualizzazione Grafico</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Interfaccia utente di PSD Exporter](exporting-psd-files.resources/psd-dialog.png "Interfaccia utente di PSD Exporter")

</td>
<td style="border: 0;" valign="top">

1. <b>Nome file e percorso:</b> impostazione della cartella e del nome file per l&#39;esportazione qui. Premete il pulsante Esporta per eseguire l’esportazione.
1. <b>Aggiungi gruppo:</b> aggiunge un gruppo di livelli
1. <b>Menu a discesa Aggiungi livello:</b> scegliere uno dei due metodi per aggiungere un livello. I livelli possono essere aggiunti anche *trascinando i nodi con il pulsante destro del mouse* nella pila.
1. <b>Menu a discesa Rimuovi livello:</b> rimuovi tutti i livelli o solo quelli selezionati.
1. <b>Stack di livelli:</b> la maggior parte del lavoro di installazione viene eseguita qui. L&#39;interfaccia rispecchia opzioni limitate in Photoshop. Imposta il nome del livello, il metodo di fusione e l’opacità qui. Se un livello ha due miniature, la seconda rappresenta il canale di Alpha.

</td>
</tr>
</table>

## Flusso di lavoro

Poiché Photoshop non supporta direttamente i materiali con più output, esistono diversi modi per impostare le PSD. Di seguito è riportato un sommario del metodo più comune.

* Imposta un numero di cartelle per tutti gli output. Una cartella per Colore di base, una per Normale, una per Disturbo e così via.
* Trascina gli output con il pulsante destro del mouse nel gruppo appropriato. Se si vuole mantenere le cose semplici, il PSD può essere lasciato solo a questo.
* Per espandere ulteriormente il PSD: torna alla parte sinistra del grafico, facendo scorrere le fasi intermedie del grafico nel gruppo appropriato. Non sarà possibile condividere livelli tra output e gruppi.

Nel raro caso in cui il tuo PSD sia l&#39;output più importante, puoi creare il grafico in modo da utilizzare solo i metodi di fusione. In tal caso, dovrebbe essere possibile ricreare una versione più modificabile del grafico come un documento a più livelli.
