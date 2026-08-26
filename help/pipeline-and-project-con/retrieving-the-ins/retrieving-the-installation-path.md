---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: Scopri come recuperare il percorso di installazione di Substance 3D Designer per scopi di scripting e automazione.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recupero del percorso di installazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 6%

---


# Recupero del percorso di installazione

Questa pagina raggruppa le informazioni sui modi per recuperare il percorso di installazione di [Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) a seconda della versione e della piattaforma.

## Windows

### Creative Cloud desktop

1. Apri <b>editor del Registro di sistema di Windows</b> (regedit)
1. Accedi alla chiave del Registro di sistema: <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\&lt;/b>
1. Apri la sottochiave <b>Adobe Substance 3D Designer.exe</b>
1. Il valore della chiave contiene il percorso del file eseguibile dell&#39;applicazione in cui è installato

>[!NOTE]
>
> Questa chiave del Registro di sistema è disponibile solo dalla versione 11.2.\
> Per le versioni precedenti, il percorso di installazione può essere recuperato dalle associazioni di file in HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExts

### Edizione Substance (autonoma)

1. Apri <b>editor del Registro di sistema di Windows</b> (regedit)
1. Accedi alla chiave del Registro di sistema: <b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>
1. Trova la sottochiave corrispondente all&#39;<b>AppID</b> della versione dell&#39;applicazione (vedi la tabella seguente)
1. Il valore della chiave contiene il percorso di installazione dell&#39;applicazione

| Versione | AppId |
| --- | --- |
| **Versione 5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **Versione 6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **Versione 7.x (2017.x) a 11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **Versione 11.2 (o successiva)** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Edizione Steam

L’applicazione viene installata nella sottocartella steamapps/common/ della cartella di installazione di Steam.

## macOS

In Mac l’applicazione viene installata nei seguenti casi:

| Versione | Percorso |
| --- | --- |
| **11.2 o versione successiva** | **/Applicazioni/Adobe Substance 3D Designer.app** |
| **Precedente** | **/Applicazioni/Substance Designer.app** |

## Linux

Su Linux il pacchetto rpm è installato nel seguente percorso:

| Versione | Percorso |
| --- | --- |
| **11.2 o versione successiva** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **Precedente** | **/opt/Allegorithmic/Substance\_Designer** |
