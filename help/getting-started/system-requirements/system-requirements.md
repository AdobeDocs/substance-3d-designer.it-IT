---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ""
description: Esaminare i requisiti di sistema di Substance 3D Designer per verificare che il computer soddisfi le specifiche necessarie.
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Requisiti di sistema
user-guide-description: ""
user-guide-title: ""
source-git-commit: aeb517a0def4b5bc2de723633f8932dfc03f052c
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%
---

# Requisiti di sistema

Di seguito è riportato un elenco di hardware e sistemi supportati dall&#39;applicazione:

## Configurazione del sistema per piattaforma

### Windows

|             | Minimo | Consigliato | Ottimale |
|:------------|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| **SO** | Windows 11 64 bit versione 23H2 | Windows 11 64 bit versione 24H1 | Windows 11 64 bit versione 24H2 |
| **CPU** | Intel Core i5<br>AMD Ryzen 5 | Intel Core i7<br>AMD Ryzen 7 | Intel Core i9<br>AMD Ryzen 9 |
| **GPU** | NVIDIA GeForce RTX 2060 Super<br>NVIDIA Quadro RTX 4000<br>AMD Radeon RX 5700 XT<br>AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080<br>NVIDIA Quadro RTX A4000<br>AMD Radeon RX 6800 XT<br>AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090<br>NVIDIA Quadro RTX 5000 Ada Generation<br>AMD Radeon RX 7900 XTX<br>AMD Radeon Pro W7800 |
| **VRAM** | 8 GB | 16 GB | 24 GB |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Archiviazione** | SSD con 30 GB di spazio disponibile | SSD con 50 GB di spazio disponibile | SSD con 70 GB di spazio disponibile |

### macOS

|             | Minimo | Consigliato | Ottimale |
|:------------|:----------------------------------|:----------------------------------|:----------------------------------|
| **SO** | macOS 14 Sonoma | macOS 26 Tahoe | macOS 26 Tahoe |
| **CPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **GPU** | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| **RAM** | 16 GB | 32 GB | 64 GB |
| **Archiviazione** | SSD con 30 GB di spazio disponibile | SSD con 50 GB di spazio disponibile | SSD con 70 GB di spazio disponibile |

### Linux

| Enterprise | Vapore |
|:------------------|:-------------|
| RHEL 8</br>RHEL 9 | Ubuntu 22,04 |

## Raccomandazioni generali

* Per lavorare in condizioni ottimali, consigliamo un monitor con una risoluzione superiore a 1 Mega Pixel e una larghezza superiore a 1280 pixel.
* Molte app Substance dipendono da OpenSSL 1.1.1 per la compatibilità con RHEL8/9. Per i sistemi con versioni OpenSSL più recenti, dovrai fornirlo manualmente.
* *Solo* versioni **2019.x** e successive sono state autenticate per l&#39;esecuzione su **macOS 10.15 Catalina**.
* La connessione **Desktop remoto** è possibile se è disponibile un contesto OpenGL 3.3. Funzionerà su **Nvidia Quadro** ma *non* su Nvidia GeForce perché fornisce solo un contesto OpenGL 1.4. In caso di problemi, si consiglia di utilizzare soluzioni alternative come **VNC/Teamviewer**.
* Gli utenti della versione **Steam** devono *disabilitare* la **Sovrapposizione vapore** per Designer, poiché potrebbe causare problemi di prestazioni quando è attiva.

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
> Per una migliore stabilità complessiva durante l’esecuzione di calcoli complessi sulla GPU, ad esempio il rendering di grafici complessi, il rendering nella vista 3D, l’esportazione di una scena dalla vista 3D e così via, si consiglia vivamente di assicurarsi che i valori di **Rilevamento e ripristino del timeout** corrispondano ai consigli riportati in [questa pagina](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) della documentazione.

## Configurazione non supportata

**Windows**

* La macchina virtuale non è supportata.
* Windows Server non è supportato.

**macOS**

* I sistemi macOS basati su Intel non sono supportati.
* Sono supportate solo le configurazioni Apple ufficiali.
* Le eGPU non sono attualmente supportate e potrebbero presentare problemi di stabilità.

**Linux**

* I driver Mesa su Linux non sono supportati.

**Qualsiasi piattaforma**

* Le GPU integrate non sono supportate su CPU x86-64 (Intel, AMD).
* L’utilizzo di Designer in combinazione con software di terze parti che intercetta le chiamate Designer ai driver grafici non è supportato. Tali software includono:
  * Iniettori di post-elaborazione come tinte reshader che applicano Color Grading, effetti fotocamera, ...
  * Sovrapposizioni su schermo come mirini personalizzati, metriche delle prestazioni GPU, interfacce per lo streaming video...

## Versioni minime del driver GPU

Di seguito è riportato un elenco delle versioni minime dei driver della GPU necessarie per l&#39;esecuzione dell&#39;applicazione senza problemi. Questo elenco è soggetto a modifiche come nuove versioni.

Per scaricare nuovi driver, vedere: [La GPU contiene driver obsoleti](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers).

| SO | NVIDIA | AMD | Intel |
|:------------|:-----------------------------|:-----------------------------------------|:------------|
| **Windows** | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro/FirePro 18.Q4 | 15.33 |
| **Linux** | 535.129.03 | Radeon 23.20 Pro 23.Q3 | Non supportato |

>[!NOTE]
>
> In **macOS** il driver della GPU è fornito dal sistema operativo stesso. Esegui l’aggiornamento alla versione più recente del sistema operativo per accedere al driver più recente.

## Raytracing GPU per eseguire i baking

Per attivare il Raytracing GPU tramite Optix o DXR, è necessario installare i driver sopra consigliati.

**DXR** richiede la seguente configurazione minima:

* **Windows 10** versione 1809; per ulteriori informazioni, vedere [questa pagina](https://experienceleague.adobe.com/it/docs/substance-3d/bakers/features/gpu-raytracing)
* **GPU con architettura Pascal** (Nvidia GeForce 10XX)

>[!TIP]
>
> Raytracing GPU funziona in modo ottimale su hardware di raytracing dedicato come le GPU NVIDIA GeForce RTX o NVIDIA Quadro RTX.

## Uso delle compresse

Gli utenti della tavoletta su **Windows** devono applicare le impostazioni descritte nella pagina seguente per ottenere l&#39;esperienza più affidabile: [Configurazione di penne e tablet](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets).

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
