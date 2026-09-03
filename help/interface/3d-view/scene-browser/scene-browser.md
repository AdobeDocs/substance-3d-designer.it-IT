---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/scene-browser.html"
breadcrumb-title: ''
description: Utilizza l’Elenco scene per navigare e gestire elementi, materiali e oggetti della scena 3D nella finestra della vista.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Scene browser
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Browser scene
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 1%

---


# Browser scene

Il browser scene della vista 3D elenca tutti gli elementi della scena e la loro gerarchia.

Offre controlli per la selezione degli oggetti, l&#39;attivazione della loro visibilità e la selezione del materiale che deve [sostituire un materiale della scena](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md).

Poiché Designer utilizza [USD](https://openusd.org/release/index.html) per descrivere e gestire le scene, la terminologia e i concetti utilizzati sono disponibili nell&#39;albero delle scene.

Viene visualizzato facendo clic sul relativo pulsante di attivazione/disattivazione dedicato ![](scene-browser.resources/scene-browser-01.png) nella barra degli strumenti [della scena della vista 3D](../../../interface/3d-view/3d-view.md).

![Browser scene - Scena 3D caricata](scene-browser.resources/scene-browser-02.png "Browser scene - Scena 3D caricata"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Albero delle scene

</td>
<td style="border: 0;" valign="top">

### Alternare gli oggetti nella scena

</td>
<td style="border: 0;" valign="top">

### Materiali connessi

</td>
</tr>
</table>

## Albero delle scene

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

L’elenco delle scene visualizza un elenco di oggetti disposti in una struttura gerarchica.

Gli oggetti sono associati ad altri oggetti, fino alla radice della scena. Un oggetto principale è dotato di un pulsante freccia che consente di espandere o comprimere l’elenco dei relativi oggetti secondari.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Browser scene - Albero scene](scene-browser.resources/scene-browser-03.png "Browser scene - Albero scene"){zoomable="yes"}

</td>
</tr>
</table>

Lasciare il cursore su qualsiasi elemento nella struttura per un paio di secondi per visualizzare una descrizione con le seguenti informazioni:

* <b>Percorso:</b> il percorso completo dell&#39;oggetto nella scena.
* <b>TypeName:</b> il tipo USD dell&#39;oggetto.
* <b>Documentazione:</b> informazioni dettagliate sull&#39;oggetto come elemento di scena USD.

Le trame hanno ulteriori informazioni: conteggio dei vertici, conteggio dei volti e conteggio UV.

### Oggetti aggiunti da Designer

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designer aggiunge alcuni oggetti a qualsiasi scena caricata. Gli oggetti aggiunti da Designer sono etichettati in <b>bold</b>.

Quando si utilizza l&#39;azione &quot;Modifica...&quot; nei menu Luci, Videocamera e Ambiente, questi sono gli oggetti che vengono modificati, indipendentemente dal fatto che ci siano altre luci, videocamere o ambienti nella scena.

Questi oggetti sono inclusi nella scena quando [viene esportato](../../../working-with-3d-scenes/exporting-scenes/exporting-scenes.md).

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Browser scene - Oggetti aggiunti da Designer elencati in grassetto](scene-browser.resources/scene-browser-04.png "Browser scene - Oggetti aggiunti da Designer elencati in grassetto"){zoomable="yes"}

</td>
</tr>
</table>

