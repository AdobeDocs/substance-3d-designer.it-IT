---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Risolvi i problemi con i parametri del grafico Substance che non funzionano come previsto e trova soluzioni.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: I parametri non funzionano come previsto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---


# I parametri non funzionano come previsto

In questa pagina sono elencate le cause comuni dei parametri che non funzionano come previsto in Substance 3D Designer e sono disponibili passaggi per la risoluzione dei problemi per ciascuno di essi.

## Il parametro non funziona in modalità di anteprima e la risorsa Substance 3D pubblicata (SBSAR)

<b>![(errore)](../../assets/error.svg) Problema</b>

Alcuni parametri esposti per un grafico sono *non elencati* quando si utilizza la [modalità Anteprima](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) in Designer o nell&#39;elenco dei parametri delle risorse Substance 3D (SBSAR) [pubblicate](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) di tale grafico.

<b>![(tick)](../../assets/check.svg)Passaggi consigliati</b>

I parametri mancanti sono probabilmente [parametri statici](../../glossary/glossary.md), che *non possono essere modificati al volo* dopo che il grafico è stato *elaborato*, ovvero elaborato per eseguire il relativo algoritmo in modo rapido ed efficiente. La cottura avviene in Designer ogni volta che il grafico viene *modificato* o *pubblicato*. I parametri interessati da tali limitazioni sono elencati nella sezione [Limitazioni](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) della pagina [Esposizione di un parametro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) di questa documentazione.

Di conseguenza, i parametri statici sono visibili e modificabili in Designer, ma sono *nascosti* in una risorsa Substance 3D pubblicata. È possibile utilizzare la [modalità anteprima](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) per verificare l&#39;applicazione di queste limitazioni prima della pubblicazione in una risorsa di Substance 3D.

Di seguito è riportato un elenco di parametri statici:

| Nodo | Parametro |
| --- | --- |
| Tutti i nodi | Modalità di stampa in porzioni |
| [Colore uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Metodo colore |
| [Processore pixel](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Metodo colore |
| [Fusione](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Metodo fusione Alpha fusione Area di ritaglio |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Metodo fusione |
| [Quadrante](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Immagine di input pattern alfa Filtraggio dell&#39;immagine di input |

## Risultato errato per il grafico della funzione Substance applicato al parametro

<b>![(errore)](../../assets/error.svg) Problema</b>

Un grafico della funzione Substance applicato a un parametro del nodo non genera il valore previsto quando viene utilizzato un numero intero negativo.

<b>![(tick)](../../assets/check.svg) Passaggi consigliati</b>

I numeri interi negativi non sono attualmente supportati correttamente. Come soluzione alternativa, utilizzare il valore intero negativo in un valore [Integer2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) ed estrarlo utilizzando un nodo [Swizzle Integer](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md).
