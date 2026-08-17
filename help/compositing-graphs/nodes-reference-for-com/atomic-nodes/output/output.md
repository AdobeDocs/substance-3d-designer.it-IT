---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Output
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# Output

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Output](../../../../assets/comp_output_1.png "Nodo atomico: Output"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Il nodo di output specifica il <b>risultato</b> di un grafico a Substance o uno dei suoi risultati se in esso sono presenti più nodi di output.

L&#39;immagine o il valore connesso al nodo di output di un grafico viene generato da qualsiasi [nodo di istanza](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) che rappresenta questo grafico e può [essere esportato come output del grafico](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md).

</td>
</tr>
</table>

Analogamente, quando un [file SBSAR pubblicato](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) include questo grafico, tale file può generare l&#39;immagine in qualsiasi integrazione o plug-in che utilizza il file.

Dispone di un singolo slot di input indipendente dal tipo, ovvero digita se stesso dopo aver connesso il tipo di dati.

Non ha parametri, ma attributi che sono di grande importanza per etichettare correttamente l&#39;output e metterlo all&#39;uso previsto.

Ogni grafico Substance deve avere *almeno un* nodo di output. Se non esiste alcun output, il grafico non può mai restituire un risultato effettivo e viene generato un [avviso](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md).

## Attributi

|  |  |
| --- | --- |
| <b>Identificatore</b> *Stringa* | Identificatore univoco dell&#39;output. Questa proprietà non può essere lasciata vuota e non può contenere spazi o caratteri speciali.   L&#39;identificatore viene utilizzato perché l&#39;etichetta del nodo è la proprietà &#39;Label&#39; viene lasciata vuota. Può essere utilizzato anche per denominare [texture esportate](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). |
| <b>Descrizione</b> *Stringa* | Descrizione facoltativa utilizzata come descrizione dell&#39;output sono i grafici a Substance. |
| <b>Etichetta</b> *Stringa* | Viene utilizzata come etichetta per il nodo di output e il connettore corrispondente nei [nodi di istanza](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) che rappresentano questo grafico. L&#39;etichetta può contenere spazi e caratteri speciali. |
| <b>Dati utente</b> *Stringa* | Metadati facoltativi che possono essere utilizzati per operazioni di filtro specifiche. [Substance 3D Painter](https://www.adobe.com/products/substance3d/apps/painter.html) utilizza questi dati per [attivare alcune funzionalità](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/content/creating-custom-effects/user-data). |
| <b>Gruppo</b> *Stringa* | Attributo utilizzato per raggruppare gli output per le [modalità di creazione dei collegamenti](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) di Designer.   Gli output con un attributo &quot;Group&quot; identico vengono presentati come una singola connessione nella modalità di creazione del collegamento &quot;Compact Material&quot;. |

## Attributi integrazione

Si tratta di attributi che devono essere utilizzati da integrazioni/plug-in che utilizzano il grafico in un [file SBSAR pubblicato](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

Di conseguenza, non influiscono sul formato delle [esportazioni bitmap](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md). Inoltre, in Designer viene utilizzato solo l&#39;attributo <b>Utilizzo</b>. Per ulteriori informazioni, vedere di seguito.

<b>Utilizzo</b>

|  |  |
| --- | --- |
| <b>Componente</b> *Stringa* | Questa tecnica viene utilizzata per mappare alcuni canali di texture agli input dello shader SVBRDF appropriati nei flussi di lavoro AxF. |
| <b>Utilizzo</b> *Stringa* | Definisce il tipo e l&#39;utilizzo del nodo di output. Questa proprietà è importante in quanto guida:<ul data-preserve-html="true"> <li data-preserve-html="true">Connessione di nodi nei grafici a Substance quando si utilizzano alcune [modalità di creazione del collegamento](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) </li> <li data-preserve-html="true">Connessione delle texture agli shader nella vista 3D (vedere di seguito: &#39;[Informazioni sul ruolo degli usi nella vista 3D](#usages-role-3dview)&#39;)</li> <li data-preserve-html="true">Connessione delle texture ai materiali nelle integrazioni/plug-in</li> </ul> |
| <b>Spazio colore</b> *Stringa* | Imposta lo spazio cromatico in cui deve essere interpretato questo output. Viene utilizzato da alcune integrazioni in altre applicazioni e non ha alcun impatto su Designer. |

### Informazioni sul ruolo degli utilizzi nella vista 3D

Poiché gli output dei grafici sono spesso destinati a essere il risultato finale per un canale di texture specifico, gli output possono essere inviati automaticamente al campionatore appropriato dello shader utilizzato nella vista 3D.

In effetti, un output la cui proprietà *Utilizzo</b> corrisponde all&#39;utilizzo di un campionatore* nella vista 3D verrà collegato a tale campionatore. <b>Ad esempio, un output con utilizzo `basecolor` verrà collegato al campionatore `basecolor` dello shader vista 3D. Ulteriori informazioni sono disponibili nella sezione [Visualizza dati nella vista 3D](../../../../interface/3d-view/3d-view.md) della pagina [Vista 3D](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion).

Fate clic su RMB in un&#39;area vuota della [vista Grafico](../../../../interface/the-graph-view/the-graph-view.md) e selezionate l&#39;opzione <b>Visualizza output in vista 3D</b> nel menu di scelta rapida per connettere tutti gli output ai campionatori della vista 3D con *usi corrispondenti*.

>[!IMPORTANT]
>
> Se sono impostati più utilizzi, ad esempio per assegnare gli utilizzi ai canali in una texture compressa, solo il *primo utilizzo* nell&#39;elenco sarà connesso alla vista 3D. Si tratta di una limitazione nota.

## Output predefinito

Quando un grafico ha più di un output, uno di questi può essere impostato come output predefinito per quel grafico. Specifica quali output devono essere utilizzati per:

* Miniatura di qualsiasi nodo di istanza che rappresenta il grafico
* Visualizzazione di questi nodi di istanza nella vista 2D
* Miniatura del grafico nella libreria (ulteriori informazioni sull&#39;aggiunta di risorse proprie [qui](../../../../interface/preferences-window/project-settings/project-settings.md))

Questa funzione consente di disporre gli output del grafico in qualsiasi ordine indipendentemente da come verrà visualizzato il grafico come nodo.

Per impostare un nodo di output come output predefinito del grafico:

* Fare clic con il pulsante destro del mouse su un nodo Output e selezionare l&#39;azione &#39;Imposta come output predefinito&#39; nel menu di scelta rapida.
* Nelle proprietà del nodo di output, utilizzare il pulsante &#39;Imposta come predefinito&#39; nell&#39;intestazione della sezione &#39;Attributi&#39;.

Di seguito è riportato un esempio di nodi di istanza prima e dopo l&#39;impostazione di un output predefinito:

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="../../../../assets/defaultouput2.png" alt="defaultouput2">
      <br><i>Prima</i>
    </td>
    <td style="border: 0">
      <img src="../../../../assets/defaultouput1.png" alt="defaultouput1">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
