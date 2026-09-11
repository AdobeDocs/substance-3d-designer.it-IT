---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Scopri l’interfaccia legacy dei baker Substance 3D Designer per gli utenti che hanno familiarità con le versioni precedenti.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interfaccia legacy baker
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 4%

---


# Interfaccia legacy baker

Ecco la descrizione dell&#39;interfaccia di baker disponibile nelle versioni [Adobe Substance 3D Designer](https://www.adobe.com/products/substance3d-designer.html) precedenti alla 6.0.4.

## Panoramica

![](bakers-legacy-interface.resources/image2017-3-13-9-33-40.png)

Il pannello baker è diviso in 4 parti:

### 1: Scena

![](bakers-legacy-interface.resources/image2017-3-13-9-35-53.png)

Consente di definire quale parte della trama è coinvolta nel processo di esegue i baking.

Novità nella versione 6, è anche possibile selezionare in base al materiale:

![](bakers-legacy-interface.resources/image2017-3-13-9-45-26.png)

### 2: Baker

![](bakers-legacy-interface.resources/image2017-3-13-9-46-26.png)

Premendo il pulsante ![](bakers-legacy-interface.resources/image2017-3-13-9-47-47.png), puoi aggiungere i baker desiderati all&#39;elenco di elaborazione

>[!NOTE]
>
> I banco vengono elaborati in base all&#39;ordine degli elenchi (dall&#39;alto verso il basso): questo può essere importante se si desidera riutilizzare il risultato di un eseguo i baking (come la mappa normale) in un altro eseguo i baking

Facendo clic sul segno &quot;+&quot; nel layout baker è possibile aggiungere i baker in una pila (è possibile inserire in una pila tutti i baker desiderati).

.![](bakers-legacy-interface.resources/image2017-3-13-9-52-8.png)

È possibile rimuovere un eseguo i baking dall&#39;elenco premendo ![](bakers-legacy-interface.resources/image2017-3-13-9-54-33.png)

È possibile riordinare l&#39;elenco dei processi di esegue i baking selezionando un processo di esegue i baking e utilizzando ![](bakers-legacy-interface.resources/image2017-3-13-9-55-33.png)

### 3: Parametri Baker

![](bakers-legacy-interface.resources/image2017-3-13-13-24-0.png)

In questa sezione vengono visualizzate le opzioni specifiche per il baker selezionato corrente.

### 4: Parametri comuni

![](bakers-legacy-interface.resources/image2017-3-13-13-28-12.png)

Visualizza i parametri condivisi tra baker.

>[!NOTE]
>
> Per impostazione predefinita, la modifica di uno di questi parametri avrà effetto su tutti i baker, a meno che non si selezioni Ignora parametri, comuni a tutti i baker: in tal caso, le modifiche saranno locali rispetto al baker corrente.

* **Il campo Nome risorsa** consente di modificare il nome della bitmap generata, se necessario.
* **L&#39;elenco a discesa Formato file** consente di modificare il formato di file dal predefinito (formato bitmap Windows o OS/2, &quot;BMP&quot;).
* **La casella di controllo** Posiziona **risorsa** in una cartella specifica della trama consente di scegliere se la bitmap generata viene memorizzata allo stesso livello del modello o in una nuova sottocartella denominata &quot;Resources&quot;.
* **Il metodo** consente di definire se la nuova risorsa bitmap deve essere collegata o incorporata nel pacchetto Substance.
* **La cartella** consente di definire la posizione in cui salvare le mappe.

Premendo il pulsante OK in basso a destra della finestra baker si avvia la esegue i baking.

Novità della versione 6: è ora possibile annullare la procedura di esegue i baking con il pulsante Annulla:

![](bakers-legacy-interface.resources/image2017-3-13-13-50-4.png)
