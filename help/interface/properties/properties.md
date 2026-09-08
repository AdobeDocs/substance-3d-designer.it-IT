---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Usate il pannello Proprietà in Substance 3D Designer per visualizzare e modificare le proprietà dei nodi e i parametri dei grafici.
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proprietà
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Proprietà

Questa pagina presenta il pannello <b>Proprietà </b> di Substance 3D Designer, il relativo layout e i diversi rolluut, categorie e parametri che si trovano all&#39;interno. Si concentra sulle proprietà per [grafici Substance](../../compositing-graphs/substance-compositing-graphs.md). I [grafici a funzione](../../function-graphs/function-graphs.md) e i [grafici FX-Map](../../function-graphs/fxmaps/fxmaps.md) hanno layout più semplici.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Panoramica

Il pannello <b>Proprietà </b> è un pannello sensibile al contesto che cambia in base alla selezione effettuata nella [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) e nella finestra [Esplora risorse](../the-explorer-window/the-explorer-window.md).

</td>
<td style="border: 0;" valign="top">

![Ancoraggio proprietà](../../assets/image2020-11-9-13-49-48.png "Ancoraggio proprietà")

</td>
</tr>
</table>

Consente di modificare le proprietà dei nodi e delle risorse selezionati, insieme a [Visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md), è probabilmente il secondo pannello dell&#39;interfaccia utente più utilizzato in Designer.

Il pannello Proprietà viene suddiviso in alcuni rollup diversi, a seconda della selezione, ad esempio:

* <b>Parametri di base</b> e <b>Input-</b> o <b>Parametri specifici</b> per i nodi
* <b>Attributi</b> e <b>Metadati</b> per la maggior parte dei nodi e dei pacchetti

Una funzione chiave dell&#39;ecosistema Substance, [Esposizione dei parametri](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), viene eseguita tramite il pannello Proprietà.

>[!NOTE]
>
> La maggior parte dei campi numerici supporta *formule matematiche di base* come input, ad esempio `17+3.5`, `7/3`, `(4+2)*3`. Premere *Invio* per convalidare la formula e il risultato verrà inserito nel campo. Se la formula non è valida, il campo torna al valore precedente.\
> Questa funzionalità è supportata anche da alcuni campi numerici in altre parti dell&#39;applicazione, ad esempio la finestra di dialogo [Parametro di esposizione](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

## Nodi e Substance grafici

I nodi e i [grafici a Substance](../../compositing-graphs/substance-compositing-graphs.md) presentano un insieme leggermente sovrapposto di categorie di proprietà e le loro funzionalità sono simili.

<b>I parametri di base</b> e <b>gli attributi</b> sono identici tra nodi e grafici.

I nodi offrono <b>parametri specifici</b> o<b> parametri di istanza</b> (a seconda che siano [nodi atomici](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) o [istanze](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)), nonché <b>valori di input</b> per l&#39;utilizzo di [valori](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

I nodi [Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)e [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)atomici sono eccezioni in quanto presentano <b>Attributi di integrazione</b> e <b>Condizioni</b> per la visibilità. È possibile accedere a questi due insiemi di proprietà anche in modo centralizzato nelle proprietà del grafico, in Input e Output.

I grafici hanno alcune categorie in più. <b>I parametri di input</b> elencano [parametri esposti](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), <b>Input</b> e <b>Output</b> elencano tutte le proprietà dei nodi di input e di output. [Tutte le proprietà del grafico illustrate in dettaglio sono disponibili in una pagina dedicata.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Risorse e pacchetti

Il pannello Proprietà risponde anche alle modifiche apportate alla selezione in [Esplora risorse](../the-explorer-window/the-explorer-window.md). Può essere utile anche per selezionare un grafico (anziché fare doppio clic su un&#39;area vuota) e consente inoltre di modificare le proprietà Pacchetto e [Risorsa](../../resources/resources.md).

I pacchetti contengono **informazioni**, **attributi** e **metadati** sezioni. [I metadati del pacchetto sono descritti in una pagina dedicata.](../../package-metadata/package-metadata.md)

Le risorse dispongono di proprietà specifiche per il tipo, [dettagliate nelle pagine dedicate](../../resources/resources.md).
