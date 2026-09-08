---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: Importa e utilizza la grafica vettoriale di SVG come risorse in Substance 3D Designer per la creazione di materiale procedurale.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risorsa grafici vettoriali (SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---


# Risorsa grafici vettoriali (SVG)

Substance 3D Designer supporta una forma limitata di grafica vettoriale, tramite il formato di grafica vettoriale scalabile. I file SVG possono essere inseriti come risorse in diversi modi, da utilizzare come risorse per i grafici.

I file SVG [possono essere creati o modificati tramite il nodo atomic SVG,](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) possono essere creati anche da [UV to SVG baker.](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)

>[!NOTE]
>
> I file di Adobe Illustrator (**.ai**) sono *non* attualmente supportati.

## Archiviazione SVG

Lo spazio di archiviazione SVG dipende da se è collegato o importato. I file SVG importati sono incorporati nel file SBS e non richiedono [file esterni come Bitmap](../../resources/bitmap-resource/bitmap-resource.md) e possono essere modificati utilizzando gli [strumenti di modifica vettoriale](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Attributi SVG

Le risorse SVG in un pacchetto hanno diversi attributi che è possibile personalizzare. La maggior parte degli attributi non ha uno scopo principale e viene utilizzata per i filtri libreria, ma solo una piccola parte incide sulla qualità del rendering.

| Nome attributo | Scopo |
| --- | --- |
| Identificatore | Utilizzato per fare riferimento alla risorsa SVG in un pacchetto, deve essere univoco. |
| Percorso del file | Percorso su disco del file SVG a cui fa riferimento la risorsa. |
| Descrizione | Descrizione visualizzata nelle descrizioni comandi [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) e [Libreria](../../interface/the-library/the-library.md) per questa risorsa. |
| Categoria | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Etichetta | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Autore | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| URL dell&#39;autore | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Tag | Utilizzato per [ordinare e gestire la risorsa](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) nella [libreria](../../interface/the-library/the-library.md). |
| Dati utente | Dati aggiuntivi opzionali, non utilizzati nella grafica vettoriale. |
| Mostra nella libreria | Determina se la risorsa SVG deve essere nascosta nella [visualizzazione Libreria.](../../interface/the-library/the-library.md) |
| Qualità grafica vettoriale | Influisce sulla qualità del rendering. L&#39;intervallo non è lineare e si ottiene la migliore qualità a 0,5. |

## SVG authoring

Poiché è supportato solo un insieme limitato di funzionalità, l’SVG di creazione è vincolato.

In generale, è vero quanto segue:

* Solo semplici forme e tracciati primitivi possono essere disegnati correttamente;
* Il tratto è supportato ma produce solo un tratto di 1 pixel di larghezza e lo stile del tratto viene ignorato;
* Gli stili di linea tratteggiata si interrompono definitivamente;
* Il testo deve essere convertito in tracciati/contorni per essere sottoposto a rendering;
* [I percorsi composti](https://helpx.adobe.com/ie/illustrator/using/combining-objects.html#compound_paths) non sono supportati;
* Le funzioni avanzate, come le sfumature, non sono supportate;
* Gli elementi di stile per le proprietà CSS non sono supportati.

## Opzioni di esportazione consigliate

Le opzioni di esportazione sono leggermente diverse per ogni applicazione:

### Adobe Illustrator

[Illustrator](https://www.adobe.com/products/illustrator.html) consente il massimo controllo sulle esportazioni di SVG se presti attenzione alle seguenti opzioni.

* Usa solo <b>Salva con nome</b>, *non* Esporta con nome.
* <b>Il profilo SVG</b> non ha molta importanza, anche se per lo più il profilo Tiny utilizzerà per impostazione predefinita le impostazioni sicuramente corrette;
* <b>I font</b> devono essere impostati su <b>Converti in contorno</b> per funzionare;
* <b>Le proprietà CSS</b> devono essere *non* impostate su Elementi stile. Tutte le altre opzioni funzioneranno.
* Deseleziona <b>Mantieni funzionalità di modifica di Illustrator</b>;
* Deseleziona <b>Reattivo</b>;
* I tratti non funzionano correttamente. Utilizza <b>Oggetto > Tracciato > Traccia contorno</b> per visualizzarli.

L’immagine a destra mostra le opzioni di esportazione consigliate, fai clic su di essa per visualizzarla a grandezza naturale.

>[!IMPORTANT]
>
> Le tavole da disegno possono influire sul risultato del file SVG generato. Alcuni modelli di file Illustrator presentano più tavole da disegno.\
> Provate a fare in modo che una sola tavola da disegno sia ritagliata correttamente e a farla selezionare nella finestra Tavola da disegno quando viene salvata come SVG.

![Opzioni di esportazione di Illustrator SVG](../../assets/svg-export-options-ai.jpg "Opzioni di esportazione di Illustrator SVG"){width="512px"}

### Inkscape

Inkscape viene salvato in modo nativo come SVG, ma con un minore controllo sul formato del file. I file Inkscape funzionano principalmente in modalità nativa nell’applicazione, ma con alcune limitazioni:

* I tratti vengono visualizzati solo con una larghezza di 1 px in Substance 3D Designer. Utilizza <b>Tracciato > Traccia tracciato</b> per ripristinarne il funzionamento.
* Il testo non funzionerà. Utilizzare <b>Percorso > Oggetto in percorso</b> per far funzionare il testo.

### Adobe Photoshop

Photoshop ha un esportatore di SVG molto limitato (<b>File > Esporta > Esporta come..</b>) che al momento non è in grado di produrre risultati corretti per Substance 3D Designer. Potete ottenere le informazioni su forma e tracciato, ma Stile viene sempre salvato come Elementi, il che non è compatibile.

Può essere utilizzato per semplici maschere di forma in bianco e nero, in cui una soluzione consiste nell&#39;estrarre l&#39;Alpha dalle SVG utilizzando [Divisione Alpha](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md).

In alternativa, un SVG esportato da Photoshop può essere [Importato](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md), che consente di [modificare le informazioni sullo stile in modo nativo all&#39;interno dell&#39;applicazione.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
