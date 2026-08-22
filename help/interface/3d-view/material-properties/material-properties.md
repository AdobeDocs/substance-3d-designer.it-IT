---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/3d-view/material-properties.html"
breadcrumb-title: ''
description: Configura le proprietà del materiale nella vista 3D per visualizzare in anteprima e regolare l'aspetto dei materiali Substance sugli oggetti 3D.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Material properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Proprietà dei materiali
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1345'
ht-degree: 29%

---


# Proprietà dei materiali

La [vista 3D](../../../interface/3d-view/3d-view.md) esegue il rendering della superficie dei modelli utilizzando un programma denominato *shader*. Lo shader definisce il materiale
applicato al modello utilizzando un elenco di proprietà che influiscono su vari aspetti dell&#39;aspetto del modello.

Il menu **Materiali** della vista 3D consente di verificare quale shader viene utilizzato per ciascun materiale della scena.

<a name="openpbr"></a>

## OpenPBR

Per impostazione predefinita, Designer utilizza il modello di materiale [OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/), che supporta diversi effetti complessi, ad esempio l&#39;anisotropia,
trasmissione e fuzz.

I [modelli di grafici](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#graph-templates) predefiniti e i [campioni di materiale](../../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md#material-samples) inclusi in Designer sono tutti basati sul modello di OpenPBR.

Le proprietà di questo shader seguono il [riferimento a un parametro di OpenPBR](https://academysoftwarefoundation.github.io/OpenPBR/#parameterreference) e sono *condivise* in Rasterizer,
[moduli di rendering 3D](../3d-renderers/3d-renderers.md) per Pathtracer GPU e OpenGL.

+++ UV

| Parametro | Tipo | Predefinito | Descrizione |
|---------------------------------|---------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Affiancamento | A virgola mobile | 1.0 | Quantità di ripetizioni di texture in una cella UV, dove un valore più alto<br/>produce più ripetizioni di texture. |
| Abilita dimensioni fisiche da grafico | Booleano | False | Regola automaticamente la porzione in base alla [Dimensioni fisiche](../../../compositing-graphs/graph-parameters/graph-parameters.md)<br/>del grafico per rappresentare il materiale alla scala appropriata. |
| Scala UV | Float2 | 1.0, 1.0 | Regola la scala dell&#39;affiancatura in base a un fattore separato per U e V, dove <br/>un valore più elevato genera un maggior numero di ripetizioni della texture. |

+++

+++ Base

| Parametro | Tipo | Predefinito | Descrizione |
|-------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 1.0 | Moltiplicatore sull&#39;intensità del riflesso dalla base diffusa e metallica. |
| Colore | Float3 (RGB) | 0.8, 0.8, 0.8 | Colore del riflesso dalla base diffusa e metallica. |
| Metallicità | A virgola mobile | 0.0 | Consente di specificare l’aspetto metallico del materiale di base. (Quadra la base dal dielettrico puro al metallo puro) |
| Rugosità diffusa | A virgola mobile | 0.0 | Rugosità della riflessione diffusa. Più alti sono i valori, più piatta apparirà la superficie. |

+++

+++ Speculare

| Parametro | Tipo | Predefinito | Descrizione |
|------------|--------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 1.0 | Moltiplica la riflettanza speculare. |
| Colore | Float3 (RGB) | 1.0, 1.0, 1.0 | Colore del riflesso dello specular. (Controlla la tinta dei bordi fisica per i metalli,<br/>e una tinta complessiva non fisica per i dielettrici) |
| Ruvidità | A virgola mobile | 0.3 | Rugosità del riflesso specular. I numeri più bassi producono riflessi più netti, mentre quelli più alti producono riflessi più sfocati.<br/> |
| Anisotropia | A virgola mobile | 0.0 | La distorsione direzionale della rugosità della base metallica/dielettrica, risultante<br/>in luci sempre più allungate lungo la direzione tangente. |
| IOR | A virgola mobile | 1.5 | Indice di rifrazione della base dielettrica. |

+++

+++ Trasmissione

| Parametro | Tipo | Predefinito | Descrizione |
|------------------|--------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 0.0 | Peso della miscela tra la base dielettrica trasparente e opaca.<br/>Maggiore è il valore, maggiore sarà la trasparenza del materiale. |
| Colore | Float3 (RGB) | 1.0, 1.0, 1.0 | Controlla il colore della base trasparente dovuto all&#39;assorbimento volumetrico<br/>della legge della birra sotto la superficie. |
| Profondità | A virgola mobile | 0.0 | Specifica la distanza di percorrenza della luce all&#39;interno della base trasparente prima che <br/> diventi esattamente `transmission_color` in base alla legge di Beer. |
| A dispersione | Float3 (RGB) | 0.0, 0.0, 0.0 | Controlla il colore della luce distribuita volumetricamente all’interno della base trasparente. |
| Anisotropia | A virgola mobile | 0.0 | Quantità di distorsione direzionale, o anisotropia, della dispersione volumetrica<br/>nella base trasparente. |
| Scala di dispersione | A virgola mobile | 0.0 | Scala in modo lineare la quantità di dispersione. |
| Numero Abbe | A virgola mobile | 20.0 | Numero Abbe fisico del mezzo dielettrico, che descrive quanto<br/>l&#39;indice dielettrico di rifrazione varia a seconda delle lunghezze d&#39;onda. |

+++

+++ Sottosuperficie

| Parametro | Tipo | Predefinito | Descrizione |
|--------------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 0.0 | Peso della miscela che regola la base dielettrica opaca tra <br/>riflessione diffusa e dispersione sottosuperficiale. |
| Colore | Float3 (RGB) | 0.8, 0.8, 0.8 | Colore del riflesso osservato del mezzo di dispersione della sottosuperficie. |
| Raggio | A virgola mobile | 1.0 | Scala di lunghezza del percorso libero medio di dispersione della sottosuperficie. |
| Scala raggio | Float3 (RGB) | 1.0, 0.5, 0.25 | Moltiplicatore RGB a subsurface_radius, che fornisce la dispersione per canale<br/>percorsi medi liberi. |
| Anisotropia | A virgola mobile | 0.0 | Controlla la funzione di fase della dispersione del sottosuolo, dove zero<br/>dispersione la luce in modo uniforme, i valori positivi dispersione in avanti e i valori negativi<br/>dispersione all&#39;indietro. |

+++

+++ Rivestimento

| Parametro | Tipo | Predefinito | Descrizione |
|------------|--------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 0.0 | Il peso della presenza di uno strato riflettente trasparente sopra il materiale.<br/>Usare per materiali quali pittura per auto o un livello oleoso. |
| Colore | Float3 (RGB) | 1.0, 1.0, 1.0 | Colore della trasparenza dello strato di rivestimento, dovuto all&#39;assorbimento nel rivestimento. |
| Ruvidità | A virgola mobile | 0.0 | Rugosità dei riflessi del rivestimento trasparente.<br/>Più basso è il valore, più nitido sarà il riflesso. |
| Anisotropia | A virgola mobile | 0.0 | Distorsione direzionale della rugosità del livello del rivestimento trasparente,<br/>risultante in luci sempre più allungate lungo la direzione della tangente del pelo. |
| IOR | A virgola mobile | 1.6 | Indice di rifrazione dello strato riflettente trasparente. |
| Oscuramento | A virgola mobile | 1.0 | Modula l’effetto fisico di scurimento del rivestimento. |

+++

+++ Fuzz

| Parametro | Tipo | Predefinito | Descrizione |
|-----------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 1.0 | Spessore della presenza di uno strato di fuzz che può essere utilizzato per approssimare microfibre,<br/>per tessuti quali velluto e satinato nonché grani dust. |
| Colore | Float3 (RGB) | 1.0, 1.0, 1.0 | Il colore del livello Fuzz. |
| Ruvidità | A virgola mobile | 0.5 | Rugosità del livello Fuzz. |

+++

+++ Emissione

| Parametro | Tipo | Predefinito | Descrizione |
|-----------|--------------|---------------|------------------------------------------------------|
| Luminanza | A virgola mobile | 0.0 | Quantità di luce emessa, indicata come luminanza in nit. |
| Colore | Float3 (RGB) | 1.0, 0.0, 0.0 | Il colore della luce emessa. |

+++

+++ Pellicola sottile

| Parametro | Tipo | Predefinito | Descrizione |
|-----------|-------|---------|-------------------------------------------------------------------------------------------------------|
| Spessore | A virgola mobile | 0.0 | Peso di copertura del film sottile.<br/>Utilizzare per materiali quali la pittura per auto con più toni o le bolle di sapone. |
| Spessore | A virgola mobile | 0.5 | Il thickness dello strato sottile sulla base. (in micrometri) |
| IOR | A virgola mobile | 1.4 | L&#39;indice di rifrazione della pellicola sottile. |

+++

+++ Geometria

| Parametro | Tipo | Predefinito | Descrizione |
|-------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Opacità | A virgola mobile | 1.0 | Opacità dell&#39;intero materiale. |
| Con pareti sottili | Booleano | False | Se è true, la superficie è a due lati e rappresenta un guscio infinitesimalmente sottile.<br/>Ideale per oggetti estremamente geometricamente sottili come foglie o carta. |
| Normale | Float3 (RGB) | 0.5, 0.5, 1.0 | Immettete una normale geometrica per la superficie. |
| Tangente | Float3 (RGB) | 1.0, 0.5, 0.0 | Immettete una tangente geometrica. |
| Rivestimento normale | Float3 (RGB) | 0.5, 0.5, 1.0 | Inserite la normale per lo strato di rivestimento. |
| Tangente rivestimento | Float3 (RGB) | 1.0, 0.5, 0.0 | Immettete una tangente geometrica per il livello di rivestimento. |
| Altezza | A virgola mobile | 0.5 | Quantità di Spostamento (o rilievo) nella direzione della normale.<br/>Quando il height è uguale al livello del height, non si verifica spostamento.<br/>Lo Spostamento è un cambiamento scalare nella posizione della superficie verso una superficie normale non perturbata<br/>fusa.<br/>Nei casi in cui lo spostamento tassellato non è possibile o desiderato, è possibile implementare <br/>il height come mappa di rilievo. |
| Livello di altezza | A virgola mobile | 0.5 | Valore del height corrispondente all&#39;assenza di spostamento (valore di livello zero).<br/>Il livello del Height sposta (ma non ridimensiona né capovolge) lo spostamento rispetto<br/>alla superficie dell&#39;oggetto non spostato.<br/>Se il livello del height è 0, lo spostamento è superiore.<br/>Se il livello del height è 1, tutto lo spostamento si trova sotto la superficie, ma mantiene comunque<br/>la stessa scala e direzione. |
| Scala altezza | A virgola mobile | 1.0 | Scala dello spostamento o del rilievo nelle unità di spazio della scena.<br/>L&#39;ampiezza e la direzione della scala sono indipendenti dal valore del livello del height. |
| Occlusione ambientale | A virgola mobile | 1.0 | Mappa di occlusione ambientale per scurire le aree occluse.<br/>Bianco (1,0) significa completamente illuminato, nero (0,0) significa completamente occluso. |

+++

### Compatibilità con i grafici esistenti

Alcune proprietà dei materiali OpenPBR hanno identificatori di utilizzo diversi rispetto ad altri modelli inclusi in Designer.
Designer abbina automaticamente alcuni identificatori per garantire la compatibilità con OpenPBR come modello predefinito.

+++ Mapping da legacy a utilizzo OpenPBR

| Precedente | OpenPBR |
|-------------------------|-----------------------------|
| metallico | metallicità |
| specularEdgeColor | specularColor |
| ruvidità | specularRoughness |
| anisotropiaLivello | specularRoughnessAnisotropy |
| IOR | specularIOR |
| absorptionColor | transmissionColor |
| absorptionDistance | transmissionDepth |
| translucenza | subsurfaceWeight |
| scatteringColor | subsurfaceColor |
| scatteringDistance | subsurfaceRadius |
| scatteringDistanceScale | subsurfaceRadiusScale |
| coatOpacity | coatWeight |
| sheenOpacity | fuzzWeight |
| sheenColor | fuzzColor |
| sheenRoughness | fuzzRoughness |
| con emissioni | emissionColor |

+++

### Ulteriore lettura

Per ulteriori informazioni su OpenPBR, ecco alcune risorse:

* [Adobe di blog](https://blog.adobe.com/en/publish/2023/08/08/openpbr-strengthens-interoperability-enabling-enhanced-creativity)
* [White paper](https://academysoftwarefoundation.github.io/OpenPBR/)
* [OpenPBR BSDF su GitHub](https://github.com/adobe/openpbr-bsdf)
* [Designer 16.0: supporto di OpenPBR](../../../release-notes/version-16-0/version-16-0.md#openpbr-support)

<a name="adobe-standard-material"></a>

## Materiale standard Adobe

Il modello Adobe Standard Material (ASM) è stato introdotto in Designer 11.2 ed è lo shader predefinito di Designer.
fino alla versione 15.1

Mentre Designer viene spostato in OpenPBR come nuovo modello predefinito, ASM è ancora incluso e le sue proprietà sono condivise
attraverso i moduli di rendering Rasterizer, Pathtracer GPU e OpenGL [3D](../3d-renderers/3d-renderers.md).

Modello documentato [qui](https://experienceleague.adobe.com/it/docs/substance-3d/general-knowledge/asm/adobe-standard-material).

<a name="usdpreviewsurface"></a>

## UsdPreviewSurface

Lo scopo del modello UsdPreviewSurface è l&#39;anteprima dei materiali con un set di funzionalità di base che promuova la compatibilità
tra moduli di rendering che includono USD e/o Hydra.

In Designer, questo modello di materiale è supportato solo dal rasterizzatore e dal Pathtracer GPU [moduli di rendering 3D](../3d-renderers/3d-renderers.md).

Modello documentato [qui](https://openusd.org/dev/spec_usdpreviewsurface.html).
