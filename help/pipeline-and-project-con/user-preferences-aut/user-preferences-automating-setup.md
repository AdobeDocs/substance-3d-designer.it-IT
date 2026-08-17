---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/user-preferences-automating-setup.html"
breadcrumb-title: ''
description: Scopri come automatizzare la configurazione delle preferenze utente in Substance 3D Designer per una configurazione del flusso di lavoro semplificata.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > User Preferences - Automating Setup
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Preferenze utente - Configurazione automatica
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---


# Preferenze utente - Configurazione automatica

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Il file utente\_preferences.xml contiene tutte le impostazioni specifiche dell&#39;utente diverse da quelle definite in una [configurazione del progetto](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Si riferiscono principalmente a specifiche impostazioni dell&#39;interfaccia utente e delle prestazioni.

L&#39;unica impostazione pertinente da modificare è il [file di configurazione](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) che contiene un elenco di progetti. Questo può essere fatto in alcuni modi, come elencato di seguito.

In alternativa, potete ignorare completamente la modifica delle preferenze utente ed eseguire una sostituzione basata su sessione del file SBSCFG utilizzando un argomento della riga di comando sul collegamento a Designer, vedere di seguito.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Icona file XML](../../assets/xml-5.png "Icona file XML")

</td>
</tr>
</table>

## Permanente o basato su sessioni

Esistono due modi diversi per configurare Designer per l&#39;utilizzo di un altro [file di configurazione](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md) rispetto all&#39;impostazione predefinita, entrambi con vantaggi e svantaggi:

* <b>Modifica permanente di user\_preferences.xml\
  </b>Il file si trova in *~User\AppData\Local\Adobe\Adobe Substance 3D Designer* for Windows. Se lo modificate, Designer utilizzerà sempre ciò che vi è definito, indipendentemente da come, quando o dove lo avviate. Per apportare modifiche è necessario modificare nuovamente il codice XML, entrambi descritti di seguito, che tendono ad essere coinvolti in qualche modo.
* <b>Impostazione temporanea della sessione tramite un argomento della riga di comando\
  </b>Designer può utilizzare un argomento della riga di comando all&#39;avvio per eseguire l&#39;override del file SBSCFG per quella sessione (vedere di seguito per istruzioni). Si tratta di una soluzione semplice ed elegante che consente di cambiare progetto in modo molto più rapido rispetto alla modifica di un file XML. Il pericolo è che se si aprono più scelte rapide (ad esempio Menu Start e Desktop su Windows), è possibile ottenere risultati diversi senza che ciò sia del tutto evidente. Inoltre, non è a prova di manomissione: gli utenti possono infatti eliminare, spostare o modificare le scelte rapide in modo molto più semplice rispetto a user\_preferences.xml.

## Modifica XML

### Modifica manuale delle preferenze

Se non è disponibile una configurazione automatica o per scopi di test, è possibile accedere manualmente a <b>Modifica > Preferenze...</b> e quindi fare clic sulla sezione &quot;<b>Progetti</b>&quot; a sinistra.

![Impostazioni progetto](../../assets/preferences-ui.png "Impostazioni progetto")

Il pulsante contrassegnato in rosso consente all&#39;utente di scegliere un diverso [file SBSCFG](../../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md).

### Modifica tramite script

Proprio come per i file di progetto e di configurazione, le preferenze dell’utente sono XML strutturato, con l’impostazione pertinente chiaramente identificabile. Invece di apportare modifiche tramite un editor di testo come Blocco note++ o Testo sublime, è molto adatto per le modifiche tramite una configurazione con script esterno.

Il vantaggio dello scripting è che l&#39;utente non deve fare altro che fare clic su un pulsante, e se viene creato un sistema sufficientemente complicato è possibile gestire e scambiare facilmente il progetto senza dover gestire file e impostazioni manualmente.

La riga pertinente è simile alla seguente:

```
  <configuration> 

   <configurationfile>file:///C:/Users/John/AppData/Local/Adobe/Adobe Substance 3D Designer/default_configuration.sbscfg</configurationfile> 

  </configuration>
```


#### Esempio di Python

Di seguito è riportata una semplice funzione di esempio Python 2.7 per Windows che modifica l&#39;utente\_preferences.xml per un altro file di configurazione. Questo modifica permanentemente il valore finché non viene ripristinato. La funzione SetConfigurationFile può quindi essere chiamata con il percorso del file sbscfg personalizzato come parametro.

