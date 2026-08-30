---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: Risoluzione dei problemi di scripting Python in Substance 3D Designer, inclusi problemi relativi a plug-in e API.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemi con Python
user-guide-description: ''
user-guide-title: ''
source-git-commit: 21af965a075e8c119d16922f15b867da99c21397
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Problemi con Python

In questa pagina sono elencati i problemi tecnici relativi all&#39;[API Python](../../scripting/scripting.md) di Substance 3D Designer e alle funzionalità implementate in Python. Per ciascuno di essi sono disponibili procedure di risoluzione dei problemi.

Le funzionalità implementate in Python includono le azioni [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Invia a](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) nella barra degli strumenti di [Explorer](../../interface/the-explorer-window/the-explorer-window.md), nonché lo strumento per rimuovere i nodi inutilizzati nei grafici.

## Impossibile caricare il modulo &#39;QtForPython&#39;

<b>![(errore)](python-issues.resources/error.svg) Problema</b>

Il modulo Python &#39;QtForPython&#39; non viene caricato e ciò causa la mancanza di funzionalità implementate in Python, ad esempio le azioni [Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[Invia a](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) nella barra degli strumenti di [Explorer](../../interface/the-explorer-window/the-explorer-window.md) e lo strumento per rimuovere i nodi inutilizzati nei grafici.

Inoltre, molti [plug-in Python](../../scripting/plugin-basics/plugin-basics.md) non verranno caricati o non funzioneranno come previsto.

<b>![(tick)](python-issues.resources/check.svg) Passaggi consigliati</b>

È probabile che vi sia un conflitto tra l&#39;installazione di QtForPython da parte di Designer e le relative dipendenze e un&#39;installazione esistente sul sistema.

Rimuovi qualsiasi altra installazione di sistema di [QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/)) e [Shiboken2](https://pypi.org/project/shiboken2/).

In alternativa, invece di un&#39;installazione a livello di sistema di QtForPython, puoi prendere in considerazione l&#39;utilizzo di Python *ambienti virtuali* o di un *gestore pacchetti* come [rez](https://github.com/AcademySoftwareFoundation/rez).
