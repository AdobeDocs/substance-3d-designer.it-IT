---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill.html"
breadcrumb-title: ''
description: Utilizzate il nodo di Flood Fill per riempire le aree connesse di colore simile per la creazione di maschere e gli effetti di elaborazione delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 1%

---


# Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill.resources/flood-fill-01.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Flood Fill fa parte di un set avanzato di effetti che consente di aggiungere molta più variazione a una texture di base di tessere binarie. Non è pensato per essere usato da solo: è piuttosto un punto di partenza per altri effetti di Flood Fill. La separazione dei dati consente un flusso di lavoro più dinamico, ottimizzato e meno distruttivo.

Gli altri effetti Flood Fill sono [da Flood Fill a sfumatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), [da Flood Fill a colore/scala di grigi](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-grayscale-col/flood-fill-to-grayscale-color.md), [da Flood Fill a scala di grigi casuale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), [da Flood Fill a colore casuale](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-color/flood-fill-to-random-color.md), [da Flood Fill a dimensione casella BB](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-bbox-size/flood-fill-to-bbox-size.md), [da Flood Fill a posizione](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-position/flood-fill-to-position.md), [Mappatura Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-mapper/flood-fill-mapper.md) e [da Flood Fill a indice](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-index/flood-fill-to-index.md)

>[!WARNING]
>
> La mappa di input deve essere adatta al Flood Fill per funzionare. Idealmente si tratta di una mappa binaria (solo bianco/nero, senza scala di grigi) in cui ogni porzione è separata dalle altre da un bordo nero (0,0,0) per ogni pixel. Un esempio di candidato perfetto per questo è il [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).
> 
> I problemi si verificano se le porzioni non sono separate da pixel neri interi, in genere quando si utilizzano valori in scala di grigi e inclinati. È possibile identificare questo fenomeno in base a una mancanza complessiva di valori rossi nel risultato e a possibili strane linee di artefatti. In questi casi, regolate il contrasto sulla mappa di input o disattivate la mappa di input. Modificare l&#39;impostazione di compensazione Sicurezza/Velocità per verificare eventuali miglioramenti.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Compensazione tra sicurezza e velocità</b> <i>Forme semplici o piccole, forme complesse o grandi, nessuna modalità di errore.</i> | Impostare la modalità di calcolo più adatta alle forme di input. Consente risultati molto più precisi se si sceglie la modalità corretta. |
| <b>Opzioni avanzate</b> <i>Visualizzazione parametri avanzati e output/Nascondi parametri avanzati e output</i> |  |
| <b>Sostituire il compromesso sicurezza/velocità</b> <i>-1 - 100</i> | Visibile solo se sono attivate le opzioni avanzate. Consente di sostituire le feature interne. Molto avanzato, serve per creare effetti o debug propri. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill.resources/flood-fill-03.png" />
        </td>
    </tr>
</table>

Buoni e cattivi esempi di risultati dal Flood Fill.
