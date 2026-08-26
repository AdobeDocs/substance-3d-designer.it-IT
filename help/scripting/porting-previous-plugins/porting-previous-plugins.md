---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: Scopri come trasferire i plug-in dalle versioni precedenti di Substance Designer all'API Python corrente.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Portare i plug-in precedenti
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Portare i plug-in precedenti

A causa delle modifiche apportate al supporto di Qt per Python, **i plug-in precedenti non funzioneranno più**.\
In particolare, si prega di notare quanto segue:

## Caricamento e scaricamento del plug-in

I plug-in vengono ora caricati all&#39;avvio <b>dell&#39;applicazione</b> e vengono scaricati quando <b>esce</b>.\
Di conseguenza, non è più *necessario* che i plug-in ereditino da &#39;*sdplugins.Plugin*&#39;.

Per ulteriori informazioni, consulta la sezione [Nozioni di base sui plug-in](../../scripting/plugin-basics/plugin-basics.md).

## Creazione di elementi dell&#39;interfaccia utente

I plug-in *non necessitano di* per definire un elemento &#39;*sdplugins.PluginDesc*&#39;.\
I plug-in possono invece utilizzare il <b>nuovo oggetto [Gestione interfaccia utente](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> e <b>Qt per Python</b> per creare gli elementi dell&#39;interfaccia utente necessari.

È possibile trovare piccoli esempi di codice nella sezione [Creazione di elementi dell&#39;interfaccia utente](../../scripting/creating-user-interface/creating-user-interface-elements.md).

## Sostituzione degli usi del contesto di posizione

La classe &#39;*SDLocationContext*&#39; è stata *rimossa* dall&#39;API Python.\
I plug-in possono utilizzare l&#39;oggetto <b>[Gestione interfaccia utente](../scripting-api-reference/scripting-api-reference.md#ui-manager-sduimgr)</b> per accedere al grafico e alla selezione attualmente attivi.

Alcuni esempi sono disponibili nella sezione [Accesso a grafici e selezioni](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md).
