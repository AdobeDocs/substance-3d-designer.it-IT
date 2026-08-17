---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ''
description: Scopri come importare, modificare e lavorare con le scene 3D in Substance 3D Designer per visualizzare in anteprima e testare i materiali.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilizzo di scene 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 0%

---


# Utilizzo di scene 3D

![Operazioni con scene 3D](../assets/workingWith3DScenes.png "Operazioni con scene 3D"){zoomable="yes"}

Designer consente di caricare [scene 3D](../glossary/glossary.md) per lavorare sui materiali nel contesto. Qui trovi un elenco dei formati di file supportati per le scene 3D e un elenco delle funzioni supportate per ogni formato. <b>&lt;collegamento necessario></b>

Per lavorare nel contesto, [modificate](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) uno dei [materiali](../glossary/glossary.md) della scena per sostituirlo con un materiale creato in Designer.\
Potete iniziare da zero utilizzando uno qualsiasi dei modelli di grafico delle Substance disponibili in Designer o [estrarre valori e texture](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md) dal materiale della scena 3D come punto di partenza.

Al termine della scena 3D, puoi [esportarla](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md) in un nuovo file da assimilare in un&#39;altra applicazione.

Durante l’esportazione nei formati USD., questo flusso di lavoro può essere completamente <b>non distruttivo</b>, ovvero vengono esportate solo le modifiche e le aggiunte.

Innanzitutto, è necessario caricare una scena 3D su cui lavorare e poter mantenere il suo stato in Designer nelle varie sessioni.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Contenuto delle scene 3D

</td>
<td style="border: 0;" valign="top">

### Caricamento di una scena

</td>
<td style="border: 0;" valign="top">

### file di stato della scena

</td>
</tr>
</table>

## Contenuto delle scene 3D

Quando si carica una scena 3D, Designer ha creato una propria scena per ospitarla.

Potete interagire con i seguenti contenuti della scena:

* <b>Materiali:</b> tutti i materiali utilizzati nella scena possono essere [sostituiti](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) con una copia creata da Designer. Puoi modificare le [proprietà dei materiali](../interface/3d-view/material-properties/material-properties.md) di quella copia, con valori raw o texture da un grafico a Substance.
* <b>Trame:</b> la geometria può essere selezionata direttamente nella finestra della vista o dal [Visualizzatore scene](../interface/3d-view/scene-browser/scene-browser.md), per accedere alle relative azioni materiali ([ignora](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [ripristina](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), [estrai nel grafico della Substance](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md))
* <b>Luci:</b> tutte le luci della scena possono essere disattivate nel [Browser scene](../interface/3d-view/scene-browser/scene-browser.md).
* <b>Fotocamere:</b> tutte le videocamere rilevate nella scena vengono aggiunte come predefinite alla videocamera aggiunta da Designer.

![Contenuto di una scena 3D](../assets/loaded3DScene.png "Contenuto di una scena 3D"){zoomable="yes"}

Designer usa una descrizione USD per la scena 3D. Il layout può essere visualizzato nell&#39;elenco Scene, in cui ogni tipo [USD prim](https://openusd.org/release/glossary.html#usdglossary-prim) ha una propria icona (geometria, materiale, shader, fotocamera, trasformazione, ecc.).

Il [browser scene](../interface/3d-view/scene-browser/scene-browser.md) può essere utilizzato per selezionare, attivare e disattivare il contenuto della scena. Pertanto, ti consigliamo di mantenerla visualizzata quando lavori con scene 3D personalizzate.

## Caricamento di una scena

Nella vista 3D sono disponibili diversi metodi per caricare una scena 3D:

1. Fate doppio clic o trascinate una [risorsa scena 3D](../resources/3d-scene-resource/3d-scene-resource.md) da un [pacchetto](../glossary/glossary.md) nella vista 3D
1. Trascina un elemento di scena 3D dalla [libreria](../interface/the-library/the-library.md) nella vista 3D (a condizione che tu abbia [aggiunto i tuoi contenuti alla libreria](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md))
1. Trascinate un file di scena 3D dal browser di file del sistema alla vista 3D
1. Caricare un file di stato della scena 3D (SBSSCN) insieme alla trama a cui fa riferimento

Solo i metodi 1 e 4 consentono di caricare nuovamente la scena esattamente come l’ultima volta che ci hai lavorato, poiché lo stato della scena è scritto nel file di risorse e stato della scena 3D e salvato nel pacchetto. I metodi 2 e 3 caricano la scena come qualsiasi altro metodo.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Caricamento di una scena 3D - Da una risorsa scena 3D](../assets/load3DScene-3DSceneResource.gif "Caricamento di una scena 3D - Da una risorsa scena 3D"){zoomable="yes"}