Uno script python consente un codice potente e pulito, e può essere facilmente integrato altrove, ma l&#39;aspetto negativo è che per essere eseguito da un utente, deve essere compilato su un eseguibile o l&#39;utente ha bisogno di una distribuzione Python.

```
import xml.etree.ElementTree as ElementTree 

import os 

 

##Example Python script for changing Substance 3D Designer user preference file## 

 

def SetConfigurationFile(p_ConfigPath): 

## Check is the path passed as parameter exists.

    if(os.path.isfile(p_ConfigPath)): 

## replace backslashes by forwardslahes to ensure consistency

        p_ConfigPath = p_ConfigPath.replace("\", "/") 

## get Local Appadata path from Environment variables, construct full path to user_preferences.xml and check if it exists.

        m_AppDataPath = os.environ.get('LOCALAPPDATA') 

        if m_AppDataPath != None: 

            m_UserPrefsPath = os.path.join(m_AppDataPath, str("Adobe/Adobe Substance 3D Designer/user_preferences.xml")) 

            if(os.path.isfile(m_UserPrefsPath)): 

## read XML elementtree from file, find correct element until we get to the actual line that defines the configurationfile path

                m_PrefsTree = ElementTree.parse(m_UserPrefsPath) 

                m_PrefsRoot = m_PrefsTree.getroot() 

                m_PrefsElement = m_PrefsRoot.find("preferences") 

                m_XMLError = True 

                if(m_PrefsElement != None): 

                    m_ConfigElement = m_PrefsElement.find("configuration") 

                    if(m_ConfigElement != None): 

                        m_ConfigFileElement = m_ConfigElement.find("configurationfile") 

                        if(m_ConfigFileElement != None): 

                            m_XMLError = False 

## Check if path is already set, to avoid double work

                            if m_ConfigFileElement.text.replace("file:///","") == p_ConfigPath: 

                                print "configurationfile is already set to desired path. Aborting." 

                                return True 

                            else: 

## construct correctly formatted path, insert into elementtree

                                m_ConfigPath = str("file:///" + p_ConfigPath) 

                                m_ConfigFileElement.text = m_ConfigPath 

 

## Write to file

                                m_XMLString = str("<?xml version="1.0" encoding="UTF-8"?>n") + ElementTree.tostring(m_PrefsRoot, 'utf-8') 

                                m_File = open(m_UserPrefsPath,'w') 

                                m_File.write(m_XMLString) 

                                m_File.close() 

                                print "configuration file path succesfully changed!" 

                                return True 

                if m_XMLError: 

## if this flag was not set to false, we can assume something was missing or went wrong when walking through the XML

                    print("Error: malformed content in user_preferences.xml!") 

                    return False 

            else: 

                print "Error: user_preferences.xml does not exist, try starting Substance 3D Designer first!" 

                return False 

        else: 

            print "Error: LocalAppData path returned None" 

            return False 

    else: 

        print "Error: Invalid Configuration File path!" 

        return False
```


## Scelta rapida degli argomenti della riga di comando

In modo molto più semplice, Designer può essere avvisato di utilizzare un SBSCFG specifico all&#39;avvio tramite l&#39;argomento &quot;—config-file&quot; (opzionale).

### Impostazione manuale

Sebbene non sia consigliabile utilizzare un metodo manuale in un ambiente di produzione, a scopo di test questo può essere fatto abbastanza rapidamente se avete già impostato il file SBSCFG.

1. Aggiungi uno spazio
1. Add —config-file dopo il percorso di progettazione nella sezione Target.
1. Aggiungi un altro spazio
1. Aggiungi il percorso, *racchiuso tra virgolette* per evitare problemi con gli spazi nel percorso
1. Il risultato dovrebbe essere simile al seguente:

   *&quot;C:\Program Files\Adobe\Adobe Substance 3D Designer\Adobe Substance 3D Designer.exe&quot; —config-file &quot;C:\Dev\Substance\custom\_configuration.sbscfg&quot;*

![Input del file di configurazione nelle proprietà del file eseguibile](../../assets/shortcutargument.jpg "Input del file di configurazione nelle proprietà del file eseguibile")
