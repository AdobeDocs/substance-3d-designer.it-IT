---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: Risoluzione dei problemi di Visualizzazione 3D in Substance 3D Designer, inclusi problemi di rendering, visualizzazione e prestazioni.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Problemi della vista 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: d81d92788a4d52b5ae1ed3ac4287f07260894f3c
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 0%

---


# Problemi della vista 3D

In questa pagina sono elencati i problemi tecnici relativi alla [vista 3D](../../interface/3d-view/3d-view.md) in Substance 3D Designer e sono disponibili procedure per la risoluzione dei problemi per ciascuno di essi.

## Prestazioni ridotte: la GPU discreta non viene utilizzata

**![(errore)](../../assets/error.svg) Problema**

Substance 3D Designer non utilizza la GPU *separata* del sistema (<b>dGPU</b>) e utilizza invece la GPU *integrata* (<b>iGPU</b>). Questo comporta prestazioni ridotte durante il rendering dei grafici e/o della [vista 3D](../../interface/3d-view/3d-view.md).

**![(tick)](../../assets/check.svg) Passaggi consigliati**

I sistemi con grafica commutabile possono *forzare la dGPU* che deve essere utilizzata per *un&#39;applicazione specifica* in un software dedicato, a seconda del produttore della GPU.

Ad esempio, gli utenti con una <b>Nvidia dGPU</b> possono effettuare le seguenti operazioni:

1. Chiudi Substance 3D Designer
2. Apri il <b>Pannello di controllo NVIDIA</b>
3. Passate alla schermata <b>Gestisci impostazioni 3D</b> nella sezione <b>Impostazioni 3D</b>
4. Cercare la voce &#39;Substance 3D Designer&#39; nella scheda <b>Impostazioni programma</b>
5. Selezionate <b>Processore NVIDIA ad alte prestazioni</b> nella casella combinata <b>GPU preferita</b>
6. Avvia Substance 3D Designer

>[!WARNING]
>
> Le GPU integrate (iGPU) sono *non supportate*. Ulteriori informazioni sono disponibili nella pagina [Requisiti di sistema](../../getting-started/system-requirements/system-requirements.md).

## L&#39;oggetto 3D è piatto

**![(errore)](../../assets/error.svg) Problema**

Un oggetto 3D che presentava volumi dettagliati in una sessione diventa piatto nella sessione successiva, tuttavia il grafico non è cambiato e la mappa del Height contiene gli stessi dati.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

L&#39;effetto di deformazione di un oggetto 3D in base a una mappa del Height viene eseguito utilizzando una tecnica denominata **spostamento di tassellatura**. Questa tecnica prevede due fasi:

1. **Tassellatura**: la geometria dell&#39;oggetto è *suddivisa* in vertici, risultando in una *geometria più densa* per supportare dettagli di volume più precisi
2. **Spostamento**: i vertici sono *spostati*, ovvero spostati, lungo il *vettore normale*. Il vettore normale segue la direzione verso cui è rivolto un poligono e ha una grandezza (cioè lunghezza) di 1

La *direzione* dello spostamento è nota: la direzione del vettore normale.\
Lo spostamento *distanza* in base al quale vengono spostati i vertici viene calcolato come segue: `Distance = Height scale * Height map`. Poiché la mappa Height *non è stata modificata* nel grafico, rimane la **scala Height**.

Il valore di scala Height predefinito è **1.0** e questo può causare un effetto di spostamento *non visibile* a seconda della trama visualizzata nella vista 3D e della mappa del Height ad essa applicata.

Questo valore può essere modificato nei modi seguenti:

| Nella vista 3D | Nella vista Grafico |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Utilizza la finestra a comparsa **Spostamento** nella barra degli strumenti a sinistra.<br>Ulteriori informazioni nella [pagina dedicata](../../interface/3d-view/displacement/displacement.md). | Creare un nodo [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) e impostare l&#39;utilizzo `heightScale` nelle relative proprietà.<br>Fornire un valore a questo output con un valore, utilizzando ad esempio un [nodo mobile costante](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats), quindi *riapplicare il grafico* nella vista 3D. |

>[!TIP]
>
> Utilizzando questo metodo, puoi impostare un valore di scala Height personalizzato *per grafico*, che ti consente di regolarlo in modo che corrisponda al materiale specifico di quel grafico.

## La vista 3D è completamente nera

**![(errore)](../../assets/error.svg) Problema**

Nelle versioni 15.0.0 e successive, il riquadro della vista 3D è nero piatto. Vedo alcune sovrapposizioni di testo (ad esempio, campioni e tempo di rendering) ma la scena 3D non è visibile.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Versione 15.1 e successive

I nuovi moduli di rendering 3D sono stati aggiornati nella versione 15.1 e richiedono driver GPU recenti. Aggiornate i driver della GPU del sistema alla versione più recente.

