---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Scoprite come creare e utilizzare i predefiniti dei parametri in Substance 3D Designer per salvare e applicare le configurazioni dei parametri.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Predefiniti di parametri
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Predefiniti di parametri

I predefiniti di parametro consentono all’utente di memorizzare e trasferire grandi quantità di valori preconfigurati per un insieme di parametri.Possono essere utili in molti scenari e sono particolarmente utili quando è presente una grande quantità di parametri con un&#39;ampia gamma di possibilità.

Esistono due modi per archiviare e caricare i predefiniti, entrambi con casi d’uso diversi, descritti di seguito.

![Menu a discesa Carica/Salva predefinito](parameter-presets.resources/parameter-presets-01.gif "Menu a discesa Carica/Salva predefinito"){width="512px"}

## Predefiniti esterni

I Predefiniti esterni riguardano un file esterno sul disco, un file \*.SBSPRS. Possono essere trasferiti tra grafici e nodi diversi, ma solo all&#39;interno dell&#39;applicazione. Il loro scopo principale è esattamente questo: trasferire un numero di valori troppo grande per copiare uno ad uno.

I predefiniti esterni sono disponibili per tutti i parametri specifici nelle [istanze del grafico](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), per la maggior parte dei parametri specifici nei [nodi atomici](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ([eccezioni sono i parametri che non possono essere esposti](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)) e per i parametri di input esposti nei [parametri](../../graph-parameters/graph-parameters.md)parametri di un grafico a Substance.

Vengono semplicemente salvati e caricati tramite questo menu. I file SBSPRS salvati possono essere caricati su qualsiasi altro nodo o grafico.

>[!NOTE]
>
> Funzioneranno anche le corrispondenze parziali: i parametri memorizzati in un SBSPRS che non esistono nel nodo caricato verranno semplicemente ignorati. Ciò significa che è possibile trasferire proprietà tra nodi che sono per lo più simili, [ad esempio la versione a colori e in scala di grigio di Tile Sampler](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md). Verranno caricati tutti i parametri condivisi. La corrispondenza avviene sull&#39;identificatore e sul tipo.

![Predefiniti incorporati che modificano](parameter-presets.resources/parameter-presets-02.gif "Predefiniti incorporati che modificano"){width="512px"}

## Predefiniti incorporati

I predefiniti incorporati funzionano in modo diverso dai predefiniti esterni. Il loro vantaggio principale è che sono contenuti nel file SBS o SBSAR, in modo che possano essere facilmente trasferiti e caricati in Substance Painter, Maya e 3DS Max (attualmente non disponibili in Substance 3D Sampler, UE4 e Unity). L&#39;utente non deve perdere tempo nemmeno con i file SBSPRS.

ma hanno uno scopo diverso: non è possibile trasferirli tra Nodi e Grafici (a tale scopo dovreste utilizzare i Predefiniti esterni). Possono essere creati solo sui parametri di input delle proprietà di un grafico e solo in modalità anteprima.

Il flusso di lavoro è il seguente:

1. Passa alla <b>modalità anteprima</b> per i <b>parametri di input</b>
1. Imposta i valori sul risultato desiderato
1. Fai clic su <b>+</b> accanto al menu a discesa dei predefiniti per creare un nuovo predefinito incorporato. Il predefinito viene quindi creato e archiviato immediatamente

I predefiniti incorporati non possono essere modificati in seguito, anche se possono essere rinominati. La modifica e la loro rimozione si verificano facendo clic sull&#39;icona a forma di ingranaggio accanto al menu a discesa e sull&#39;icona +. Premete il segno meno accanto a un predefinito per rimuoverlo.

Non è necessario fare altro per abilitare i predefiniti: una volta pubblicati come SBSAR, i predefiniti saranno disponibili in Substance Painter dopo l&#39;importazione.

>[!IMPORTANT]
>
> La scheda <b>Predefiniti</b> è disabilitata quando si utilizza [la modifica in contesto](../../../interface/preferences-window/preferences-window.md).
