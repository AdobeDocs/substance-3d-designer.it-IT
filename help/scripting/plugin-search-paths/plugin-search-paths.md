---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Configura i percorsi di ricerca dei plug-in in Substance 3D Designer per specificare dove si trovano i plug-in Python.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Percorsi di ricerca plug-in
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Percorsi di ricerca plug-in

Designer cercherà i plug-in in directory specifiche (ad esempio, i percorsi di ricerca). Questa pagina spiega come configurare questi percorsi.

Gli utenti possono *aggiungere directory personalizzate* manualmente nelle preferenze del software o specificarle utilizzando variabili di ambiente.

## Aggiunta manuale di percorsi di ricerca dei plug-in

1. Vai a <b>Modifica > Preferenze...</b>
1. Selezionare la categoria <b>Progetti</b>
1. Selezionare il <b>file di progetto</b> che si desidera modificare
1. Nella scheda <b>Python</b>, fai clic sul pulsante *<b>+</b>*per aggiungere la directory che contiene i plug-in
1. Fai clic su <b>OK</b> per convalidare

![Impostazioni dei percorsi di ricerca dei plug-in Python Impostazioni del progetto](../../assets/image-70.png "Impostazioni dei percorsi di ricerca dei plug-in Python Impostazioni del progetto")

## Utilizzo delle variabili di ambiente

L&#39;applicazione cercherà i plug-in in tutti i percorsi specificati utilizzando la variabile di ambiente <b>SBS\_DESIGNER\_PYTHON\_PATH </b>.
