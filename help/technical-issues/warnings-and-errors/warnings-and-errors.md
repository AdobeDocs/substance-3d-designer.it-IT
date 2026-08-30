---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: Trovate le soluzioni per gli avvisi e gli errori più comuni in Substance 3D Designer per risolvere rapidamente i problemi.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avvertenze ed errori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 4%

---


# Avvertenze ed errori

In questa pagina vengono illustrate le segnalazioni di avvisi e messaggi di errore che possono essere visualizzati in [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) e vengono forniti collegamenti alla risoluzione dei problemi relativi agli avvisi in base alla loro origine.

## Panoramica

Durante l’utilizzo dei progetti in Designer, è possibile che vengano visualizzati avvisi e messaggi di errore che segnalano un problema nel progetto:

* **Gli avvisi** vengono visualizzati in testo *giallo* e attirano l&#39;attenzione su un problema che potrebbe causare un risultato indesiderato a causa della mancanza di input o di una configurazione errata. In genere *non bloccano* il tuo lavoro.
* **Gli errori** vengono visualizzati nel testo *rosso* e indicano un errore di calcolo, un risultato imprevisto o l&#39;impossibilità di eseguire un&#39;attività. In genere *bloccano* il tuo lavoro.

In genere, gli avvisi e gli errori vengono visualizzati sull&#39;elemento che li ha attivati e *vengono visualizzati in ogni elemento padre* dell&#39;elemento. Di seguito è riportato un elenco di posizioni comuni in cui vengono segnalati avvisi ed errori:

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Explorer

Per qualsiasi elemento nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) che presenta un avviso, tale avviso viene visualizzato con un&#39;icona ![](warnings-and-errors.resources/warning-icon.png) sul bordo più a destra della voce dell&#39;elemento nell&#39;elenco. Lascia il cursore sull&#39;icona per alcuni secondi per visualizzare una *descrizione comandi* che elenca tutti gli avvisi nel dettaglio.

Seguono queste regole:

* Se l&#39;elemento è nidificato sotto qualsiasi altro elemento (ad esempio, una cartella), gli avvisi vengono visualizzati in caso di compressione.
* Gli elenchi di avvisi sono *cumulativi*, in quanto sono la somma degli avvisi di un elemento *e* di tutti gli avvisi in superficie dei relativi elementi secondari.
* Tutti gli avvisi segnalati dal contenuto di un pacchetto vengono visualizzati nell&#39;elemento *pacchetto* e aggiunti agli avvisi *propri* del pacchetto.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-explorer.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Vista Grafico

Per qualsiasi elemento nella [visualizzazione Grafico](../../interface/the-graph-view/the-graph-view.md) che presenta un avviso, quest&#39;ultimo viene visualizzato con testo colorato nell&#39;*angolo inferiore sinistro* della finestra della vista. Se l&#39;avviso viene attivato da un nodo specifico, tale nodo avrà un badge di avviso ![](warnings-and-errors.resources/warning-badge.png). Lascia il cursore sul badge per alcuni secondi per visualizzare una *descrizione comandi* che elenca tutti gli avvisi nel dettaglio.

Seguono queste regole:

* Se un grafico di origine *istanziato* in qualsiasi altro grafico host presenta uno o più avvisi, il [nodo di istanza](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) per tale grafico di origine avrà un avviso *singolo* `The referenced data has some warnings`.
* Gli elenchi di avvisi sono *cumulativi*, in quanto rappresentano la somma degli avvisi del grafico *e* di tutti gli avvisi dei relativi nodi figlio.
* Tutti gli avvisi di un grafico vengono riportati sull’elemento che lo rappresenta nel pannello Esplora risorse.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-graph.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Proprietà

Per qualsiasi elemento nel pannello [Proprietà](../../interface/properties/properties.md) che presenta un avviso, quest&#39;ultimo viene visualizzato con un&#39;icona ![](warnings-and-errors.resources/warning-icon.png) sul bordo più a destra della voce dell&#39;elemento nell&#39;elenco. Lascia il cursore sull&#39;icona per alcuni secondi per visualizzare una *descrizione comandi* che elenca tutti gli avvisi nel dettaglio.

Seguono queste regole:

* Se l&#39;elemento è nidificato sotto qualsiasi altro elemento (ad esempio, un&#39;intestazione di sezione), vengono visualizzate avvertenze in caso di compressione.
* Gli elenchi di avvisi sono *cumulativi*, in quanto sono la somma degli avvisi di un elemento *e* di tutti gli avvisi in superficie dei relativi elementi secondari.
* Se il [grafico della funzione](../../function-graphs/function-graphs.md) applicato a un [parametro di input](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) include uno o più avvisi, l&#39;elemento del parametro avrà un avviso *singolo* `The [x] parameter's function has some warnings`.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-properties.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### Console

Sia l&#39;avviso che gli errori vengono segnalati nel pannello **Console**, a cui è possibile accedere tramite il menu **Windows** nel [menu principale](../../interface/the-main-toolbar/the-main-toolbar.md). È possibile isolare gli avvisi e gli errori dalle altre voci della console impostando **Canale** su `ErrorMgr`.

>[!NOTE]
>
> Poiché tutto il testo nella console è *selezionabile*, puoi utilizzare questo pannello per *copiare facilmente avvisi e messaggi di errore* e incollarli nello strumento **Ricerca locale** di questa documentazione o in qualsiasi motore di ricerca Internet. Ciò accelera la ricerca di assistenza per la risoluzione dei problemi.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-and-errors.resources/warning-overview-console.png){width="256px"}

</td>
</tr>
</table>

### Messaggi con &quot;(# volte)&quot;

Nell&#39;avviso o nell&#39;errore *esattamente uguale* viene attivato *più di una volta* su un elemento *e* uno qualsiasi dei relativi elementi figlio, questi avvisi verranno *uniti in un unico* e verrà visualizzato il suffisso `(# times)`, indicando quante volte questo avviso o errore è stato segnalato.

## Categorie

Di seguito è riportato un elenco di avvisi ed errori che potresti incontrare in Designer, ordinati in base alla loro origine. I titoli delle categorie sono collegati alla pagina dedicata, che offre spiegazioni e guide per la risoluzione di ogni problema.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Avvertenze nei grafici Substance

* Nessun nodo di output definito
* La funzione del parametro `[x]` contiene alcuni avvisi
* I dati di riferimento presentano alcune avvertenze
* Risorsa di riferimento non trovata
* Il nodo di testo utilizza un font non valido

</td>
<td style="border: 0;" valign="top">

### Avvertenze nei grafici delle funzioni

* Nessun nodo di output definito
* Il nodo di output corrente restituisce un valore di tipo x
* Alcuni nodi Get non hanno un nome di variabile
* Alcuni nodi Set non dispongono di un nome di variabile

</td>
</tr>
</table>

### Avvisi da dipendenze

* Pacchetto dipendente non valido
* Verifica che l’alias &quot;x&quot; sia definito nel progetto
* Impossibile trovare un file corrispondente a questa risorsa
* File collegato non trovato
* Spazio colore non trovato
* Risorsa di riferimento non trovata
* Le porzioni UV vengono assegnate più volte
* Tessere UV non valide
