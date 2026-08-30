---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render.html"
breadcrumb-title: ''
description: Utilizza il nodo del PBR render per eseguire il rendering di materiali basati fisicamente con un'illuminazione realistica per visualizzare in anteprima l'aspetto del materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR render
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 6%

---


# PBR render

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render.resources/pbr-render.png){width="250px"}

<b>In:</b> Filtri materiali > Utilità PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue il rendering di un materiale PBR su una sfera, un piano o un cilindro utilizzando l&#39;illuminazione basata su immagine (IBL). Si tratta di un motore di rendering all&#39;interno di un nodo che può essere molto utile per generare miniature, anteprime o risorse 2D. Non è un rendering come la vista 3D, ma una texture effettiva generata nel grafico.

Questo nodo richiede almeno un materiale PBR completo da collegare. Idealmente si utilizza la modalità di creazione del collegamento per collegare il materiale al PBR render. Inoltre, per il rendering è necessario un ambiente HDRI con bordi sferici da cui calcolare l’illuminazione. I materiali per i test sono disponibili in Materiali PBR, le mappe dell&#39;ambiente sono disponibili in [vista 3D nella libreria.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/3d-view-library.md)

</td>
</tr>
</table>

>[!WARNING]
>
> **Motore CPU (SSE2)**
> 
> Il PBR render Node è molto pesante e non funziona bene con il motore CPU SSE2. Passare a un altro motore premendo F9, se il nodo non funziona correttamente.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input del canale del materiale</b> | Per eseguire il rendering del materiale sulla geometria vengono utilizzati più input di materiale:<br><br>- Colore di base<br>- Normale<br>- Emissivo<br>- Rugosità<br>- Metallico<br>- Specular level<br>- Height<br>- Occlusione ambientale<br>- Maschera di opacità<br>- Livello di anisotropia<br>- Angolo di anisotropia<br>- Traslucidità<br>- Scala della distanza di dispersione |
| <b>Mappa Dirt obiettivo</b> <i>Input scala di grigi</i> | Mappa personalizzata per dirt su obiettivo, visualizzata quando sono visibili i riflessi dell’obiettivo. |
| <b>Mappa apertura obiettivo</b> <i>Input scala di grigi</i> | Può essere utilizzato per sostituire la forma Bokeh, sfocata. Più è contrastato, più è visibile. Tieni presente che viene campionato solo un cerchio all&#39;interno della texture, in modo che qualsiasi forma si adatti a un cerchio. |
| <b>Input in background</b> <i>Input colore</i> | Mapping personalizzato utilizzato come sfondo quando il parametro <b>Modalità sfondo</b> è impostato su <i>Input sfondo</i> |
| <b>Mappa ambiente</b> <i>Input colore</i> | Mappa dell’ambiente utilizzata per calcolare l’illuminazione. Deve essere mappato a livello sferico e in HDR. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Bellezza</b> | Rendering finale |
| <b>Irradianza raw</b> | Dati di irradianza del rendering finale<br><br><i>Alpha:</i> mappa di opacità |
| <b>Specular non elaborato</b> | I dati di specular del rendering finale<br><br><i>Alpha:</i> mappa ombreggiatura Specular |
| <b>Spazio mondo normale</b> | I dati normalizzati dello spazio globale del rendering finale<br><br><i>Alpha:</i> Mappa altezza spazio globale |
| <b>Spazio tangente normale</b> | Dati delle normali dello spazio tangente del rendering finale<br><br><i>Alpha:</i> mappa altezza spazio tangente |
| <b>UV</b> | Dati UV del rendering finale<br><br><i>Alpha:</i> mappa di opacità |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Forma</b> <i>Sfera, Piano, Cilindro</i> | Imposta la forma utilizzata per il rendering. Le forme personalizzate non sono possibili. |
| <b>Intensità Spostamento</b> <i>0.0 - 0.5</i> | Impostate l’intensità dello spostamento dal height. |
| <b>Rotazione ambiente</b> <i>0.0 - 1.0</i> | Ruota l’ambiente di illuminazione. Pre-ruota rispetto allo spostamento della videocamera. |
| <b>Modalità sfondo</b> <i>Colore, Ambiente, Ambiente, Input Sfondo</i> | Impostate gli elementi visualizzati sullo sfondo. Il colore è una tinta unita, l&#39;ambiente è la mappa a cui è stata collegata una sfocatura opzionale. Ambient è una versione molto sfocata dell&#39;ambiente. |
| <b>Colore di sfondo</b> <i>(valore colore)</i> | Disponibile solo quando la modalità Sfondo è impostata su Colore. |
| <b>Sfocatura sfondo ambiente</b> <i>0.0 - 1.0</i> | Disponibile solo quando la modalità Sfondo è impostata su Ambiente. |
| <b>Forma</b> |  |
| <b>Scala</b> <i>0.0 - 2.0</i> | Impostate la scala per la sfera. |
| <b>Dimensione piano</b> <i>0.0 - 1.0</i> | Impostate la scala per il piano. |
| <b>Raggio cilindro</b> <i>0.0 - 1.0</i> | Impostate il raggio per il cilindro. |
| <b>Lunghezza cilindro</b> <i>0.0 - 1.0</i> | Impostate la lunghezza del cilindro. |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Ruota la forma senza l’illuminazione rotante. |
| <b>Direzione rotazione</b> <i>0.0 - 1.0</i> | Imposta l&#39;asse di rotazione in 2D. |
| <b>Rotazione Attorno Alla Direzione</b> <i>0.0 - 1.0</i> | Ruota la forma sull&#39;asse di rotazione. |
| <b>Posizione forma</b> <i>-1.0 - 1.0</i> | Sposta le forme. |
| <b>Affiancamento UV</b> <i>1.0 - 6.0</i> | Imposta la quantità di Affiancamento UV. |
| <b>Scala UV Sfera</b> <i>0.0 - 4.0</i> | Imposta la scala degli UV sulla sfera. |
| <b>Scala UV piano</b> <i>1.0 - 4.0</i> | Imposta la scala degli UV sul piano. |
| <b>Scala UV cilindrica</b> <i>1.0 - 6.0</i> | Imposta la scala degli UV sul cilindro. |
| <b>Offset UV</b> <i>0.0 - 1.0</i> | Scostamento UV |
| <b>Inclinazione UV</b> <i>Falso/Vero</i> | Inclina gli UV di 45 gradi per la Sfera. |
| <b>Fotocamera</b> |  |
| <b>Esposizione</b> <i>-4.0 - 4.0</i> | Impostate l&#39;esposizione della fotocamera. |
| <b>Mappatura toni</b> <i>Lineare, ACE, Hejl cinematografico</i> | Impostate la soluzione di mappatura dei toni da usare per l’immagine finale. |
| <b>Modalità fotocamera</b> <i>Prospettiva, Ortografica</i> | Passa tra due modalità di proiezione. |
| <b>Campo di visualizzazione</b> <i>0.01 - 100.0</i> | Impostare l&#39;angolo FOV della fotocamera. |
| <b>Distanza</b> <i>0.0 - 4.0</i> | Impostate la distanza della videocamera dal centro dell’oggetto. |
| <b>Intensità vignettatura</b> <i>0.0 - 1.0</i> | Impostate l’intensità dell’effetto vignettatura. |
| <b>Raggio vignettatura</b> <i>0.0 - 1.0</i> | Impostate il raggio dell’effetto vignettatura. |
| <b>Posizione schermo</b> | Sposta la videocamera intorno all’oggetto; può essere modificata anche con un gizmo nella vista 2D. |
| <b>Profondità di campo</b> |  |
| <b>Raggio apertura</b> <i>0.0 - 0.1</i> | Imposta il raggio dell’apertura. Valori più elevati rendono le aree sfocate più sfocate (bokeh). |
| <b>Blade di apertura</b> <i>3 - 9</i> | Imposta la forma della sfocatura bokeh. |
| <b>Anello apertura</b> <i>0.0 - 1.0</i> | Aggiunge una sfumatura interna alla forma bokeh. |
| <b>Difrazione dell&#39;apertura</b> <i>0.0 - 2.0</i> | Aggiunge aberrazione cromatica al bokeh. |
| <b>Bokeh vorticoso</b> <i>0.0 - 1.0</i> | Aggiunge un effetto vorticoso o che gira nelle aree di sfocatura bokeh sfocate. |
| <b>Modalità Focus</b> <i>Automatico, Punto</i> | Impostata se lo stato attivo è predeterminato o impostato dall&#39;utente. Il Punto di interesse consente di spostare un punto nella vista 2D per determinare la distanza focale. |
| <b>Punto di interesse</b> | Se lo stato attivo è impostato su Punto, questo consente di spostare quel punto. ha un gizmo per la visualizzazione 2D. |
| <b>Scostamento messa a fuoco</b> <i>-0.5 - 0.5</i> | Se lo stato attivo è impostato su Automatico, consente di spostarlo avanti e indietro. |
| <b>Usa mappa apertura personalizzata</b> <i>Falso/Vero</i> | Ignora le impostazioni di apertura precedenti e utilizza l&#39;input della mappa di apertura per determinare la forma bokeh. Richiede un input. |
| <b>Effetti post</b> |  |
| <b>Abilita Effetti post</b> <i>Falso/Vero</i> | Attiva/disattiva <i>tutti</i> i post-effetti nel rendering finale. |
| <b>Intensità fioritura</b> <i>0.0 - 2.0</i> | Consente di impostare l’intensità dell’effetto fioritura. |
| <b>Soglia di fioritura</b> <i>0.0 - 2.0</i> | Imposta una soglia bassa per la visualizzazione della fioritura. |
| <b>Spostamento crominanza fiorita</b> <i>0.0 - 1.0</i> |  |
| <b>Intensità alone obiettivo</b> <i>0.0 - 1.0</i> | Imposta l’intensità dell’effetto alone lente. |
| <b>Intensità riflessi obiettivo</b> <i>0.0 - 1.0</i> | Imposta l’intensità del riflesso dell’obiettivo. Assicurati che la luce proveniente dallo sfondo dell’ambiente sia in grado di vedere correttamente questo effetto. |
| <b>Intensità Dirt obiettivo</b> <i>0.0 - 1.0</i> | Imposta l’effetto della mappa del dirt dell’obiettivo sui riflessi dell’obiettivo. |
| <b>Impostazioni rendering</b> |  |
| <b>Qualità Diffusa</b> <i>16 Campioni, 32 Campioni, 64 Campioni, 128 Campioni</i> | Consente di passare da un livello di qualità all&#39;altro per la mappa di diffusione. |
| <b>Moltiplicatore Emissivo Diffusa</b> <i>0.0 - 1.0</i> | Controlla l&#39;entità del contributo delle parti di emissione all&#39;irradianza. |
| <b>Intensità ombra Diffusa</b> <i>0.0 - 1.0</i> | Controlla l’intensità delle ombre diffuse. |
| <b>Dithering Specular</b> <i>0.0 - 1.0</i> | Impostate la quantità di dithering dello specular. |
| <b>Moltiplicatore ombra Specular</b> <i>0.0 - 1.0</i> | Controlla l’intensità delle ombre nei riflessi degli specular. |
| <b>Modalità opacità</b> <i>Test Alpha con dithering, Fusione Alpha semplice</i> | Controlla il metodo di applicazione della trasparenza. La modalità <i>Fusione Alpha semplice</i> è più visibile su sfondi uniformi. |
| <b>Intensità Occlusione ambientale</b> <i>0.0 - 1.0</i> | Imposta l’intensità delle ombre di occlusione ambientale. |
| <b>Regolazioni materiale</b> |  |
| <b>Ricalcola normali</b> <i>Falso/Vero</i> | I valori normali verranno ricalcolati dalla mappa dell&#39;altezza in base all&#39;intensità dello spostamento. |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passare da un Formato mappa normale a un altro (inverte il canale verde) |
| <b>Input F0 dielettrico</b> <i>Valore costante, input Specular level</i> | Impostate le unità con i valori F0. L&#39;input di Specular level indica che sarà guidato da una mappa di input. |
| <b>Dielettrico F0</b> <i>0.0 - 0.08</i> | Se per l’input Dielettrico F0 viene selezionato Valore costante, questo cursore consente di impostare il valore globale. |
| <b>Cancella pelo</b> |  |
| <b>Abilita Clear Coat</b> <i>Falso/Vero</i> | Consente di applicare uno strato di rivestimento trasparente aggiuntivo e semplice sopra il materiale di input. |
| <b>Cancella peso pelo</b> <i>0.0 - 1.0</i> | Imposta l’intensità o l’intensità del livello del rivestimento trasparente. |
| <b>Cancella Livello speculare dei rivestimenti</b> <i>0.0 - 1.0</i> | Consente di impostare la ruvidità del livello del rivestimento trasparente. |
| <b>Eredita normale dal livello di base</b> <i>Falso/Vero</i> | Impostate questa opzione se il rivestimento trasparente ignora o utilizza le normali del materiale di base. |
| <b>Emissivo</b> |  |
| <b>Attiva illuminazione Emissivo</b> <i>Vero/Falso</i> | Attiva/disattiva il contributo diffuso dell’illuminazione emissivo. |
| <b>Intensità di emissione</b> <i>0.0 - 10.0</i> | Imposta il moltiplicatore globale per la mappa emissivo. |
| <b>Dispersione sottosuperficie</b> |  |
| <b>Abilita dispersione sottosuperficie</b> <i>Vero/Falso</i> | Attiva/disattiva la dispersione sottosuperficie nel rendering finale.<br><br><i>Nota:</i> la dispersione sottosuperficie richiede che il valore di input <b>Traslucidità</b> sia <i>superiore a 0,0</i> |
| <b>Distanza di dispersione</b> <i>0.0 - 1.0</i> | Regola la distanza massima dell&#39;effetto di dispersione.<br><br><i>Nota:</i> questo valore viene moltiplicato rispetto al valore di input <i>per canale di colore</i> della <b>Scala distanza di diffusione</b>. |
| <b>Scostamento rosso</b> <i>0.0 - 1.0</i> | Regola l’intensità dell’effetto Spostamento rosso nella dispersione. |
| <b>Rayleigh</b> <i>0.0 - 1.0</i> | Regola l’intensità dell’effetto Rayleigh nella dispersione. |

## Esempi

Tutte le immagini sono state generate direttamente all&#39;interno di Designer, nella finestra della vista 2D, utilizzando materiali dalla libreria [Risorse Substance 3D](https://substance3d.adobe.com/assets).

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/pbr-render-v2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-thermal-insulation-panel.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-ominous-obsidian.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-forest-gravel-1.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-chesterfield-1.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/sphere-carbon-fiber.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/plane-inclined-lumber-tiles.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render.resources/cylinder-medieval-leaded-glass-window.jpg" />
        </td>
    </tr>
</table>
