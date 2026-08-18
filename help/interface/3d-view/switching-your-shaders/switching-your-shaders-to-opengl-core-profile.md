---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Scopri come passare dagli shader al profilo OpenGL Core nella vista 3D di Substance 3D Designer per compatibilità e prestazioni.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Passaggio degli shader al profilo OpenGL Core
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# Passaggio degli shader al profilo OpenGL Core

A partire dalla versione 2018.2.0, la finestra della vista 3D utilizza OpenGL Core Profile.\
In questa occasione, abbiamo aggiornato alcuni shader forniti con l&#39;applicazione da GLSL versione 120 a GLSL versione 330.

Potete aggiornare i vostri shader per sfruttare le nuove funzioni GLSL disponibili o per rendere il vostro codice GLSL più moderno. Tieni presente che su MacOS i vecchi shader potrebbero non funzionare più.\
Per una panoramica completa delle nuove funzioni, consigliamo vivamente di consultare la documentazione ufficiale di OpenGL. È possibile, ad esempio, esaminare la specifica [OpenGL Ombreggiature Language 3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf).\
Altrimenti, ecco una guida rapida che vi aiuterà a convertire i vostri shader GLSL 1.20 in GLSL 3.30:

## Aggiornare il numero di versione

Prima di tutto, sostituisci (o aggiungi il file nella parte superiore se non lo hai ancora) la tua precedente direttiva `#version` di `#version 330`.

### Sostituisci &quot;attributo&quot; e &quot;variabile&quot; con &quot;attacco&quot; o &quot;stacco&quot;

Ora, le variabili `attribute` e `varying` sono dichiarate in modo esplicito come `in` o `out` a seconda dello stadio dello shader:

Nello shader dei vertici, `attribute` dei vertici vengono dichiarati come `in`, mentre `varying` da passare allo shader dei frammenti vengono dichiarati come `out`.\
Ad esempio:

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


diventa:

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


Analogamente, nello shader del frammento, l’opzione variabile diventa attiva. È inoltre necessario dichiarare una variabile out che sostituirà gl\_FracColor (che non è più incorporata):

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


diventa:

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### Usare le nuove funzioni di ricerca delle texture

Con la nuova versione del linguaggio di ombreggiatura, l’API di ricerca delle texture è stata semplificata e migliorata.

Le funzioni `texture1D()`, `texture2D()`, `texture3D()` e `textureCube()` diventano tutti overload di `texture()`.\
Analogamente `texture2DLod()` diventa `textureLod()`, `texture2DGrad()` diventa `textureGrad()` e così via.

Ora puoi anche accedere a funzioni utili come `textureSize()` (per eseguire una query sulle dimensioni del campionatore in texel), `textureOffset()` (per campionare i vicini della posizione di destinazione), `textureFetch()` (per fornire una posizione di esempio in pixel) e altro ancora.
