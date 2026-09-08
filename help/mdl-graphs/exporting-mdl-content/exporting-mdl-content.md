---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Scopri come esportare contenuti MDL da Substance 3D Designer per utilizzarli in applicazioni e renderer esterni.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Esportazione di contenuto MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# Esportazione di contenuto MDL

Questa pagina descrive i processi di esportazione relativi a [grafici MDL](../../mdl-graphs/mdl-graphs.md) e ai materiali in Substance 3D Designer.

## Panoramica

Una volta creato in Designer, il materiale MDL deve essere esportato in un formato che possa *contenere la definizione del materiale* e possa essere letto dai moduli di rendering che supportano MDL. MDL utilizza formati proprietari per trasportare definizioni di materiali, chiamati moduli MDL, scritti e confezionati in formati diversi che possono essere esportati da Designer.

>[!NOTE]
>
> Tutti questi formati possono essere aperti direttamente con un *editor di testo* - a volte dopo averli disimballati con un gestore di archivio - per ispezionare la definizione del materiale in loro possesso.

## Modulo MDL (\*.mdl)

Questo è il formato di file di scambio fondamentale per le definizioni dei materiali. Un modulo MDL definisce quanto segue:

* caratteristiche e comportamento del materiale
* i parametri esposti e i valori predefiniti
* le relative annotazioni (ad esempio, metadati): autore, tag, categorie, ...

L&#39;esportazione di un modulo MDL viene eseguita al livello *pacchetto*. Per esportare un modulo MDL per un determinato pacchetto, fare clic sul pulsante ![](../../assets/mdl-export-module-icon.png) <b>Esporta modulo MDL</b> in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) o selezionare la stessa opzione nel menu di scelta rapida del *pacchetto*. Selezionare un percorso e un nome di destinazione per il modulo MDL esportato e viene visualizzata la finestra di dialogo <b>Esporta report</b> con l&#39;elenco dei messaggi registrati durante il processo di esportazione.

Il modulo esportato conterrà le definizioni di *tutti* i materiali MDL definiti da un [grafico MDL](../../mdl-graphs/mdl-graphs.md) nel pacchetto.

>[!NOTE]
>
> Ulteriori informazioni sui moduli MDL nelle sezioni 4 e 15 della [specifica MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) di NVIDIA.

>[!NOTE]
>
> Gli avvisi seguenti questo modello: `x appears to be invalid whereas it was expected to be an mdl::call` sono causati dal modo in cui i materiali MDL vengono elaborati nei grafici MDL e sono *sicuri da ignorare*.

![Percorso di esportazione MDL](../../assets/mdl-export-module.png "Percorso di esportazione MDL")

*I percorsi &quot;Esporta modulo MDL&quot; in Esplora risorse e la finestra di dialogo Esporta report risultante*

### Predefinito MDL (\*.mdl)

Un predefinito del modulo MDL è in gran parte identico al modulo su cui è basato, con l&#39;unica differenza che contiene un diverso set di valori predefiniti. Ulteriori informazioni [qui](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details).

Un predefinito per un materiale MDL assegnato a un materiale di scena `my_material` può essere esportato dai seguenti percorsi:

* Nel pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), facendo clic su <b>RMB</b> nella risorsa grafico MDL e selezionando l&#39;opzione <b>Esporta predefinito...</b> nel menu di scelta rapida
* Il pannello [Vista 3D](../../interface/3d-view/3d-view.md) utilizzando l&#39;opzione di menu <b>Materiali > il mio\_materiale > Esporta predefinito...</b>

L&#39;opzione di menu apre la finestra di dialogo <b>Esporta predefinito materiale MDL</b>, che offre le seguenti opzioni:

* <b>Directory</b>: percorso di destinazione in cui viene esportato il modulo MDL
* <b>Nome file MDL</b>: nome del modulo MDL
* <b>Incorpora moduli MDL importati</b>: se il modulo MDL si basa su moduli importati, ovvero presenta dipendenze del modulo, selezionando questa opzione le dipendenze del modulo verranno *incorporate* nel modulo MDL esportato, rendendolo *autosufficiente* a scapito della dimensione del file e dell&#39;ereditarietà dinamica

Il predefinito esportato utilizzerà i *valori correnti* dei parametri del materiale nella vista 3D come *nuovi valori predefiniti*. Questi valori possono essere modificati utilizzando l&#39;opzione <b>Materiali > il mio\_materiale > Modifica</b>, che visualizzerà i parametri esposti del materiale nel pannello Proprietà.

