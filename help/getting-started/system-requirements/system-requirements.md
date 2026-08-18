---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Esaminare i requisiti di sistema di Substance 3D Designer per verificare che il computer soddisfi le specifiche necessarie.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Requisiti di sistema
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Sistemi supportati

Di seguito è riportato un elenco di hardware e sistemi supportati dall&#39;applicazione:

## Windows

|  | Minimo | Consigliato | Ottimale |
| --- | --- | --- | --- |
| <b>SO</b> | Windows 11 64 bit versione 23H2 | Windows 11 64 bit versione 24H1 | Windows 11 64 bit versione 24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Archiviazione</b> | SSD con 30 GB di spazio disponibile | SSD con 50 GB di spazio disponibile | SSD con 70 GB di spazio disponibile |

### macos

|  | Minimo | Consigliato | Ottimale |
| --- | --- | --- | --- |
| <b>SO</b> | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>Archiviazione</b> | SSD con 30 GB di spazio disponibile | SSD con 50 GB di spazio disponibile | SSD con 70 GB di spazio disponibile |

### Linux

| Enterprise | Vapore |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22,04 |

## Raccomandazioni generali

* Per lavorare in condizioni ottimali, consigliamo un monitor con una risoluzione superiore a 1 Mega Pixel e una larghezza superiore a 1280 pixel.
* Molte app Substance dipendono da OpenSSL 1.1.1 per la compatibilità con RHEL8/9. Per i sistemi con versioni OpenSSL più recenti, dovrai fornirlo manualmente.
* *Solo* versioni <b>2019.x</b> e successive sono state autenticate per l&#39;esecuzione su <b>MacOS 10.15</b> (Catalina).
* La connessione <b>Desktop remoto</b> è possibile se è disponibile un contesto OpenGL 3.3. Funzionerà su <b>Nvidia Quadro</b> ma *non* su Nvidia GeForce perché fornisce solo un contesto OpenGL 1.4. Se si tratta di un problema, si consiglia di utilizzare soluzioni alternative come <b>VNC</b>/<b>Teamviewer</b>.
* Gli utenti della versione <b>Steam</b> devono *disabilitare* la <b>Sovrapposizione vapore</b> per Designer, poiché potrebbe causare problemi di prestazioni quando è attiva.

## GPU supportate

Di seguito è riportato un elenco della GPU compatibile con l&#39;applicazione:

* NVIDIA GeForce GTX 1060 e versioni successive
* NVIDIA Quadro P2200 e versioni successive
* AMD Radeon RX 580 e versioni successive
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR (solo Windows)**
> 
> Per una migliore stabilità complessiva durante l’esecuzione di calcoli complessi sulla GPU, ad esempio il rendering di grafici complessi, il rendering nella vista 3D, l’esportazione di una scena dalla vista 3D e così via, si consiglia vivamente di assicurarsi che i valori di <b>Rilevamento e ripristino del timeout</b> corrispondano ai consigli riportati in [questa pagina](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) della documentazione.

## Configurazione non supportata

<b>Windows</b>

* La macchina virtuale non è supportata.
* Windows Server non è supportato.

<b>macOS</b>

* I sistemi macOS basati su Intel non sono supportati.
* Sono supportate solo le configurazioni Apple ufficiali.
* Le eGPU non sono attualmente supportate e potrebbero presentare problemi di stabilità.

<b>Linux</b>

* I driver Mesa su Linux non sono supportati.

<b>Qualsiasi piattaforma</b>

* Le GPU integrate non sono supportate su CPU x86-64 (Intel, AMD).
* L’utilizzo di Designer in combinazione con software di terze parti che intercetta le chiamate Designer ai driver grafici non è supportato. Tali software includono:
  * Iniettori di post-elaborazione come tamponi che applicano Color Grading, effetti fotocamera, ...
  * Sovrapposizioni su schermo come mirini personalizzati, metriche delle prestazioni GPU, interfacce per lo streaming video...

## Versioni minime del driver GPU

Di seguito è riportato un elenco delle versioni minime dei driver della GPU necessarie per l&#39;esecuzione dell&#39;applicazione senza problemi. Questo elenco è soggetto a modifiche come nuove versioni.

Per scaricare nuovi driver, vedere: [La GPU contiene driver obsoleti](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SO | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>Windows</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro/FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Non supportato |

>[!NOTE]
>
> In **Mac OS** il driver della GPU è fornito dal sistema operativo stesso. Esegui l’aggiornamento alla versione più recente del sistema operativo per accedere al driver più recente.

## Raytracing GPU per la cottura al forno

Per attivare Raytracing GPU tramite Optix o DXR, è necessario installare i driver sopra consigliati.

<b>DXR</b> richiede la seguente configurazione minima:

* <b>Windows 10</b> versione 1809; per ulteriori informazioni, vedere [questa pagina](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/features/gpu-raytracing)
* <b>GPU con architettura Pascal</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> Raytracing GPU funziona in modo ottimale su hardware dedicato per il ray tracing, ad esempio le GPU NVIDIA GeForce RTX o NVIDIA Quadro RTX.

## Uso delle compresse

Gli utenti della tavoletta su <b>Windows</b> devono applicare le impostazioni descritte nella pagina seguente per ottenere l&#39;esperienza più affidabile: [Configurazione di penne e tablet](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

## Lingue

L&#39;interfaccia software è disponibile nelle seguenti lingue:

* Deutsch (Germania)
* Inglese (Stati Uniti)
* Español (Spagna)
* Français (Francia)
* Italiano (Italia)
* Português (Brasil)
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)
