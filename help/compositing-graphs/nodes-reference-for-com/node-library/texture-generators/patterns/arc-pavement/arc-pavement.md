---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilizzate il nodo Padiglione arco per generare pattern di pavimentazione a forma di arco per la creazione di texture di strade e tracciati curvi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arco pavimentazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# Arco pavimentazione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera un pattern di pavimentazione ad arco parigino. Questo effetto non può essere ottenuto con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)o [Affianca Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) standard, quindi questo nodo dedicato.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Scala</b> <i>1 - 8</i> | Imposta scala globale/Affiancamento. |
| <b>Quantità motivo</b> <i>1 - 32</i> | Imposta la quantità di mattoni utilizzata in ogni arco. |
| <b>Quantità motivo casuale</b> <i>0.0 - 1.0</i> | Rende casuale la quantità di mattoni in ogni arco. Ha l&#39;effetto di dare ai mattoni scale diverse. |
| <b>Quantità minima modello</b> <i>1 - 10</i> | Controlla la quantità minima di mattoni durante la randomizzazione degli archi. |
| <b>Quantità archi</b> <i>0 - 20</i> | Imposta la quantità di archi sovrapposti verticalmente. Cambia il height di mattoni. |
| <b>Pattern</b> <i>Immagine di input, Quadrato, Disco, Paraboloide, Campana, Gaussiano, Torace, Piramide, Mattone, Gradazioni, Onde, Mezza campana, Campana con dorso, Mezzaluna, Capsula, Cono</i> | Seleziona la forma del motivo da utilizzare. |
| <b>Filtro immagine di input</b> <i>Bilineare + Mipmap, Bilineare, Più Vicino</i> |  |
| <b>Scala pattern</b> <i>0.0 - 1.0</i> | Imposta la scala per ogni porzione. |
| <b>Larghezza motivo</b> <i>0.0 - 1.0</i> | Imposta la larghezza per ogni porzione. |
| <b>Height di pattern</b> <i>0.0 - 1.0</i> | Imposta il height per ogni porzione. |
| <b>Larghezza motivo casuale</b> <i>0.0 - 1.0</i> | Rende casuale la larghezza delle porzioni. |
| <b>Height di pattern casuale</b> <i>0.0 - 1.0</i> | Rende casuale il height di riquadri. |
| <b>Larghezza motivo globale casuale</b> <i>0.0 - 1.0</i> | Rende casuale la larghezza delle porzioni, senza creare spazi più ampi tra di esse. |
| <b>Diminuzione Height Motivo</b> <i>0.0 - 1.0</i> | Controlla la compressione del height di sezioni alla fine di ogni arco. |
| <b>Colore casuale</b> <i>0.0 - 1.0</i> | Rende casuali i colori delle porzioni. |
| <b>Non square expansion</b> <i>Falso/Vero</i> | Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/arcpavement-ex.png" />
        </td>
    </tr>
</table>