* <b>Fotocamera:</b> La videocamera predefinita della scena. Questa è l’unica videocamera con cui potete interagire in Designer. Tutte le fotocamere incluse in una scena caricata vengono aggiunte come predefiniti per la videocamera predefinita.
* <b>Ambiente:</b> l&#39;ambiente predefinito della scena. Qualsiasi texture applicata all’ambiente della scena verrà applicata solo a tale ambiente. Allo stesso modo, la rotazione dell&#39;ambiente influisce solo su quell&#39;ambiente.\
  Quando una scena caricata include una o più luci ambiente ([DomeLight](https://openusd.org/release/user_guides/schemas/usdLux/DomeLight.html) in USD), l&#39;ambiente predefinito viene disattivato automaticamente per non interferire con l&#39;illuminazione ambiente della scena.
* <b>Luce puntiforme #:</b> Se una delle luci puntiformi di Designer è abilitata in Luci > Modifica proprietà, ogni luce puntiforme viene aggiunta alla scena.

## Alternare gli oggetti nella scena

### Tutti i tipi

Qualsiasi oggetto può essere attivato e disattivato nella scena. Quando è disattivata, un oggetto non contribuisce più alla scena: non proietta ombre, non emette né riflette la luce.

Lo stato di un oggetto principale viene mantenuto sui relativi oggetti secondari, pertanto la disattivazione di un oggetto principale ne comporta anche la disattivazione.

È possibile attivare o disattivare la visibilità di un oggetto facendo clic sul relativo pulsante a forma di occhio ![](scene-browser.resources/scene-browser-05.png) o dal relativo menu di scelta rapida. Il menu offre alcune azioni in più per la gestione della visibilità degli oggetti della scena:

* <b>Nascondi:</b> disabilita l&#39;oggetto selezionato.
* <b>Mostra:</b> abilitare l&#39;oggetto selezionato.

Alcune azioni hanno un impatto specifico sulla visibilità delle trame:

* <b>Mostra solo:</b> disabilita tutte le trame tranne quella selezionata e i relativi elementi figlio.
* <b>Mostra tutto:</b> Abilita tutte le trame.

Gli oggetti principali dispongono delle seguenti azioni aggiuntive:

* <b>Nascondi elementi figlio:</b> Disattiva tutti gli elementi figlio dell&#39;oggetto selezionato, in modo ricorsivo.
* <b>Mostra elementi figlio:</b> Abilita tutti gli elementi figlio dell&#39;oggetto selezionato, in modo ricorsivo.
* <b>Espandere tutti gli elementi figlio:</b> Espandere tutti gli elenchi di elementi figlio sotto l&#39;oggetto selezionato in modo ricorsivo.
* <b>Comprimi tutti i figli:</b> Comprime tutti gli elenchi di figli sotto l&#39;oggetto selezionato in modo ricorsivo.

![Browser scene - Attivazione/disattivazione della visibilità degli oggetti](scene-browser.resources/scene-browser-06.gif "Browser scene - Attivazione/disattivazione della visibilità degli oggetti"){zoomable="yes"}

### Ambienti

La visibilità di qualsiasi luce ambiente (DomeLight) può essere attivata e disattivata allo stesso modo degli altri oggetti.

Quando una luce ambiente è disattivata, anche il suo contributo di illuminazione alla scena è disattivato.

Se sono abilitate più luci ambiente, i relativi contributi di illuminazione sono *aggiunti cumulativamente*.

![Browser scene - Attivazione/disattivazione della visibilità dell&#39;ambiente](scene-browser.resources/scene-browser-07.gif "Browser scene - Attivazione/disattivazione della visibilità dell&#39;ambiente"){zoomable="yes"}

### Luci

Lo stesso vale per qualsiasi luce nella scena: ciascuna può essere attivata o disattivata singolarmente.

![Browser scene - Attivazione/disattivazione della visibilità delle luci](scene-browser.resources/scene-browser-08.gif "Browser scene - Attivazione/disattivazione della visibilità delle luci"){zoomable="yes"}

## Materiali connessi

L&#39;elenco scene consente inoltre di collegare qualsiasi materiale sottoposto a override a un altro materiale elencato da Designer nel [menu Materiali](../../../interface/3d-view/3d-view.md) della vista 3D.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

I materiali elencati da Designer sono gli oggetti Materiali nell&#39;albero della scena utilizzati su almeno una trama.

Quando [sostituisci](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md) uno di questi materiali, Designer crea una copia con suffisso numerico.

Un materiale sottoposto a override offre un elemento aggiuntivo nel relativo menu di scelta rapida: il sottomenu &#39;[Materiale connesso](../../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)&#39; elenca tutti gli altri materiali disponibili che possono essere utilizzati per sovrascrivere questo materiale.

</td>
<td style="border: 0;" valign="top">

![Browser scene - Materiale connesso](scene-browser.resources/scene-browser-09.png "Browser scene - Materiale connesso"){zoomable="yes"}

</td>
</tr>
</table>
