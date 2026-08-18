---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Utilizza il nodo Rendering volume texture 3D per eseguire il rendering delle texture volumetriche dai dati 3D per creare effetti cloud e nebbia.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rendering volume texture 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# Rendering volume texture 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**Ingresso:** *Filtro/Effetto*

**Semplice**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrizione

Il nodo **Rendering volume texture 3D** esegue il rendering del volume di una forma descritta da una *texture 3D*, utilizzando il corrispondente *campo distanza con segno* dall&#39;input dell&#39;immagine **3D Signed distance field**.

Il volume è rappresentato entro i limiti di un *cubo di unità*. L&#39;illuminazione viene calcolata utilizzando *luce direzionale* e un *lucernario emisferico*.

>[!NOTE]
>
> Il campo distanza con segno deve essere una texture **4096x4096** che descrive la forma con una griglia **16x16** di 256 sezioni.\
> È possibile utilizzare il nodo [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) per calcolare il campo distanza con segno per una texture 3D di 256 sezioni.

</td>
</tr>
</table>

## Parametri

### Input

* **Signed distance field 3D** *Scala Di Grigi*\
  Immagine 4096x4096 che rappresenta le 256 *sezioni* di un *campo distanza con segno* di una forma, disposta in una griglia 16x16.\
  È possibile utilizzare il nodo [3D Texture SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) per calcolare il campo distanza con segno per una texture 3D di 256 sezioni.
* **Densità** *Scala Di Grigi*\
  Immagine 4096x4096 che rappresenta le 256 *sezioni* della *densità* di una forma, disposta in una griglia 16x16. La densità viene mappata usando valori in scala di grigio da 0 (completamente trasparente) a 1 (interamente opaco).\
  Per generare una maschera di volume come texture 3D di 256 sezioni potete utilizzare [maschera di volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) o nodi di disturbo 3D ([disturbo di Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [frattale con rilievi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) e così via), combinati con un nodo [posizione texture 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) come input di posizione.

### Parametri

* **Risoluzione output** *Numero intero2*\
  La risoluzione dell&#39;immagine di output in **X** e **Y**, espressa come *potenza di due*.
* **Posizione fotocamera** *Mobile2*\
  La posizione della videocamera attorno alla forma.\
  Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella **vista 2D** per *orbita* della fotocamera.
* **Posizione Chiara** *Float2*\
  Posizione della *luce direzionale* attorno alla forma.\
  Quando il nodo è selezionato, è possibile utilizzare il gizmo posizione nella **vista 2D** per *orbita* della sorgente luminosa.
* **Distanza fotocamera** *Mobile*\
  La distanza tra la fotocamera e la forma.
* **Fotocamera FOV** *Mobile*\
  Il campo visivo della fotocamera in *gradi*.
* **Assorbimento** *Mobile*\
  Regola la quantità di luce assorbita mentre passa *attraverso* il volume.
* **Sfumatura** *Mobile*\
  Moltiplica il valore fornito dall&#39;input **Densità** con il valore del campo distanza *interna*.\
  In questo modo la larghezza della *sfumatura di dissolvenza* viene regolata in modo efficace dal limite esterno del volume verso l&#39;interno.
* **Metodo colore chiaro** *Numero intero*\
  Consente di impostare il metodo di acquisizione del colore della luce direzionale:
  * *Temperatura (Kelvin)*: il colore è il risultato della temperatura della luce, dove un valore *inferiore* produce un colore *più caldo*
  * *Colore RGB*: definisci il colore utilizzando i valori RGB
* **Temperatura leggera (Kelvin)** *Fluttuazione*\
  Temperatura della luce direzionale che influisce sul *colore*. Un valore *inferiore* produce un colore *più caldo*.\
  Valori utili:\
  1800 K - Candela\
  2800 K - Lampada a incandescenza\
  5500 K - Luce diurna\
  6200 K - Bianco naturale\
  7000 K - Cielo coperto\
  *Nota*: questo parametro è disponibile solo quando **Metodo colore chiaro** è impostato su *Temperatura (Kelvin)*.
* **Colore chiaro** *Float3*\
  Colore della luce direzionale.\
  *Nota*: questo parametro è disponibile solo quando **Metodo colore chiaro** è impostato su *Colore RGB*.
* **Intensità luce** *Mobile*\
  Intensità della luce direzionale.
* **Colore ambiente** *Float3*\
  Il colore del lucernario ambiente.
* **Intensità ambiente** *Mobile*\
  Intensità del lucernario ambiente.
* **Albedo** *Float3*\
  Colore di albedo del volume.
* **Modalità sfondo** *Numero intero*\
  Metodo di ombreggiatura dello sfondo della scena sottoposta a rendering, basato sul **colore di sfondo**:
  * *Ombreggiato*: il colore è influenzato dal *colore* e dalla *intensità* della luce direzionale - *colore costante*: il colore viene applicato in modo uniforme *indipendentemente* dalla luce direzionale
* **Colore di sfondo** *Float4*\
  Il colore usato per riempire lo sfondo della scena sottoposta a rendering.
* **Dithering** *Mobile*\
  Regola l’intensità del *dithering blu del disturbo* utilizzato per attenuare l’ombreggiatura.
* **Abilita piano terreno** *Booleano*\
  Quando *True*, esegue il rendering di un piano terreno *infinito*. Il *cubo di unità* che racchiude la forma si trova su questo piano.
* **Piano infinito** *Booleano*\
  Imposta il piano terreno in modo che si estenda *all&#39;infinito* fino all&#39;orizzonte.\
  *Nota*: questo parametro è disponibile solo quando il parametro **Abilita piano terreno** è impostato su *True*.
* **Dimensioni piano terreno** *Float2* Regola le dimensioni del piano terreno.\
  *Nota*: questo parametro è disponibile solo se il parametro **Abilita piano terreno** è impostato su *True* e il parametro **Piano infinito** è impostato su *False*.

## Immagini di esempio

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
