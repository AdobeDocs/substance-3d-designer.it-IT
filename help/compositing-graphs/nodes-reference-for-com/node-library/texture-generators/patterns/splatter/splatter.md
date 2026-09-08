---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Usa il nodo Splatter per creare forme dispersioni tra texture per creare pattern casuali e dettagli di texture organiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schizzo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# Schizzo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Splatter è un generatore di pattern destinato al posizionamento casuale di un input mappa. Dispone di molti controlli per il posizionamento con motivi geometrici ed è più semplice da usare rispetto a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Quest&#39;ultimo può ottenere risultati simili, ma è molto più complesso.

Lo splatter è utile per ottenere rapidamente alcune forme stampate verso il basso, senza bisogno di troppe modifiche.

Tieni presente che i parametri di splatter predefiniti non sembrano affatto casuali: è necessario modificarne alcuni per ottenere la randomizzazione (principalmente i parametri di Disturbo). Tieni inoltre presente che per funzionare è necessario un input mappa.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Larghezza dimensione pattern</b> <i>0.0 - 1000.0</i> | Numero di serie da utilizzare sull&#39;asse X. |
| <b>Height dimensioni pattern</b> <i>0.0 - 1000.0</i> | Numero di serie da utilizzare sull&#39;asse Y. |
| <b>Rotazione</b> <i>-360.0 - 360.0</i> | Ruota ogni pattern di un valore impostato. |
| <b>Variazione rotazione</b> <i>0.0 - 360.0</i> | Introduce una rotazione casuale per ogni forma separata. |
| <b>Zoom</b> <i>100.0 - 10000.0</i> | Ridimensiona il risultato finale. Tenete presente che questo rompe Affiancamento! |
| <b>Guadagno</b> <i>0.0 - 10.0</i> | Regola il guadagno di fusione di ogni pattern. Le fa risaltare di più. |
| <b>Panning X</b> <i>-100.0 - 100.0</i> | Esegue il panning dell&#39;intero risultato sull&#39;asse X. |
| <b>Panning Y</b> <i>-100.0 - 100.0</i> | Esegue il panning dell&#39;intero risultato sull&#39;asse Y. |
| <b>Disturbo</b> <i>0.0 - 100.0</i> | Sposta le forme a caso. |
| <b>Numero griglia</b> <i>0 - 8</i> | Passa da una dimensione all’altra della griglia per regolare la scala dei risultati. Mantiene Affiancamento. |
| <b>Angolo disturbo</b> <i>0.0 - 360.0</i> | Controlla l’angolo di spostamento del disturbo. |
| <b>Disturbo casuale</b> <i>Falso/Vero</i> | Rende casuale l&#39;angolo del disturbo, aggiungendo molto più caos. |
| <b>Dimensione motivo</b> <i>5 - 12</i> |  |
| <b>Variazione dimensioni</b> <i>0.0 - 100.0</i> | Introduce il ridimensionamento casuale per ogni forma. |
| <b>Filtro input immagine (solo motore > v4)</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> | Quali filtri applicare all&#39;immagine di input? |
| <b>Livello Di Output Min</b> <i>0.0 - 1.0</i> | Regolazione del livello minimo. |
| <b>Livello di output massimo</b> <i>0.0 - 1.0</i> | Regolazione del livello massimo. |
| <b>Colore di sfondo</b> <i>(valore scala di grigi)</i> | Imposta il colore di sfondo in tinta unita. |
| <b>Variazione luminanza</b> <i>0.0 - 1.0 (solo versione in scala di grigio)</i> | Introduce la variazione della luminanza. |
| <b>Variazione colore</b> <i>0.0 - 1.0 (Solo Versione A Colori)</i> | Introduce variazioni di colore. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/splatter-ex.gif" />
        </td>
    </tr>
</table>