>[!WARNING]
>
> Durante l&#39;esportazione di un modulo MDL dal pannello [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), viene generato un modulo MDL contenente *tutti* i materiali MDL definiti da un grafico MDL nel pacchetto. L&#39;esportazione di un predefinito MDL dalla [vista 3D](../../interface/3d-view/3d-view.md) genera un modulo MDL contenente *solo* la definizione dei materiali MDL applicata al *materiale selezionato* nel menu - `my_material` in questo esempio.

![Percorso di esportazione predefiniti MDL](../../assets/mdl-export-preset.png "Percorso di esportazione predefiniti MDL")

*Il percorso &quot;Esporta predefinito&quot; nella vista 3D e la finestra di dialogo risultante Esporta predefinito materiale MDL*

## Archivio modulo MDL (\*.mdr)

Un archivio di moduli MDL combina i moduli MDL, vedere sopra, con risorse quali *texture* e file readme in un *singolo file trasportabile*.

L&#39;esportazione di un archivio del modulo MDL viene eseguita al livello *pacchetto*. Per esportare un archivio del modulo MDL per un determinato pacchetto, fare clic sul pulsante ![](../../assets/mdl-export-module-icon.png) <b>Esporta archivio moduli MDL</b> in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) oppure selezionare la stessa opzione nel menu di scelta rapida del *pacchetto*. Selezionare un percorso e un nome di destinazione per l&#39;archivio del modulo MDL esportato e viene visualizzata la finestra di dialogo <b>Esporta report</b> con l&#39;elenco dei messaggi registrati durante il processo di esportazione.

L&#39;archivio del modulo esportato conterrà il modulo MDL contenente le definizioni di *tutti* i materiali MDL definiti da un [grafico MDL](../../mdl-graphs/mdl-graphs.md) nel pacchetto. Se un [grafico a Substance](../../compositing-graphs/substance-compositing-graphs.md) è [istantaneo in un grafico MDL](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md) e connesso a un flusso che va al nodo [principale](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md), le texture generate vengono *salvate nell&#39;archivio*.

Oltre a questi elementi, l&#39;archivio include un file <b>MANIFEST</b> che descrive i metadati seguenti per l&#39;archivio del modulo MDL:

* `mdl`: versione di MDL utilizzata per esportare l&#39;archivio del modulo, ad esempio &quot;1.5&quot;
* `version`: versione dell&#39;archivio del modulo, ad esempio &quot;1.0.0&quot;
* `module`: nome dell&#39;archivio del modulo, ad esempio &quot;::pbr\_metallic\_roughness\_basic&quot;
* `exports.material`: il nome dei materiali definiti nell&#39;archivio del modulo, ad esempio &quot;::pbr\_metallic\_roughness\_basic::MDL\_graph&quot;

>[!NOTE]
>
> Ulteriori informazioni sul formato di file di archivio MDL nell&#39;appendice C della [specifica MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) di NVIDIA.

![Percorso di esportazione MDR](../../assets/mdl-export-archive.png "Percorso di esportazione MDR")

*I percorsi &quot;Esporta archivio moduli MDL&quot; in Esplora risorse e la finestra di dialogo Esporta report risultante*

## Modulo incapsulato MDL (\*.mdle)

I grafici MDL con parametri esposti possono essere esportati come materiali MDL incapsulati. L&#39;incapsulamento *esegue il wrapping dei dati* in una classe dedicata in modo che non sia possibile accedere direttamente ai dati **.

Ad esempio, sebbene sia ancora possibile modificare i valori dei parametri esposti per controllare il comportamento di un materiale, la *definizione* di questi parametri è *non disponibile* in un modulo MDL incapsulato.

L&#39;esportazione di un modulo MDL incapsulato viene eseguita in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md) a livello di grafico MDL, selezionando l&#39;opzione <b>Esporta come .mdle</b> nel menu di scelta rapida di un grafico MDL. Selezionare un percorso e un nome di destinazione per il modulo incapsulato MDL esportato e viene visualizzata la finestra di dialogo <b>Esporta report</b> con l&#39;elenco dei messaggi registrati durante il processo di esportazione.

*Solo* la definizione del materiale per il *grafico MDL selezionato* verrà inclusa nel modulo MDL incapsulato esportato.

>[!NOTE]
>
> Per ulteriori informazioni sulle definizioni dei materiali incapsulati, consulta la sezione 13.5 della [specifica MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) di NVIDIA e la [API MDL SDK](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html).

![Percorso di esportazione MDLE](../../assets/mdl-export-encapsulated.png "Percorso di esportazione MDLE")

*Percorso &quot;Esporta come mdle&quot; in Esplora risorse e finestra di dialogo del report di esportazione*
