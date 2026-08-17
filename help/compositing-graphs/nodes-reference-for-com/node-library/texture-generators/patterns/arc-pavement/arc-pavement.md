---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Utilizzate il nodo Pavimentazione arco per generare pattern di pavimentazione a forma di arco per creare texture di strade e tracciati curvi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arco pavimentazione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Arco pavimentazione

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## Arco pavimentazione

**Ingresso:** *Generatori Di Texture**/Pattern*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera un pattern di pavimentazione ad arco parigino. Questo effetto non può essere ottenuto con [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)o [Affianca Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) standard, quindi questo nodo dedicato.

## Parametri

* **Scala**: *1 - 8* Imposta scala/porzioni globali.
* **Entità motivo**: *1 -* 32\
  Imposta la quantità di mattoni utilizzata in ogni arco.
* **Quantità motivo casuale**: *0,0 - 1,0*\
  Rende casuale la quantità di mattoni in ogni arco. Ha l&#39;effetto di dare ai mattoni scale diverse.
* **Quantità Minima Pattern**: *1 - 10*\
  Controlla la quantità minima di mattoni durante la randomizzazione degli archi.
* **Quantità archi**: *0 - 20*\
  Imposta la quantità di archi sovrapposti verticalmente. Cambia il height di mattoni.
* **Pattern**: *Immagine di input, Quadrato, Disco, Paraboloide, Campana, Gaussiana, Torace, Piramide, Mattone, Gradazioni, Onde, Mezza campana, Campana Ridotta, Crescente, Capsula, Cono*\
  Seleziona la forma del motivo da utilizzare.
* **Filtro delle immagini di input**: *Bilineare + Mipmap, Bilineare, Più vicino*
* **Scala pattern**: *0.0 - 1.0* Imposta la scala per ogni porzione.
* **Larghezza motivo**: *0,0 - 1,0*\
  Imposta la larghezza per ogni porzione.
* **Height di pattern**: *0,0 - 1,0*\
  Imposta il height per ogni porzione.
* **Larghezza motivo casuale**: *0,0 - 1,0*\
  Rende casuale la larghezza delle porzioni.
* **Height di pattern casuale**: *0,0 - 1,0*\
  Rende casuale il height di riquadri.
* **Larghezza motivo globale casuale**: *0.0 - 1.0* Rende casuale la larghezza delle porzioni, senza creare spazi più ampi tra di esse.
* **Diminuzione Height pattern**: *0.0 - 1.0* Controlla la compressione del height di sezioni alla fine di ogni arco.
* **Colore casuale**: *0,0 - 1,0*\
  Rende casuali i colori delle porzioni.
* **Non square expansion**: *Falso/Vero*\
  Consente la compensazione di schiacciamento e allungamento con rapporti non quadrati.

## Immagini di esempio

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