I driver sono disponibili qui: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us) [AMD](https://www.amd.com/en/support) [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Versione 15.0 e successive

In Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) sono stati introdotti nuovi [moduli di rendering 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) interni, che utilizzano tecnologie moderne e non sono pertanto supportati dalle GPU meno recenti.

Le GPU supportate includono NVIDIA RTX 20 Series (Turing) o versioni successive, in base ai [requisiti di sistema](../../getting-started/system-requirements/system-requirements.md) di Designer.

Per impostazione predefinita, potete continuare a utilizzare il modulo di rendering OpenGL utilizzando la [nuova opzione nelle impostazioni del progetto](../../interface/preferences-window/project-settings/project-settings.md):

1. Seleziona Modifica > Preferenze > Progetti.
2. Seleziona l’ultimo file di progetto nell’elenco
3. Nell’elenco dei file di progetto, seleziona la scheda Visualizzazione 3D
4. Imposta l’opzione &quot;Modulo di rendering predefinito&quot; su &quot;OpenGL (obsoleto)&quot;
5. Fare clic su &#39;OK&#39; per convalidare le modifiche

Ora, per impostazione predefinita, in tutte le nuove viste 3D viene utilizzato il modulo di rendering OpenGL, che consente di continuare a lavorare come prima.

>[!NOTE]
>
> Le stesse procedure per la risoluzione dei problemi e la risoluzione dei problemi si applicano alla maggior parte delle GPU AMD e Intel, attualmente *non supportate* dai nostri nuovi moduli di rendering 3D.

>[!IMPORTANT]
>
> Il modulo di rendering OpenGL è *deprecato* e potrebbe essere rimosso da Designer in futuro. Si consiglia di aggiornare la GPU del sistema per evitare interruzioni nel flusso di lavoro e garantire un supporto continuo.

## Viene visualizzato il messaggio &quot;Rendering non supportato&quot;

**![(errore)](../../assets/error.svg) Problema**

Nelle versioni 15.0.0 e successive, il messaggio &quot;Modulo di rendering non supportato&quot; viene visualizzato nell’angolo inferiore destro della finestra della vista quando si utilizzano i nuovi moduli di rendering 3D (Rasterizzatore, Tracciatore percorso GPU). La scena 3D non è visibile.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

In Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md) sono stati introdotti nuovi [moduli di rendering 3D](../../interface/3d-view/3d-renderers/3d-renderers.md) interni, che utilizzano tecnologie moderne e non sono pertanto supportati dalle GPU meno recenti.

Le GPU supportate includono NVIDIA RTX 20 Series (Turing) o versioni successive, in base ai [requisiti di sistema](../../getting-started/system-requirements/system-requirements.md) di Designer.

In base alle impostazioni predefinite, la Vista 3D tornerà automaticamente al modulo di rendering OpenGL se l’opzione &quot;Modulo di rendering predefinito&quot; è impostata su &quot;Predefinito (modulo di rendering predefinito)&quot; nelle [Impostazioni progetto](../../interface/preferences-window/project-settings/project-settings.md).

Questa opzione può essere individuata e regolata come descritto di seguito:

1. Seleziona Modifica > Preferenze > Progetti.
2. Seleziona l’ultimo file di progetto nell’elenco
3. Nell’elenco dei file di progetto, seleziona la scheda Visualizzazione 3D
4. L’opzione &quot;Modulo di rendering predefinito&quot; è elencata nelle impostazioni della scheda

>[!NOTE]
>
> Al momento è possibile rilevare come non supportate solo le GPU della <b>serie NVIDIA GTX</b>.
> 
> Tuttavia, anche la maggior parte delle GPU AMD e Intel non è supportata e produrrà un rendering nero senza alcun messaggio. Consulta l&#39;elemento &quot;La vista 3D è completamente nera&quot; qui sopra per indicazioni su tali GPU.

>[!IMPORTANT]
>
> Il modulo di rendering OpenGL è *deprecato* e potrebbe essere rimosso da Designer in futuro. Si consiglia di aggiornare la GPU del sistema per evitare interruzioni nel flusso di lavoro e garantire un supporto continuo.

## L&#39;oggetto 3D appare perfettamente uniforme

**![(errore)](../../assets/error.svg) Problema**

Dopo aver lavorato sui dati inviati al **Height** [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), l&#39;oggetto sembra avere un certo volume ma *sembra perfettamente fluido*, come se le informazioni sul height fossero state ignorate nell&#39;ombreggiatura.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Assicurati che i dati di height siano *convertiti in normali* connessi all&#39;**normale** [output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

