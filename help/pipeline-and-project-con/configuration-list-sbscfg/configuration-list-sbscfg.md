---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Scopri come utilizzare gli elenchi di configurazione SBSCFG in Substance 3D Designer per gestire le impostazioni e i predefiniti del progetto.
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Elenco configurazioni - SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Elenco configurazioni - SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Il file di configurazione è molto più semplice rispetto ai [file di configurazione del progetto](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md), in quanto contiene solo un elenco di progetti e una modalità di compatibilità del motore. Fungono da elenco di configurazione di progetto/ambiente di livello superiore rispetto ai singoli file di progetto.

Puoi avere più configurazioni per ambienti diversi, questi file possono essere mantenuti sotto il controllo della versione insieme ai file SBSPRJ.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Icona file SBSCFG](../../assets/sbscfg.png "Icona file SBSCFG")

</td>
</tr>
</table>

## Modifica dei file di configurazione

Questi file sono semplici, ma possono comunque essere modificati in due modi diversi, proprio come i file SBSPRJ.

### Nelle impostazioni del progetto

La sezione evidenziata è la parte che si riferisce ai File di configurazione, è sufficiente aggiungere più Progetti all&#39;elenco che sono memorizzati nel file SBSCFG sopra definito.

![Impostazioni progetto](../../assets/config-ui.png "Impostazioni progetto")

### Modifica esterna come XML

Per Windows <b>Blocco note++</b> è una buona opzione gratuita, per macOS <b>Testo sublime</b> è un&#39;alternativa. Tuttavia, qualsiasi editor con rientri corretti, compressione delle sezioni e alcune forme di evidenziazione della sintassi semplificheranno notevolmente la vostra vita.

Una volta aperto il file SBSCFG in un editor, dovresti vedere un layout strutturato abbastanza semplice, con sezioni corrispondenti all&#39;interfaccia.

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


Tieni presente che i progetti utente e predefiniti non sono elencati in modo esplicito e che eventuali progetti aggiuntivi vengono definiti dopo questi.

L&#39;esempio precedente utilizza anche [percorsi relativi](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md). Si noti che la logica dei percorsi relativi è leggermente diversa tra i file CFG e PRJ: per i file CFG, come sopra, **non digitare &quot;file:/&quot; prima del percorso**. Al contrario, il percorso viene semplicemente aggiunto alla posizione del file CFG in cui è definito.

## Rimozione della libreria predefinita

Per il momento, la libreria predefinita non può essere rimossa. Probabilmente non è una buona idea farlo comunque, dato che perdereste molte delle funzionalità di Designer.
