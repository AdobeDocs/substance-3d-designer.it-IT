---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Utilizzate il nodo Affianca casuale per creare pattern di riquadri casuali con variazioni procedurali per gli effetti di texture organica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Affianca casuale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# Affianca casuale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random-01.png){width="128px"}

<b>In:</b> Generatori > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Porzione Casuale genera un motivo di porzione procedurale che presenta un po&#39; più di caos nelle forme della porzione rispetto alla sua controparte, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Lo fa dividendo casualmente alcune porzioni in porzioni più piccole. Ti consigliamo di trovare prima il modo di aggirare il Tile Generator prima di affrontare Tile Random, come molti concetti sono simili.

Affianca casuale viene utilizzato al posto di [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) quando l&#39;obiettivo è un modello meno organizzato e dall&#39;aspetto più vecchio. Tuttavia, presenta dei limiti, quindi [Affianca Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) per qualsiasi altra esigenza avanzata.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input pattern</b> <i>Input in scala di grigi (input colore)</i> | Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;. |
| <b>Input in background</b> <i>Input scala di grigi (input colore)</i> |  |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>X importo</b> <i>1 - 64</i> | Quantità di ripetizioni X del pattern. |
| <b>Importo Y</b> <i>1 - 64</i> | Quantità di ripetizioni Y del pattern. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |
| <b>Pattern</b> |  |
| <b>Pattern</b> <i>Input pattern, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazione, Onde, Mezza campana, Campana Ridotta, Mezzaluna, Capsula, Cono</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Filtro input immagine (motore > v4)</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> |  |
| <b>Specifico per pattern</b> <i>0.0 - 1.0</i> | Consente di modificare la forma del motivo selezionato. L’effetto dipende dal pattern selezionato. |
| <b>Casuale specifico per pattern</b> <i>0.0 - 1.0</i> | L’effetto di randomizzazione dipende dal pattern selezionato. |
| <b>Rotazione</b> <i>0, 90, 180, 270, orizzontale casuale, verticale casuale</i> | Imposta la rotazione su intervalli di 90 gradi, con possibilità di randomizzazione. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Aggiunge una rotazione libera casuale. |
| <b>Simmetria casuale</b> <i>0.0 - 1.0</i> | Riflette casualmente alcuni pattern in base alla modalità Simmetria casuale selezionata. Più alto è questo valore, maggiore sarà il mirroring dei pattern. |
| <b>Simmetria modalità casuale</b> <i>Orizzontale + Verticale, Orizzontale, Verticale</i> | Determina il comportamento di mirroring quando Simmetria casuale è maggiore di 0. |
| <b>Dividere</b> |  |
| <b>Modalità</b> <i>nessuno, automatico, automatico orizzontale, automatico verticale, casuale h+v</i> | Imposta la regola per la divisione delle porzioni. |
| <b>Soglia</b> <i>0.0 - 1.0</i> | Soglia di dimensione per quando dividere una porzione. |
| <b>Moltiplicatore</b> <i>0 - 10</i> | Moltiplicatore di divisione. Più alto è questo valore, maggiori saranno le divisioni. |
| <b>Dimensioni</b> |  |
| <b>Casuale X</b> <i>0.0 - 1.0</i> | Rende casuale il ridimensionamento non uniforme sull’asse X. |
| <b>A caso</b> <i>0.0 - 1.0</i> | Rende casuale il ridimensionamento non uniforme sull’asse Y. |
| <b>Interstizio</b> |  |
| <b>Modalità</b> <i>Rispetto al mattone più piccolo, rispetto al mattone più grande</i> | Imposta l&#39;interstizio della dimensione del mattone rispetto a. |
| <b>Importo</b> <i>0.0 - 1.0</i> | Imposta le dimensioni dello spazio tra i mattoni. |
| <b>Forma</b> |  |
| <b>Scala</b> <i>0.0 - 1.0</i> | Ridimensiona globalmente ogni porzione. |
| <b>Scala casuale</b> <i>0.0 - 1.0</i> | Ridimensionamento casuale su base per porzione. |
| <b>Rotazione</b> <i>0.0 - 1.0</i> | Rotazione globale per ogni riquadro. |
| <b>Rotazione casuale</b> <i>0.0 - 1.0</i> | Ruota in modo casuale su base per porzione. |
| <b>Vincolo di rotazione</b> <i>Falso/Vero</i> | Vincola la scala in modo che le porzioni ruotate non si sovrappongano mai. |
| <b>Posizione</b> |  |
| <b>Scostamento</b> <i>0.0 - 1.0</i> | Sposta o converte le porzioni a livello globale, scorre solo sull’asse X |
| <b>Scostamento casuale</b> <i>0.0 - 1.0</i> | Rende casuale lo scostamento per porzione, scivola solo sull’asse X |
| <b>Casuale</b> <i>0.0 - 1.0</i> | Rende casuale la posizione e le porzioni si spostano sugli assi X e Y. |
| <b>Vincoli casuali</b> <i>Falso/Vero</i> | Vincola la scala in modo che le porzioni si tocchino, ma non si sovrappongano. Attenua significativamente l’effetto Posizione casuale. |
| <b>Colore</b> |  |
| <b>Colore</b> <i>(valore scala di grigi) / (valore colore)</i> | Imposta il colore uniforme per tutte le porzioni. |
| <b>Colore casuale</b> <i>0.0 - 1.0</i> | Rende casuale il colore per porzione. |
| <b>Parametrizzazione colore</b> <i>nessuno, area, dimensione x, dimensione y</i> | Rende la variazione del colore dipendente da una di queste impostazioni. |
| <b>Intensità parametrizzazione colore</b> <i>0.0 - 1.0</i> | Moltiplicatore per l&#39;effetto di parametrizzazione sopra riportato. |
| <b>Effetto di parametrizzazione del colore (solo per il colore)</b> <i>RGB+Alpha, solo RGB, solo Alpha</i> | Determina l&#39;effetto di parametrizzazione solo colore. |
| <b>Colore di sfondo</b> <i>(valore scala di grigi) / (valore colore)</i> | Imposta il colore di sfondo in tinta unita. |
| <b>Metodo fusione</b> <i>Aggiungi/Sotto, Max / Aggiungi/Sotto, Fusione Alpha (Colore)</i> | Imposta il metodo di fusione per le porzioni sullo sfondo. |
| <b>Maschera</b> |  |
| <b>Casuale</b> <i>0.0 - 1.0</i> | Inizia a caso a mascherare le porzioni. Più alto è il valore, più porzioni scompaiono. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte il risultato della maschera. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-02.png" />
        </td>
    </tr>
</table>
