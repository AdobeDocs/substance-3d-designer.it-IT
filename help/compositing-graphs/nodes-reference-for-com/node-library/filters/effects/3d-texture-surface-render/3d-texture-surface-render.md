---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Utilizzate il nodo Rendering superficie texture 3D per eseguire il rendering delle texture di superficie dai dati 3D per creare effetti di superficie procedurali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering superficie texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# Rendering superficie texture 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**Ingresso:** *Filtro/Effetto*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rendering superficie texture 3D** esegue il rendering della superficie di una forma descritta da una *texture 3D*, utilizzando il corrispondente *campo distanza* dall&#39;input dell&#39;immagine **Campo distanza 3D**.

La superficie è rappresentata entro i limiti di un *cubo di unità*. L&#39;illuminazione viene calcolata utilizzando l&#39;immagine di input **Ambiente** mappata su una sfera infinita.

>[!NOTE]
>
> Il campo distanza dovrebbe essere una texture **4096x4096** che descrive la forma con una griglia **16x16** di 256 sezioni.\
> È possibile utilizzare il nodo [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) della texture 3D per calcolare il campo distanza per una texture 3D di 256 sezioni.

</td>
</tr>
</table>

## Parametri

### Input

* **Campo Distanza 3D** *Scala Di Grigi*\
  Immagine 4096x4096 che rappresenta le 256 *sezioni* del *campo distanza* di una forma, disposta in una griglia 16x16.\
  È possibile utilizzare il nodo [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) della texture 3D per calcolare il campo distanza per una texture 3D di 256 sezioni.
* **Ambiente** *Colore*\
  Immagine che rappresenta l&#39;*ambiente*, che deve essere mappata a una sfera infinita nel rendering e utilizzata per calcolare l&#39;*illuminazione*.\
  L&#39;immagine viene utilizzata anche per eseguire il rendering dello sfondo della scena quando il parametro **Modalità sfondo** è impostato su *Ambiente* o *Ambiente*.

### Parametri

* **Risoluzione output** *Numero intero2*\
  La risoluzione dell&#39;immagine di output in **X** e **Y**, espressa come *potenza di due*.
* **Posizione fotocamera** *Mobile2*\
  La posizione della videocamera attorno alla forma.\
  Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella **vista 2D** per *orbita* della fotocamera.
* **Distanza fotocamera** *Mobile*\
  La distanza tra la fotocamera e la forma.
* **Fotocamera FOV** *Mobile*\
  Il campo visivo della fotocamera in *gradi*.
* **Albedo** *Float3*\
  Colore di albedo della superficie della forma.
* **Modalità sfondo** *Numero intero*\
  Metodo di rappresentazione dello sfondo della scena sottoposta a rendering:
  * *Irradianza terreno*: irradianza calcolata del piano terreno
  * *Ambiente*: il colore ambiente dell&#39;input dell&#39;immagine **Ambiente** è mappato su una sfera infinita, simile a una versione fortemente sfocata dell&#39;immagine
  * *Colore uniforme*: riempi in modo uniforme lo sfondo con un colore specificato
  * *Ambiente*: input immagine **Ambiente** mappato a una sfera infinita
* **Colore di sfondo** *Float4*\
  Il colore utilizzato per riempire in modo uniforme lo sfondo della scena sottoposta a rendering.\
  *Nota*: questo parametro è disponibile solo quando **Modalità sfondo** è impostato su *Colore uniforme*.
* **Abilita piano terreno** *Booleano*\
  Se *True*, esegue il rendering di un piano terreno. Il *cubo di unità* che racchiude la forma si trova su questo piano.
* **Piano infinito** *Booleano*\
  Imposta il piano terreno in modo che si estenda *all&#39;infinito* fino all&#39;orizzonte.\
  *Nota*: questo parametro è disponibile solo quando il parametro **Abilita piano terreno** è impostato su *True*.
* **Dimensioni piano terreno** *Float2* Regola le dimensioni del piano terreno.\
  *Nota*: questo parametro è disponibile solo se il parametro **Abilita piano terreno** è impostato su *True* e il parametro **Piano infinito** è impostato su *False*.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