Quando si utilizza la tecnica **Spostamento di tassellatura** (vedere &quot;L&#39;oggetto 3D è piatto&quot; sopra), gli oggetti possono *deformarsi* per seguire i dati del height, ma la sua superficie *non reagisce alla luce in modo diverso* finché non vengono modificate anche le *normali* per tenere conto dei dati del height.

La soluzione è piuttosto semplice: connettere l&#39;ultimo nodo del flusso che porta all&#39;output del Height a un nodo [Normale](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). Regolare il parametro **Intensità** del nodo in base al materiale su cui si sta lavorando e connettere il nodo Normale all&#39;output **Normale**.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/3dview-height-without-normals.gif){width="256px"}

</td>
</tr>
</table>

## Il rendering è sfocato/pixelato

**![(errore)](../../assets/error.svg) Problema**

L&#39;immagine sottoposta a rendering appare sfocata o pixelata quando il sistema utilizza *il ridimensionamento dello schermo*.

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Per impostazione predefinita, Designer utilizza la risoluzione di visualizzazione *ridimensionata* per definire la risoluzione di rendering della [vista 3D](../../interface/3d-view/3d-view.md). Puoi modificare questa impostazione in modo che venga utilizzata la risoluzione di visualizzazione *nativa* per un rendering nitido.

Apri il menu **Modifica** e seleziona l&#39;opzione **Preferenze...**. Nella finestra [Preferenze](../../interface/preferences-window/preferences-window.md), aprite la sezione **Visualizzazione 3D** e impostate il parametro **Ridimensionamento finestra** su *Nessuno*.

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/demo-viewport-scaling-option.png){width="256px"}

</td>
</tr>
</table>

## Impossibile trovare la proprietà &#39;Fattore di tassellatura&#39;

**![(errore)](../../assets/error.svg) Problema**

Dopo aver aggiornato Designer alla versione 15.0.0, non è possibile trovare il parametro &#39;Fattore di tassellatura&#39; nelle proprietà del materiale in cui si trovava.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Quando si utilizzano nuovi moduli di rendering (rasterizzatore e Pathtracer GPU), il &quot;fattore di tassellatura&quot; si trova nelle proprietà di questi moduli di rendering. Nella vista 3D, selezionate <b>Modulo di rendering > Modifica impostazioni</b>. La proprietà verrà elencata nel Dock proprietà.

>[!NOTE]
>
> L’ambito della tassellatura varia a seconda del modulo di rendering:
> 
> * Rasterizzatore/Pathtracer GPU: valore univoco applicato globalmente all’intera scena.
> * OpenGL: un valore per materiale.
> * Matrice: un valore per trama.

## Gli oggetti 3D non vengono visualizzati correttamente: la loro ombreggiatura non è adatta all&#39;illuminazione

**![(errore)](../../assets/error.svg) Problema**

L’ombreggiatura degli oggetti si basa sui loro vettori normali, tangenti e binormali. Le loro coordinate usano l&#39;intervallo [-1, 1], mentre le mappe normali usano l&#39;intervallo [0, 1] nella maggior parte dei casi. Per adattare i valori da uno all&#39;altro, è necessario applicare un <b>bias e una scala</b>: valore\*scala+bias.

Ad esempio, una scala pari a 2 e una distorsione pari a -1 adatta il valore x da [0, 1] a [-1, 1]: x\*2-1.

Designer non applica una scala e una distorsione normali a meno che non siano specificate da una trama 3D. Se tali informazioni mancano, verrà generato un avviso nella console quando [si sostituisce uno dei materiali](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md):

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![(tick)](../../assets/check.svg) Passaggi consigliati**

Per le scene esportate nei formati USD poco tempo fa: riesporta la scena utilizzando una versione recente di USD, che includerà i dati necessari. Presta attenzione alle proprietà relative alla scala normale e ai pregiudizi, se presenti, che dipenderanno dal software utilizzato per esportare la scena.

Quando [si esegue l&#39;override di un materiale](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md), Designer elabora la trama e calcola eventuali dati mancanti relativi alle sue normali, tangenti e binormali. Se la scala e la distorsione predefinite di Designer corrispondono a quelle richieste per la trama, quest’ultima avrà un aspetto corretto quando viene sostituita.

## Arresto anomalo all’avvio della vista 3D

**![(errore)](../../assets/error.svg) Problema**

Designer si arresta in modo anomalo all’avvio della vista 3D, durante la creazione di un progetto, il caricamento di un progetto o l’avvio manuale di una vista 3D.

**![(tick)](../../assets/check.svg) Passaggi consigliati**

Per prima cosa, assicurati che il tuo sistema soddisfi i [requisiti di sistema](../../getting-started/system-requirements/system-requirements.md) di Designer.

Quindi, aggiorna i driver di grafica. Per trovare i driver più recenti per la GPU, segui questi collegamenti: [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

Se il sistema include sia una GPU integrata (iGPU) che una GPU discreta (dGPU), assicurati di *aggiornare i driver per entrambi*.

Quindi, disattivate qualsiasi software che possa inserire o sovrapporre dati in un processo di grafica 3D. Alcuni esempi:

* Iniettori post-elaborazione come ReShade
* Sovrapposizioni, ad esempio crocette personalizzate o metriche delle prestazioni GPU
* Software di acquisizione schermo per la registrazione, lo streaming o la condivisione di grafica 3D in tempo reale
