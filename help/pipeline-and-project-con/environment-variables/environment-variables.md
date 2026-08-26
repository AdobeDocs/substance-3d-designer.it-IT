---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Scoprite come utilizzare le variabili di ambiente in Substance 3D Designer per configurare i percorsi e le impostazioni di sistema.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variabili di ambiente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# Variabili di ambiente

Questa pagina elenca le variabili di ambiente che possono essere utilizzate per ignorare il comportamento predefinito dell&#39;applicazione.

| Variabile | Descrizione |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Percorso da cui Designer caricerà [Plug-in Python](../../scripting/plugin-basics/plugin-basics.md). |
| **SUBSTANCE\_DESIGNER\_LICENSE** | Percorso del file di licenza (*license.key*) che deve essere utilizzato da Designer.   Ignora il percorso impostato nell&#39;[Attivazione guidata](../../getting-started/activation-and-licenses/activation-and-licenses.md) di Designer.  **Nota:** nelle versioni precedenti potrebbe essere necessario utilizzare un nome di variabile alternativo:<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_LICENSE</strong></li></ul> |
| <b>OCIO</b> | Percorso del file di configurazione OCIO da utilizzare quando si utilizza la [gestione colore](../../color-management/color-management.md) di OpenColorIO.   Sostituisce il percorso impostato nelle impostazioni di gestione del colore di Designer in [Impostazioni progetto](../../interface/preferences-window/project-settings/project-settings.md). |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | Il ritardo in secondi prima del rilascio di un sedile con licenza in caso di configurazione multiutente Il valore predefinito è 7200 secondi (2 ore). |
