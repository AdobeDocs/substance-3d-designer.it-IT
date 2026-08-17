---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: Scopri l’interfaccia legacy dei Substance 3D Designer baker per gli utenti che hanno familiarità con le versioni precedenti.
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Interfaccia legacy Bakers
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# Interfaccia legacy Bakers

Ecco la descrizione dell&#39;interfaccia del baker disponibile nelle versioni [Adobe Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html) precedenti alla 6.0.4.

## Panoramica

![](../../assets/image2017-3-13-9-33-40.png)

Il pannello panettiera è suddiviso in 4 parti:

### 1: Scena

![](../../assets/image2017-3-13-9-35-53.png)

Consente di definire quale parte della trama è coinvolta nel processo di cottura al forno.

Novità nella versione 6, è anche possibile selezionare in base al materiale:

![](../../assets/image2017-3-13-9-45-26.png)

### 2: Panettieri

![](../../assets/image2017-3-13-9-46-26.png)

Premendo il pulsante ![](../../assets/image2017-3-13-9-47-47.png), puoi aggiungere i panettieri desiderati all&#39;elenco di elaborazione

>[!NOTE]
>
> I panifici vengono elaborati seguendo l&#39;ordine di listino (dall&#39;alto verso il basso): questo può essere importante se si desidera riutilizzare il risultato di un forno (come la mappa normale) in un altro processo di cottura

Facendo clic sul segno &quot;+&quot; nel layout panettieri è possibile aggiungere i panettieri in una pila (è possibile inserire tutti i panettieri che si desidera in una pila).

.![](../../assets/image2017-3-13-9-52-8.png)

È possibile rimuovere un processo di cottura dall&#39;elenco premendo ![](../../assets/image2017-3-13-9-54-33.png)

È possibile riordinare l&#39;elenco dei processi di cottura selezionando un processo di cottura e utilizzando ![](../../assets/image2017-3-13-9-55-33.png)

### 3: Parametri dei forni

![](../../assets/image2017-3-13-13-24-0.png)

In questa sezione vengono visualizzate le opzioni specifiche per il fornaio corrente selezionato.

### 4: Parametri comuni

![](../../assets/image2017-3-13-13-28-12.png)

Visualizza i parametri condivisi tra i panettieri.

>[!NOTE]
>
> Per impostazione predefinita, la modifica di uno di questi parametri avrà effetto su tutti i panettieri, a meno che non si selezioni Ignora parametri, comuni a tutti i panettieri: in tal caso, le modifiche saranno locali rispetto al panettiere corrente.

* **Il campo Nome risorsa** consente di modificare il nome della bitmap generata, se necessario.
* **L&#39;elenco a discesa Formato file** consente di modificare il formato di file dal predefinito (formato bitmap Windows o OS/2, &quot;BMP&quot;).
* **La casella di controllo** Posiziona **risorsa** in una cartella specifica della trama consente di scegliere se la bitmap generata viene memorizzata allo stesso livello del modello o in una nuova sottocartella denominata &quot;Resources&quot;.
* **Il metodo** consente di definire se la nuova risorsa bitmap deve essere collegata o incorporata nel pacchetto Substance.
* **La cartella** consente di definire la posizione in cui salvare le mappe.

Premendo il pulsante OK in basso a destra della finestra dei panettieri si avvia il processo di cottura.

Novità della versione 6: è ora possibile annullare il processo di cottura con il pulsante Annulla:

![](../../assets/image2017-3-13-13-50-4.png)
