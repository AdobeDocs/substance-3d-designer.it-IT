---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Scoprite come accedere e manipolare grafici e selezioni di nodi negli script Substance 3D Designer Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Accesso a grafici e selezioni
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Accesso a grafici e selezioni

La classe <b>SDApplication</b> contiene alcuni metodi utili che consentono di accedere al grafico *attivo* e alla *selezione corrente* al suo interno.

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


È possibile accedere a un grafico visualizzato in una visualizzazione grafico *specifica* utilizzando un <b>graphViewID</b>.

Questo metodo è utile quando si creano barre degli strumenti personalizzate per la visualizzazione dei grafici. Nell&#39;esempio <b>Creazione di barre degli strumenti nelle visualizzazioni del grafico</b> del capitolo [Creazione di elementi dell&#39;interfaccia utente](../../scripting/creating-user-interface/creating-user-interface-elements.md) sono disponibili ulteriori dettagli.
