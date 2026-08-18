---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Utilizza la funzione Invia a interoperabilità di Substance 3D Designer per esportare i materiali in altre applicazioni.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Invia a...  Interoperabilità
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 1%

---


# Invia a...  Interoperabilità

![Inviare da Designer alle app Substance 3D](../../../assets/explorer-interop.png "Inviare da Designer alle app Substance 3D"){width="512px"}

Adobe Substance 3D Designer offre interoperabilità con [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) e [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html). Consente di *inviare* e *inviare di nuovo* su cui si lavora rapidamente, semplificando l&#39;iterazione nell&#39;ecosistema Substance 3D.

Il flusso di lavoro è in genere il seguente:

1. Impostare l&#39;attributo <b>Type</b> nelle proprietà di un [grafico a Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md)
1. Nel pannello [Esplora risorse](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), seleziona il pacchetto che desideri inviare
1. Nell&#39;elenco a discesa <b>Publish/Send</b> di Explorer, seleziona l&#39;applicazione di destinazione
1. Apporta modifiche ai grafici
1. Ripeti il passaggio 3 per inviare nuovamente il pacchetto e aggiornare la risorsa esistente inviata con le modifiche

>[!WARNING]
>
> Le funzionalità di interoperabilità sono *non* disponibili nella versione <b>Steam</b>.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Impostazione del tipo di grafico

I grafici a Substance possono avere molte funzionalità. Dovrai definire in anticipo qual è l’esatta funzionalità di un grafico, per assicurarti che possa essere inviato correttamente.

Nella sezione <b>Attributi </b>delle proprietà di un [grafico a Substance](../../../compositing-graphs/graph-parameters/graph-parameters.md) è disponibile un&#39;opzione <b>Tipo</b> con un menu a discesa con le opzioni seguenti:

</td>
<td style="border: 0;" valign="top">

![Attributo Type del grafico a Substance](../../../assets/type-attribute.jpg "Attributo Type del grafico a Substance")

</td>
</tr>
</table>

* **Non specificato** è il tipo predefinito se non è stato impostato. A seconda dell’applicazione a cui invii, potrebbe essere interpretata in modo diverso. [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) utilizzerà per impostazione predefinita Materiale, ad esempio;
* **Il materiale standard** è per materiali PBR multicanale, con [output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) correttamente etichettati;
* **Il materiale decalcomania** è per un materiale PBR multicanale con canale alfa, da applicare come decalcomania in [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **Atlas Material** è per un materiale PBR multicanale costituito da diverse immagini atlas da utilizzare con il [nodo Atlas scatter](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md) in Designer o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **Il filtro** è per filtri di uso generale, entrambi utilizzati in [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html);
* **Mesh-Based Generator** è per i generatori di maschere di input multipli. Utilizzato solo da [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html);
* **Texture Generator** è per mappe a canale singolo, come procedure 2D e rumori;
* **Luce ambiente** è per un ambiente di illuminazione a canale singolo, utilizzato per illuminare scene e oggetti;
* **La texture della luce** è per una texture a canale singolo applicata a una luce fisica.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Menu Invia a

Il processo di invio ha comportato la [pubblicazione](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) di uno o più pacchetti in file di risorse Substance 3D (SBSAR) in background.

L’invio dei contenuti può avvenire nei modi seguenti:

* Fare clic con il pulsante destro del mouse su un pacchetto e aprire <b>Invia a...Sottomenu </b> nel menu di scelta rapida, quindi scegliere <b>Invia a...Opzione </b> per l&#39;applicazione di destinazione;
* Fai clic sul pulsante ![](../../../assets/sendto-icon.jpg) <b>Publish/Invia</b> nella parte superiore del pannello [Esplora risorse](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), quindi scegli <b>Invia a...Opzione </b> per l&#39;applicazione di destinazione.

</td>
<td style="border: 0;" valign="top">

![Menu Publish/Invia a in Esplora risorse](../../../assets/explorer-sendto-displayed.jpg "Menu Publish/Invia a in Esplora risorse")

</td>
</tr>
</table>

### Rinvio

Quando si invia nuovamente un pacchetto *già inviato una volta* all&#39;applicazione *stessa destinazione*, la risorsa verrà *aggiornata* nell&#39;applicazione di destinazione con la nuova versione.

## Invia a Player

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html) supporta *entrambi* <b>file Substance 3D</b> (SBS) e <b>risorse Substance 3D</b> (SBSAR).

L&#39;invio a Windows Media Player richiede che l&#39;eseguibile della Substance Player sia *individuato manualmente* dall&#39;utente, operazione che può essere eseguita:

* Quando viene richiesto se Windows Media Player è *mai stato individuato* dall&#39;installazione di Designer;
* In qualsiasi momento nel menu <b>Strumenti</b>, utilizzando l&#39;opzione <b>Substance Player > Trova...</b>.

In Windows Media Player, la ricezione da Designer richiede che la *directory di installazione* di Substance 3D Designer sia individuata manualmente dall&#39;utente. Questa operazione può essere eseguita:

* Quando viene richiesto se Designer non è mai stato *individuato* dall&#39;installazione di Windows Media Player;
* In qualsiasi momento nel menu <b>Opzioni</b>, utilizzando l&#39;opzione <b>Individua Adobe Substance 3D Designer</b>.

>[!NOTE]
>
> Quando si inviano file Substance 3D (SBS) al lettore, una risorsa Substance 3D (SBSAR) viene pubblicata come *file temporaneo*.

## Problemi

Potresti ricevere errori durante l&#39;invio dei pacchetti, ad esempio:

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


Questo problema si verifica in genere a causa di errori e avvisi standard; correggili per risolvere il problema:

* Nessun nodo [di output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) definito nel grafico. Aggiungi nodi di output e connetti loro qualcosa;
* Variabili mancanti o interrotte in [Ottieni nodi](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) in [grafici di funzione](../../../function-graphs/function-graphs.md). Individuali con il *badge giallo di avvertenza* sui nodi interessati.
