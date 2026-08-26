---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Risolvi i problemi con la creazione o il caricamento dei progetti in Substance 3D Designer e trova soluzioni.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Impossibile creare un progetto
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# Impossibile creare/caricare un progetto

In questa pagina sono elencate le cause più comuni di mancata creazione o caricamento dei progetti in Substance 3D Designer e sono disponibili passaggi per la risoluzione dei problemi per ciascuno di essi.

## Applicazione troppo vecchia per aprire l&#39;URL

**![(errore)](../../assets/error.svg) Problema**

Il **file Substance 3D (SBS)** è caricato da una versione di Substance 3D Designer che *non supporta il formato*. Il file Substance 3D è stato probabilmente *salvato in una versione più recente* del software che utilizza un formato aggiornato per questi file.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Con l&#39;evoluzione di Substance 3D Designer, si evolve anche il formato di file Substance 3D (SBS). Nella maggior parte dei casi, una nuova versione del software dovrà *aggiornare i file* in modo che possano supportare le funzionalità più recenti.

Ti viene *richiesto* di eseguire questo aggiornamento quando *carichi il file per la prima volta* in una nuova versione.

>[!WARNING]
>
> Se il file viene salvato *dopo* l&#39;applicazione dell&#39;aggiornamento, viene modificata anche la versione del formato. A questo punto, *non può più essere caricato nelle versioni precedenti* di Substance 3D Designer.
> 
> Questa limitazione si applica anche alla [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

Innanzitutto, controlla di utilizzare la versione più recente di Substance 3D Designer consentita dalla tua licenza corrente. Di seguito sono riportati i punti di accesso agli aggiornamenti per ogni edizione:

* <b>Abbonamento ad Substance 3D:</b> vai alla sezione Aggiornamenti della scheda App nell’applicazione [Adobe Creative Cloud Desktop](https://creativecloud.adobe.com/en/apps/download/creative-cloud)
* Abbonamento a <b>[Substance3d.com](http://Substance3d.com):</b> aggiornamento quando richiesto in Substance 3D Designer o download del programma di installazione più recente nella sezione [Licenze personali](https://store.substance3d.com/user) del sito Web [Substance3d.com](http://substance3d.com)
* <b>Steam:</b> l&#39;applicazione verrà aggiornata automaticamente per impostazione predefinita. Puoi attivare manualmente l&#39;aggiornamento avviando Substance 3D Designer o accedendo alla schermata Download

>[!WARNING]
>
> Assicurati di non dover caricare i file in una versione precedente di Substance 3D Designer *prima di salvare* un file che è stato aggiornato.
> 
> In alternativa, puoi *creare una copia* del file *prima* di caricarlo in una nuova versione di Substance 3D Designer, in modo da avere sempre un file a cui tornare se devi utilizzare una versione precedente del software.

## Arresto anomalo durante la creazione o il caricamento di un progetto

<b>![(errore)](../../assets/error.svg) Problema</b>

Un arresto anomalo durante la creazione o il caricamento di un progetto è spesso causato da un errore durante l&#39;inizializzazione della [vista 3D](../../interface/3d-view/3d-view.md), che si verifica quando viene impostata l&#39;area di lavoro.

Se il sistema è un laptop, un&#39;applicazione di terze parti potrebbe applicare un *piano di risparmio energia* che impedisce alla vista 3D di utilizzare la GPU del sistema. Questo può causare un arresto anomalo se nessun altro dispositivo GPU può eseguire l&#39;operazione al suo posto.

Può verificarsi un arresto anomalo anche quando la configurazione o il ridimensionamento della visualizzazione *sono stati modificati* tra una sessione e l’altra, per cui il fotogramma di rendering della vista 3D viene creato con coordinate non valide.

<b>![(tick)](../../assets/check.svg) Passaggi consigliati</b>

Considerando le molteplici cause possibili di questo arresto anomalo, consigliamo di eseguire i seguenti passaggi per la risoluzione dei problemi:

Aggiornare i driver grafici

Per prima cosa, assicuratevi che i driver di grafica siano aggiornati. La versione più recente per la GPU è disponibile [qui](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA), [qui](https://www.amd.com/en/support) (AMD) o [qui](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel).

Forza prestazioni migliori

Cercare qualsiasi software che gestisca la *combinazione per il risparmio di energia* del sistema (ad esempio, ASUS Armory Crate), in particolare quando il sistema è un laptop.

Alcune applicazioni di risparmio energia possono limitare l&#39;accesso di altre applicazioni alla GPU del sistema o ostacolare le prestazioni della GPU, con conseguenti arresti anomali. Se esiste e è attiva un&#39;applicazione di risparmio energia, passare al piano che consente prestazioni ottimali.

Forza l’utilizzo della GPU discreta

Se il sistema dispone di *grafica commutabile*, è consigliabile forzare l&#39;uso della GPU discreta (dGPU) per le applicazioni Substance 3D.

Nella maggior parte dei casi, questo si ottiene in un’applicazione dedicata che controlla le impostazioni della GPU. Ad esempio, per le GPU NVIDIA è possibile eseguire questa operazione nell’applicazione &quot;Pannello di controllo NVIDIA&quot;.

Ripristina interfaccia utente salvata nel Registro di sistema

Se l’arresto anomalo è causato da una modifica della configurazione o del ridimensionamento dello schermo, prova a eliminare le voci del registro di sistema esistenti per consentire a Designer di ripristinare completamente l’interfaccia utente, tra le altre impostazioni.

La procedura per eseguire questo ripristino per sistema operativo è descritta di seguito:

+++Windows
* Chiudi Designer

Chiudi Designer

* Apri l&#39;applicazione <b>prompt dei comandi</b>

Apri l&#39;applicazione <b>prompt dei comandi</b>

* Immetti il comando seguente e premi <b>Invio</b>:

  <b>Creative Cloud desktop</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>Edizione Steam/Substance</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


Immetti il comando seguente e premi <b>Invio</b>:

<b>Creative Cloud desktop</b>

<b>Edizione Steam/Substance</b>

* Scollega il secondo monitor dal sistema e ricollegalo (ignora questo passaggio se *non* ha più schermi collegati)

Scollega il secondo monitor dal sistema e ricollegalo (ignora questo passaggio se *non* ha più schermi collegati)

* Avvia Designer, ma *non* crea o apre alcun progetto

Avvia Designer, ma *non* crea o apre alcun progetto

* Nella barra superiore, apri il menu <b>Windows</b> e seleziona l&#39;opzione <b>Nuova vista 3D</b>

Nella barra superiore, apri il menu <b>Windows</b> e seleziona l&#39;opzione <b>Nuova vista 3D</b>

* Verifica che la <b>vista 3D</b> sia inizializzata correttamente e prova diverse trame di anteprima nel menu <b>Scena</b> della barra superiore del pannello

Verifica che la <b>vista 3D</b> sia inizializzata correttamente e prova diverse trame di anteprima nel menu <b>Scena</b> della barra superiore del pannello

* Creare o aprire un materiale

Creare o aprire un materiale

+++

+++macOS
* Chiudi Designer

Chiudi Designer

* Apri l&#39;applicazione <b>Terminale</b>

Apri l&#39;applicazione <b>Terminale</b>

* Immetti il comando seguente e premi <b>Invio</b>:

  <b>Creative Cloud desktop</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>Edizione Steam/Substance</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


Immetti il comando seguente e premi <b>Invio</b>:

<b>Creative Cloud desktop</b>

<b>Edizione Steam/Substance</b>

* Scollega il secondo monitor dal sistema e ricollegalo (ignora questo passaggio se *non* ha più schermi collegati)

Scollega il secondo monitor dal sistema e ricollegalo (ignora questo passaggio se *non* ha più schermi collegati)

* Avvia Designer, ma *non* crea o apre alcun progetto

Avvia Designer, ma *non* crea o apre alcun progetto

* Nella barra superiore, apri il menu <b>Windows</b> e seleziona l&#39;opzione <b>Nuova vista 3D</b>

Nella barra superiore, apri il menu <b>Windows</b> e seleziona l&#39;opzione <b>Nuova vista 3D</b>

* Verifica che la <b>vista 3D</b> sia inizializzata correttamente e prova diverse trame di anteprima nel menu <b>Scena</b> della barra superiore del pannello

Verifica che la <b>vista 3D</b> sia inizializzata correttamente e prova diverse trame di anteprima nel menu <b>Scena</b> della barra superiore del pannello

* Creare o aprire un materiale

Creare o aprire un materiale

+++