Caricamento di una risorsa scena 3D

</td>
<td style="border: 0;" valign="top">

![Caricamento di una scena 3D - Dalla libreria](../assets/load3DScene-Library.gif "Caricamento di una scena 3D - Dalla libreria"){zoomable="yes"}

Caricamento di una scena 3D dalla libreria

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Caricamento di una scena 3D - Da un file di scena 3D](../assets/load3DScene-3DSceneFile.gif "Caricamento di una scena 3D - Da un file di scena 3D"){zoomable="yes"}

Caricamento di un file di scena 3D

</td>
<td style="border: 0;" valign="top">

![Caricamento di una scena 3D - Da un file di stato della scena](../assets/load3DScene-sceneStateFile.gif "Caricamento di una scena 3D - Da un file di stato della scena"){zoomable="yes"}

Caricamento di un file di stato della scena

</td>
</tr>
</table>

>[!NOTE]
>
> La navigazione e la visualizzazione della scena nella vista 3D sono descritte nella [documentazione della vista 3D](../interface/3d-view/3d-view.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer crea sempre il proprio ambiente (DomeLight in USD) e la videocamera, oltre a quelli che potrebbero esistere nella scena.

Tutti gli elementi creati da Designer vengono elencati con <b>etichette in grassetto</b> nell&#39;elenco Scene.

>[!NOTE]
>
> Quando una scena caricata include almeno un ambiente (DomeLight), l&#39;ambiente creato da Designer è *disabilitato per impostazione predefinita* in modo che non interferisca con l&#39;illuminazione dell&#39;ambiente della scena.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Browser scene - Elementi creati da Designer](../assets/sceneBrowser-createdByDesigner.png "Browser scene - Elementi creati da Designer"){zoomable="yes"}

</td>
</tr>
</table>

## File di stato della scena

Dopo aver impostato materiali, videocamere, luci, ecc. nella vista 3D, tale stato può essere salvato in un file di stato della scena (.sbsscn) che può essere caricato in un secondo momento per ripristinarlo. Ad esempio, puoi impostare alcune scene per visualizzare in anteprima diversi tipi di materiali o un ambiente di illuminazione specifico.

![Caricare il file di stato della scena](../assets/loadSceneStateFile.gif "Caricare il file di stato della scena"){zoomable="yes"}

È inoltre possibile utilizzare uno stato di scena salvato come stato predefinito per la vista 3D, in modo che venga utilizzato ogni volta che viene creata una nuova vista 3D. Ciò è utile se desideri visualizzare in anteprima i materiali dei tuoi materiali per impostazione predefinita sulla trama Sfera 2 porzioni con un valore di affiancatura di 2 e una mappa di ambiente specifica.

Le azioni relative ai file di stato della scena si trovano nel menu Scena della vista 3D e sono documentate [qui](../interface/3d-view/3d-view.md).

I file di stato della scena utilizzano il formato XML e utilizzano gli eventuali [alias](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) definiti nelle [impostazioni del progetto](../interface/preferences-window/project-settings/project-settings.md).

>[!NOTE]
>
> Il modulo di rendering non viene salvato nel file dello stato della scena.
