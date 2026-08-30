---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Scopri come utilizzare i file di configurazione del progetto SBSPRJ in Substance 3D Designer per gestire le impostazioni del progetto.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: File di configurazione del progetto - SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Panoramica

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>I file di configurazione del progetto</b> sono i file più complessi ed estesi utilizzati per configurare Substance 3D Designer.

Sono speciali in quanto consentono di utilizzare più file di configurazione del progetto, in cui ogni successivo progetto &quot;secondario&quot; espande o sostituisce il precedente progetto &quot;principale&quot;. A meno che non sia esplicitamente necessario, le impostazioni non devono essere modificate o aggiunte ai file di progetto, in modo che Designer possa ripristinare la configurazione principale o persino le impostazioni predefinite.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Icona file SBSPRJ](project-configuration-files-sbsprj.resources/sbsprj.png "Icona file SBSPRJ")

</td>
</tr>
</table>

Per impostazione predefinita, Designer dispone di due configurazioni di progetto attive:

<b>Progetto predefinito: </b>Contiene tutte le impostazioni predefinite e la libreria Designer viene fornita con una nuova installazione.*Sola lettura, impossibile modificare o rimuovere.*

<b>Progetto utente: </b>Poiché i valori predefiniti sono di sola lettura, *le modifiche apportate dall&#39;utente* verranno inserite in questo progetto per impostazione predefinita. *Impossibile rimuovere.*

Questa configurazione di base garantisce che la libreria predefinita e le altre impostazioni non possano essere danneggiate o modificate, ma consente comunque a singoli utenti amatoriali di aggiungere le proprie modifiche senza doversi preoccupare di impostazioni complesse.

## Espandi o sostituisci

La maggior parte delle impostazioni in un progetto consecutivo <b>sovrascriverà</b> quelle del progetto precedente. Ad esempio, un plug-in diverso dello spazio tangente in un file di progetto personalizzato sostituirà qualsiasi plug-in di Servizi terminal definito nel progetto Predefinito o Utente. Ciò significa che, a meno che non sia esplicitamente necessario, si consiglia di non sovrascrivere o modificare le impostazioni nei progetti secondari.

Tuttavia, alcune impostazioni <b>espandono</b> in base alle impostazioni principali, anziché sostituirle. In particolare, queste impostazioni sono rappresentate dai percorsi e dai filtri della libreria, quindi è sempre possibile aggiungere più contenuto alla libreria invece di sovrascriverlo. Inoltre, sono presenti gli alias (parole chiave del percorso per i relativi percorsi di file) che si espandono, nonché l&#39;override se viene definito un duplicato. Questo consente un grande controllo sui percorsi dei file di contenuto e sui riferimenti.

## Contenuto del file di progetto

I file di progetto possono contenere le seguenti impostazioni:

<b>vista 3D: </b>Definizioni di Shader predefinito, HDR e stato della scena.

<b>Alias: </b>Alias parole chiave per percorsi relativi.

<b>Cottura: </b>Impostazioni per le convenzioni di denominazione della cottura al forno.

<b>Generali: </b>Modelli di grafico, plug-in per lo spazio tangente, impostazioni predefinite per formato immagine e normale.

<b>Libreria: </b>Percorsi controllati da visualizzare nella libreria.

<b>Scripting: </b>Script e interpreti di richiamata.

<b>Controllo versione: </b>Impostazioni per l&#39;integrazione del controllo versione in Designer.

## Modifica dei file di progetto

Come tutti gli altri tipi, le configurazioni di progetto vengono salvate come file XML strutturati (con estensione <b>.sbsprj</b>) che possono essere modificati tramite l&#39;interfaccia utente di Designer o un editor di testo esterno.

## All&#39;interno di Substance 3D Designer

Per ulteriori informazioni sulla gestione dei file di progetto e sulla modifica delle impostazioni del progetto, vedere la pagina [Impostazioni progetto](../../interface/preferences-window/project-settings/project-settings.md).

I file di progetto includono anche <b>categorie</b> e <b>filtri</b> personalizzati per la [libreria](../../interface/the-library/the-library.md). Ulteriori informazioni sono disponibili nella pagina [Gestione di contenuti e filtri personalizzati](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md).

