---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/2d-view/color-sampler.html"
breadcrumb-title: ''
description: Utilizzate lo strumento Sampler colori nella vista 2D per campionare i colori dalle texture per una corrispondenza di colore precisa.
helpx_creative_field: ""
helpx_description: Designer > Interface > 2D view > Color sampler tool
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Strumento campionatore colore
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---


# Strumento campionatore colore

![Strumento campionatore colore](../../../assets/color-sampler-demo.png "Strumento campionatore colore"){zoomable="yes"}

Lo strumento Sampler colori consente di <b>tenere traccia del valore di un pixel specifico</b> nella [vista 2D](../../../interface/2d-view/2d-view.md) mentre si modificano i parametri o si cambiano i nodi.

Posiziona un perno nella finestra della vista e campiona il colore e la posizione del pixel in quella posizione.

## Utilizzo dello strumento

Seguite questi passaggi per accedere e utilizzare lo strumento:

1. Fare clic sul pulsante ![](../../../assets/color-sampler-information-button.png) <b>Informazioni</b> nella barra degli strumenti della visualizzazione 2D per aprire l&#39;ancoraggio informazioni e la barra degli strumenti
1. Fai clic sul pulsante ![](../../../assets/color-sampler-tool-icon.png) <b>Strumento Sampler colori</b> nella barra degli strumenti Informazioni
1. Nella finestra della vista, fate clic sul pixel specifico da campionare per posizionare un ![](../../../assets/color-sampler-pin-icon.png) <b>pin</b>
1. Esaminare i valori campionati nella sezione dedicata del Dock informazioni
1. Al termine, fare clic sul pulsante ![](../../../assets/color-sampler-remove-pin.png) <b>Elimina</b> per rimuovere il pin dalla finestra della vista.\
   Puoi anche rimuovere il perno facendo clic su RMB e selezionando l&#39;azione &quot;Elimina&quot; nel menu di scelta rapida.

Ecco una dimostrazione dello strumento in azione:

![Campionatore colore: uso dello strumento](../../../assets/color-sampler-demo.gif "Campionatore colore: uso dello strumento"){zoomable="yes"}

*Fare clic per ingrandire*

+++Copiare i valori RGBA campionati
Potete copiare i valori campionati facendo clic su RMB sul pin e selezionando l’azione &quot;Copia valori RGBA&quot; nel menu di scelta rapida.

I valori copiati possono essere <b>incollati nei parametri utilizzando una miniatura di colore</b>.

Le miniature dei colori nel pannello Informazioni possono anche essere trascinate e rilasciate direttamente sulle miniature dei colori di tali parametri.

![Campionatore colore: copia valori RGBA](../../../assets/color-sampler-demo-copy-rgba-values.gif "Campionatore colore: copia valori RGBA"){zoomable="yes"}



*Fare clic per ingrandire*

+++

## Informazioni campionate

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Le informazioni sono raggruppate in tre tipi e due formati.

* <b>Valori campionati</b> memorizzati in ciascuno dei canali RGBA dell&#39;immagine:\
  Variabile\* / Virgola mobile
* <b>Colore campionato</b> nella rappresentazione HSV:\
  Numero intero a 8 bit / Virgola mobile
* <b>Posiziona</b> del pixel in numero di pixel e spazio dell&#39;immagine normalizzato:\
  Numero intero/virgola mobile

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Informazioni campionate](../../../assets/color-sampler-information.png "Informazioni campionate"){zoomable="yes"}

</td>
</tr>
</table>

Il valore dipende dalla profondità di bit utilizzata dall’immagine. In un grafico a Substance, la profondità di bit è controllata dal <b>Formato di output</b> [parametro di base](../../../compositing-graphs/graph-parameters/graph-parameters.md).

I valori di bit disponibili sono:

* <b>Numero intero a 8 bit:</b> 256 valori interi compresi tra 0 e 255.
* <b>Numero intero a 16 bit:</b> 65.536 valori interi compresi tra 0 e 65.535.
* <b>HDR a bassa precisione (16 bit)</b>: valore a virgola mobile codificato a 16 bit.
* <b>HDR ad alta precisione (32 bit)</b>: valore a virgola mobile codificato con 32 bit. Questa è la massima precisione disponibile in Designer.
