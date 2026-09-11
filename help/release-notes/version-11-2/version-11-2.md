---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-11-2.html"
breadcrumb-title: ''
description: Consulta le note sulla versione per Substance 3D Designer versione 11.2 per informazioni sulle nuove funzioni, i miglioramenti e le correzioni di bug.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 11.2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versione 11.2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---


# Versione 11.2

**Substance 3D Designer 11.2** ha cambiato leggermente nome ed è ora connesso a Adobe Creative Cloud. Introduce la prima versione di Substance Model Graphs, la funzionalità Invia a, una serie di nodi basati su Raytrace e alcune modifiche dell&#39;interfaccia utente.

Data di pubblicazione: *23 giugno 2021*

## Funzioni principali

### Nuovi grafici modello Substance

È disponibile un tipo di grafico completamente nuovo, il Graph del modello Substance, che consente di creare modelli 3D procedurali utilizzando un&#39;interfaccia nodo familiare.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/structure-tower-render-b.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../assets/structure-paper-creatures-render-a.jpg){width="300px"}

</td>
</tr>
</table>

Per ulteriori informazioni, consultate la nuova sezione dedicata alla documentazione.

Questa è una prima versione, quindi prevedi alcune limitazioni.

### Funzionalità Invia a

Le versioni di Adobe di Substance 3D Designer dispongono della nuova funzionalità Invia a, che consente di inviare rapidamente le risorse ad altre applicazioni Substance 3D. Non è più necessario pubblicare come SBSAR e caricare singoli file, Invia a risolve questo problema con un clic.

![](../../assets/sendto-button.gif)

>[!NOTE]
>
> Le versioni Steam di Substance 3D Designer non dispongono della funzionalità Invia a.

### Nuovi nodi Raytrace

Nessuna versione di Designer è stata completata senza alcuni nuovi nodi. Basandosi sulla fenomenale forza di PBR render, in questa release sono stati aggiunti 5 nuovi nodi basati su RT.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/image2021-6-18-11-11-11.png){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../assets/image2021-6-18-11-9-0.png){width="300px"}

</td>
</tr>
</table>

RTAO fa un lavoro ancora migliore in nitidezza, correggere AO rispetto al nodo HBAO precedente.

![](../../assets/rt-caustics-grayscale.png){width="300px"}

La caustica genera caustiche raytracing fisicamente corrette in base a una mappa di altezza, come un semplice disturbo di Perlin. Ideale per creare texture flipbook realistiche e animate per caustiche in tempo reale.

![](../../assets/image2021-6-22-16-36-36.png){width="300px"}

RT Shadow genera ombre precise e ray tracing, con alcuni semplici controlli.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/rt-irr-01.jpg){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../assets/rt-irr-03.jpg){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../assets/rt-irr-02.jpg){width="200px"}

</td>
</tr>
</table>

RT Irradiance è il più avanzato tra i nuovi nodi. Effettua l&#39;irraggiamento con ray tracing basato su un materiale con mappa del height e una mappa dell&#39;ambiente e/o una mappa di emissione.

![](../../assets/rt-irrad-pro.jpg){width="600px"}

Ciò significa che potete creare texture con illuminazione pre-cotta, come per progetti stilizzati, o potete eseguire il baking in bagliore raytracing che rimbalza sulla mappa dell’altezza.

![](../../assets/bent-normal-ex.jpg){width="300px"}

E infine c&#39;è il nodo Normale piegato. Rispetto a una normale conversione normale regolare, questo nodo utilizza AO per modificare la mappa di normalizzazione per utilizzare le informazioni di AO. Prima che tu abbia bisogno di forni a trama per creare l&#39;effetto, questo nodo lo fa in texturespace per te.

### Adobe Standard Material Shader

Nei nostri sforzi per unificare i materiali e il rendering tra le nostre applicazioni, il nuovo shader predefinito nella vista 3D è Adobe Standard Material Shader. A prima vista non è diverso dal vecchio shader rugosità metallica PBR (è basato comunque su di esso), ma supporta molti canali più esotici, consentendovi di visualizzare in anteprima questi elementi senza bisogno di un renderer esterno.

### Modifiche all’interfaccia utente

Sono state apportate piccole modifiche all’interfaccia utente, ma quelle più evidenti sono un menu File > Nuovo pacchetto migliorato, che consente di scegliere il tipo di grafico, e pulsanti migliorati e aggiornati sulla barra degli strumenti principale, che forniscono scelte rapide per nuovi tipi di grafici e l’invio ad altre applicazioni.

## Tutorial

Di seguito sono riportate le nostre esercitazioni video sulle nuove funzioni:

## Note sulla versione

### 11.2.0

*(Rilasciato Il 23 Giugno 2021)*

