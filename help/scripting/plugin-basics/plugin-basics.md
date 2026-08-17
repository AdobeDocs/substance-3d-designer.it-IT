---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Scopri le nozioni di base sulla creazione di plug-in Python per Substance 3D Designer per estendere le funzionalità delle applicazioni.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nozioni di base sui plug-in
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# Nozioni di base sui plug-in

Un plug-in è un file Python o un modulo Python che definisce una funzione <b>initializeSDPlugin()</b>.

La funzione <b>initializeSDPlugin()</b> viene chiamata quando il plug-in viene caricato.\
In questa funzione è possibile creare elementi dell&#39;interfaccia utente, registrare i callback e qualsiasi altra funzionalità necessaria.

Facoltativamente, il plug-in può definire una funzione <b>uninitializeSDPlugin()</b> che verrà chiamata quando il plug-in viene scaricato.\
È possibile utilizzare questa funzione per liberare risorse, chiudere connessioni di rete e altre funzionalità simili.

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
