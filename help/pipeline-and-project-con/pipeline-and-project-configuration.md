---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Configura le impostazioni di pipeline e progetto in Substance 3D Designer per ottimizzare il flusso di lavoro e l’output.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Configurazione della pipeline e del progetto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# Configurazione della pipeline e del progetto

Substance 3D Designer dispone di un potente sistema per configurare l&#39;applicazione per l&#39;utilizzo della pipeline. Tramite un sistema avanzato di file gerarchici &quot;**Project**&quot;, l&#39;applicazione può essere configurata istantaneamente in base agli standard di Studio o Progetto, con tutte le configurazioni e il contenuto della libreria sotto controllo versione. L&#39;obiettivo principale del sistema è quello di centralizzare tutte le impostazioni relative alla pipeline, consentendo comunque a più configurazioni di sovrascrivere ed espandersi a vicenda.

>[!WARNING]
>
> Questo sistema non è destinato a singoli utenti con requisiti più semplici, ma piuttosto a *studi con grandi progetti e team* e una maggiore necessità di organizzazione. Per utilizzare appieno questo sistema, si raccomanda un&#39;adeguata pianificazione e preparazione, nonché un certo grado di configurazione automatica.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Gerarchia dei file di configurazione

Designer dispone di 3 livelli o file di configurazione, ciascuno con uno scopo diverso. Per Windows tutti i file si trovano in *~User\AppData\Local\Adobe\Adobe Substance 3D Designer.*

L&#39;immagine mostra la relazione tra i diversi file nell&#39;installazione predefinita di Designer, dopo una nuova installazione.

</td>
<td style="border: 0;" valign="top">

![Gerarchia dei file di configurazione](../assets/filestructureoverview.png "Gerarchia dei file di configurazione")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b> contiene le impostazioni generali del programma, di cui tutte tranne una non sono rilevanti per le pipeline dei progetti. Questo file è univoco e non può essere scambiato, Designer è hardcoded per utilizzare questo file esatto.\
  Contiene un singolo riferimento a un file di configurazione.
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b> può essere scambiato per altri file SBSCFG con nomi diversi, ma è possibile utilizzare un solo file SBSCFG contemporaneamente.\
  Contiene più riferimenti a file di progetto. *Si noti che per la configurazione predefinita questi file non sono definiti in modo esplicito, ma sono hardcoded!*
* I file <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b> contengono impostazioni rilevanti per il progetto/pipeline. È possibile definire più progetti in una gerarchia, sostituendo o espandendo il progetto definito in precedenza.

## Impostazione pipeline di Designer

Ogni tipo di file viene spiegato con maggiori dettagli nelle pagine secondarie di questa pagina, ma la breve panoramica su come definire idealmente una configurazione personalizzata per Designer è la seguente:

1. <b>Identificare e raggruppare le impostazioni da aggiungere ai file di progetto.</b> Questo processo è diverso per ogni studio e richiede una certa quantità di pianificazione.\
   In quasi tutti i casi devono essere definiti almeno 2 progetti: uno per impostazioni globali e a livello di studio (come modelli standard, file di shader, impostazioni di esegue i baking) e uno con contenuti più specifici come il contenuto della libreria. Se sono in esecuzione più progetti contemporaneamente, potrebbe essere necessario creare più configurazioni di progetto per ciascuno (quindi 3 o più progetti in totale).
1. <b>Creare i [file SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) pertinenti e inserirli con i relativi contenuti in controlli versione.</b> Si consiglia vivamente di separare il contenuto della pipeline e della libreria di Designer dal contenuto e dalle risorse effettive del progetto (modelli 3D, texture, codice) creando un *repository separato*.
1. <b>Creare un file [&#x200B; SBSCFG configuration](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) che elenca tutti i file di progetto, inserirlo nel controllo versione</b>. Se disponi di più progetti, puoi creare una configurazione per ogni progetto.
1. <b>Impostare [User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md) di ogni utente in modo che faccia riferimento al relativo file di configurazione.</b>\
   Potete fare in modo che ogni utente esegua questa operazione manualmente oppure potete creare script inserendo linee nel file XML. [Ulteriori informazioni nella pagina pertinente](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md).
