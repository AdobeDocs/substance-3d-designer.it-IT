---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Risoluzione dei problemi di arresto anomalo durante il rendering dei grafici in Substance 3D Designer e individuazione di soluzioni per evitarli.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arresto anomalo durante il rendering dei grafici
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Arresto anomalo durante il rendering dei grafici

In questa pagina sono elencati gli arresti anomali che si verificano durante il processo di rendering del grafico in Substance 3D Designer e per ciascuno di essi sono disponibili i passaggi per la risoluzione dei problemi.

## TDR (solo Windows)

<b>[![(errore)](../../assets/error.svg)](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Problema</b>

Il timer di <b>Rilevamento e ripristino timeout</b> del sistema è *troppo breve* per consentire a Substance 3D Designer di completare i calcoli correnti prima del *riavvio del driver di grafica*.

I calcoli eseguiti da Substance 3D Designer possono richiedere molto tempo e utilizzare i driver grafici in misura tale che *non risponda* al sistema operativo per un certo periodo.\
Come misura di stabilità e sicurezza, il sistema operativo *riavvia il driver di grafica*, riducendo la lunghezza dei calcoli e causando l&#39;*arresto anomalo* di Substance 3D Designer.

<b>![(tick)](../../assets/check.svg) Passaggi consigliati</b>

Per evitare tali arresti anomali, i valori del timer TDR devono essere *aumentati*. Per farlo, segui le istruzioni riportate in [questa pagina](https://experienceleague.adobe.com/it/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) della documentazione di Substance 3D Painter, valide anche per Substance 3D Designer.