**Aggiunto:**

* Il Substance Designer [Branding] diventa Adobe Substance 3D Designer
* [Modelli di Substance] Nuovi grafici per modelli di Substance per creare modelli 3D procedurali
* [Content] Aggiungi nuove mappe ambiente HDR
* [Content] Nuovo nodo normale piegato
* [Content] Nuovo nodo di Occlusione ambiente RT
* [Contenuto] Nuovo nodo Riflessioni personalizzate
* [Contenuto] Nuovo nodo Riflessioni personalizzate
* [Content] Nuovo nodo Irradianza RT
* [Content] Nuovo nodo Ombre RT
* [Interoperabilità] Invia la risorsa a Painter, avvierà Painter e aggiungerà o aggiornerà la tua risorsa nella libreria (richiede un piano Substance 3D per Adobe)
* [Interoperabilità] Invia la risorsa a Sampler, avvierà Sampler e aggiungerà o aggiornerà la tua risorsa nella libreria (richiede un piano Substance 3D per Adobe)
* [Interoperabilità] Sfoglia la tua risorsa in Adobe Bridge, avvierà Bridge nel percorso della risorsa (richiede un piano Substance 3D di Adobe)
* [ASM] Supporto del nuovo Adobe Standard Material (ASM) nel grafico Grafici Substance e MDL
* [ASM] Aggiunta di maschere ASM
* [ASM] Aggiunta dello shader OpenGL per ASM
* [ASM] Impostate lo shader ASM come shader predefinito
* [Generale] Aggrega tutti i file temporanei nella directory temporanea impostata dall&#39;utente
* [Generale] Nuovo comando &quot;Salva una copia con nome&quot;
* [Generale] Menu Aggiorna file
* [Generale] Aggiorna menu?
* [Publish] Nuova finestra di pubblicazione
* [Publish] Aggiungi l&#39;opzione nelle preferenze per non salvare il file SBS durante la pubblicazione di un file SBSAR
* [Proprietà] Aggiungi il campo del tipo di grafico alle proprietà del grafico
* [Proprietà] Riordina le proprietà dei grafici in modo più pertinente
* [Branding] Nuova finestra Informazioni su
* [Branding] Aggiorna stile applicazione
* [GLSLFX] Aggiungere un&#39;etichetta alle tecniche
* [GLSLFX] Aggiungi la possibilità di impostare l’etichetta di uno shader GLSLFX
* [Metadati] Aggiungere metadati nelle risorse del pacchetto
* [Metadati] Consenti edizione metadati per grafici, input, output e risorse
* [Localizzazione] Nuove traduzioni in tedesco, francese e cinese semplificato
* [UX] Inverti zoom nella vista 3D in caso di trascinamento del mouse
* [AXF] Aggiornamento alla versione 1.8.0
* [Registri] Aggiungi i plug-in installati ai registri
* [VFX] Aggiungere la configurazione OpenColorIO ACES 1.2
* [API Python] Aggiungi un metodo per eseguire una query sulla directory tmp specificata nelle impostazioni
* [API Python] Aggiungi un metodo isModified a SDPackage per verificare se un pacchetto è stato salvato
* [API Python] Aggiungi alcuni metodi di conversione del colore a SDColorManagementEngine
* [API Python] Elimina gli oggetti del grafico (Commenti, perni, fotogrammi, ecc.)
* [API Python] Esposizione della proprietà della Dimensioni fisiche per i nodi dell&#39;istanza del grafico
* [API Python] Esponi Salva una copia con nome
* [API Python] Correggere il metodo SDPackageMgr.savePackage
* [API Python] Ottieni un elenco di oggetti grafici selezionati
* [API Python] Introduzione di nuovi nomi di metodi per l’utilizzo delle selezioni dei grafici
* [API Python] I plug-in non possono aggiungere azioni al primo pannello di navigazione creato

**Corretto:**

* [Parametri] I valori negativi nei parametri Integer1 a discesa determinano un comportamento incongruente nell&#39;istanza
* [Parametri] Problema durante l’incremento di un valore su un widget angolo
* [Grafico] Problemi di tempo quando l&#39;output viene visualizzato nella vista 2D o 3D.
* [Internazionalizzazione] Alcuni caratteri specifici vengono trasformati in spazi negli identificatori di file
* [Preferenze] L’etichetta del file &quot;Progetto utente&quot; non viene riconvertita dal giapponese
* [API Python] RecursionError durante l&#39;esecuzione del metodo SDUIMgr.getCurrentGraphSelectedNodes()
* [API Python] SDApplication.getPath(SDApplicationPath.InstallationDir) non restituisce nulla
* [API Python] SDSBSARExporter non invia notifiche di salvataggio dei file
