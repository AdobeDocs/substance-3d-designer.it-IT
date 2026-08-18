---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Scoprite come implementare la funzionalità di annullamento e ripetizione negli script Substance 3D Designer Python per le azioni degli utenti.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Annulla e ripeti
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# Annulla e ripeti

Con la classe <b>SDHistoryUtils.UndoGroup</b>, gli utenti possono *raggruppare le azioni* per *annullarle o ripristinarle* in un unico comando.

Questi gruppi sono *denominati* dagli utenti e verranno visualizzati con tale nome nell&#39;elenco Annulla/Ripeti dell&#39;interfaccia utente.  Questo rende più gestibile un gran numero di azioni.

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