## Modifica XML esternamente

Per Windows, [Blocco note++](https://notepad-plus-plus.org) è una buona opzione gratuita. In macOS, [Sublime Text](https://www.sublimetext.com/) è un&#39;alternativa. Detto questo, qualsiasi editor con un rientro appropriato, la compressione della sezione e una qualche forma di evidenziazione della sintassi renderà la tua vita molto più facile.

Una volta aperto il file SBSPRJ in un editor, dovresti vedere un layout strutturato abbastanza semplice, con sezioni corrispondenti alle schede nell&#39;interfaccia utente. Non tutte le impostazioni saranno documentate qui, poiché è abbastanza autoesplicativo.

![Modifica XML](project-configuration-files-sbsprj.resources/project-xml.png "Modifica XML")

## Percorsi e alias relativi

I percorsi relativi combinati con gli alias sono una delle parti più complicate, ma più importanti, di una configurazione di progetto. In questa sezione verranno illustrati i dettagli. L&#39;aggiunta di alias personalizzati per un file di progetto specifico viene eseguita nelle [Impostazioni progetto](../../interface/preferences-window/project-settings/project-settings.md).

Uno dei principali problemi con i file che fanno riferimento ad altri file in un sistema su più PC dell&#39;utente, è che i percorsi di file assoluti non funzioneranno. Gli utenti possono definire i propri repository SVN in posizioni completamente diverse (ad es. C:/John/Gamedev/SubstanceLibrary o D:/Dev/SubstanceLibrary). Gli alias e i percorsi relativi funzionano insieme per risolvere il problema. In caso contrario, è possibile che si apra il file di un altro utente, che proverà a cercare il nodo personalizzato utilizzato nel percorso specifico in cui l&#39;utente lo aveva localmente, che probabilmente non sarà stato definito esattamente nello stesso modo.

Un <b>alias</b> è una parola chiave che sostituisce (parte di) un percorso. È simile a una variabile di ambiente Windows come %TEMP%, in cui una singola parola sostituisce un percorso spesso utilizzato che viene quindi definito centralmente. Il vantaggio è costituito da tracciati semplificati ovunque e da un modo per modificare tutti i riferimenti in una volta sola quando si decide di riposizionare il tracciato.

>[!NOTE]
>
> **Esempio di alias**
> 
> | Alias | Valore percorso effettivo |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>personalizzato</b> | *D:\Dev\CustomProject\Substance* |
> 
> Per impostazione predefinita, la libreria predefinita si trova in *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* e tutti i grafici che utilizzano il contenuto predefinito fanno riferimento a questa directory. Anziché fare riferimento al percorso completo, è definito un alias di &#39;<b>SBS</b>&#39; (senza virgolette). Nel caso di una libreria predefinita, il valore esatto del percorso SBS viene impostato al momento dell&#39;installazione sulla directory scelta dall&#39;utente per Designer.
> 
> Internamente, un riferimento viene modificato nel modo seguente, quando contiene un percorso con un alias:
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>I percorsi relativi</b> sono sempre relativi al file in cui sono definiti. Ciò significa che la posizione corrente del file di configurazione determina la maggior parte del percorso e i percorsi degli alias saranno basati su di esso, principalmente aggiungendo solo una sottocartella. <b>Si consiglia vivamente di posizionare i file sbsprj accanto alle cartelle che si desidera guardare.</b>

Considerare ad esempio un repository in *C:/Versioncontrol/Substance/* contenente *CustomProject.sbsprj* e quindi due cartelle, */Base* e */Tools,* contenenti nodi.

Per definire due alias relativi per Base e Strumenti, si procede come segue all&#39;interno del file SBSPRJ:

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


Il risultato di questo file di configurazione è il seguente:

**BaseAlias://** sarà *C:/Versioncontrol/Substance/Base/* e **ToolsAlias://** sarà *C:/Versioncontrol/Substance/Tools/.*

Se si desidera definire solo *C:/Versioncontrol/Substance/*, il percorso verrà elencato come **&quot;file:.&quot;**, ovvero il punto che indica la posizione del file stesso.
