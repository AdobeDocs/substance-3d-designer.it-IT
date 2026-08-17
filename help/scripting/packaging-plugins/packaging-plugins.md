---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Scopri come creare pacchetti di plug-in Python per Substance 3D Designer per la distribuzione e l'installazione.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Creazione di pacchetti di plug-in
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# Creazione di pacchetti di plug-in

## Contenuto del pacchetto del plug-in

I pacchetti sono un singolo file, internamente un archivio zip, contenente un file **pluginInfo.json** con metadati sul plug-in.

il codice del plug-in e tutti gli altri file o risorse necessari al funzionamento del plug-in.

**Voci PluginInfo.json:**

| Ingresso | Descrizione | Valore predefinito | Note |
| --- | --- | --- | --- |
| metadata\_format\_version | Formato del file di metadati. | 1 | Obbligatorio.Attualmente deve essere impostato su 1. |
| nome | Il nome del plug-in. |  | Obbligatorio.Deve corrispondere al nome del modulo Python contenente il codice del plug-in |
| versione | La versione del plug-in. |  | Facoltativo. |
| autore | Autore del plug-in. |  | Facoltativo. |
| email | E-mail dell’autore del plug-in. |  | Facoltativo. |
| min\_designer\_version | Versione minima dell&#39;applicazione richiesta dal plug-in per funzionare. | 2019.2 | Facoltativo. |
| piattaforma | Piattaforma su cui viene eseguito il plug-in. | qualsiasi | Facoltativo.Per i plug-in contenenti codice compilato, questa voce può essere utilizzata per disabilitare il plug-in in piattaforme non supportate.Valori possibili: win, linux, osx, any. |

## Creazione di un nuovo progetto di pacchetto di plug-in

Forniamo un progetto modello [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/) per semplificare la creazione di progetti pacchetto di plug-in.

Potete usarlo direttamente o modificarlo per le vostre esigenze.

Il modello si trova nella directory dell&#39;applicazione, in <b>plugin/tools/pkgplugintemplate</b>.

1. <b>Installare Python, se non è già installato nel sistema</b>

   Cookiecutter è compatibile sia con Python 2 che Python 3
1. <b>Installa Cookecutter se non ne sei già provvisto</b>

   Di solito questo può essere fatto usando pip:

   ```
   pip install cookiecutter
   ```


   Per ulteriori informazioni sui metodi alternativi di installazione di Cookiecutter o per ulteriori informazioni su Cookiecutter, consultare la documentazione all&#39;indirizzo <https://cookiecutter.readthedocs.io/en/latest/installation.html>
1. <b>Crea un nuovo progetto di pacchetto di plug-in</b>

   In un&#39;esecuzione della finestra del terminale:

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   Compilate le informazioni richieste. Il nuovo progetto verrà creato nella directory specificata.
1. <b>Creare un pacchetto del plug-in una volta completato lo sviluppo</b>

   In un&#39;esecuzione della finestra del terminale:

   ```
   python makepackage.py
   ```

1. Il pacchetto del plug-in verrà generato nella directory di compilazione
