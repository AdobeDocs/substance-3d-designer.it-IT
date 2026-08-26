---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Utilizza gli shader GLSLFX nella vista 3D di Substance 3D Designer per personalizzare il rendering del materiale e gli effetti di anteprima.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shader GLSLFX
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# Shader GLSLFX

I file GLSLFX creano un ponte tra l’applicazione e i file dello shader glsl.\
Consente di utilizzare qualsiasi shader glsl senza dover modificare il codice.

## Formato file

Il formato di file GLSLFX è un file XML. I commenti sono supportati.

### Intestazione e nodo principale

L&#39;elemento nodo radice XML è denominato <b>glslfx</b>.

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Corpo

#### Tecnica

Elemento XML che descrive una tecnica. Una tecnica è una variazione del FX corrente. Un GLSLFX può contenere più tecniche, ma è necessario definirne almeno una.

La geometria verrà renderizzata con una delle tecniche definite dall&#39;applicazione.

+++Definizione elemento XML
Tecnica <b>Name:</b>

<b>Attributi:</b>

* name: stringa utilizzata per denominare la tecnica

+++

L&#39;elemento XML può avere più elementi figlio. Gli elementi definiti in una tecnica hanno la precedenza su quelli definiti a livello globale.

Ad esempio, viene utilizzato per ignorare alcuni valori di uniformi e ottenere la variazione FX per questa tecnica.

#### Passata di rendering

Elemento XML che descrive un passaggio di rendering. Una passata di rendering descrive il rendering della geometria.

Una tecnica può contenere più passaggi di rendering che verranno eseguiti in sequenza. Una tecnica che non contiene passaggi di rendering equivale a una tecnica che contiene passaggi di rendering &quot;su schermo&quot;.

Gli elementi definiti in una passata di rendering hanno la precedenza su quelli definiti nella tecnica principale.

+++Definizione elemento XML
<b>Nome:</b> passaggio

<b>Attributi:</b>

* output

* fuori schermo: il rendering verrà eseguito nelle destinazioni di rendering definite dall’utente.

* su schermo: il rendering verrà eseguito nella destinazione di rendering predefinita

+++

#### Shader

Impostate i file dello shader GLSL per ogni tipo.

Definizione elemento XML:

+++Definizione elemento XML
Shader <b>Nome:</b>

<b>Attributi:</b>

* tipo: il tipo di shader GLSL;

* nome file: il percorso del file shader glsl. Può essere assoluto o relativo al file GLSLFX;

* primitiveType: il metodo per eseguire il rendering dell&#39;elemento di base.


| Valore &#39;type&#39; | Descrizione |
| --- | --- |
| vertice | Shader vertice |
| geometria | Shader geometria |
| tess\_control | Shader di controllo tassellatura |
| tess\_eval | Shader di valutazione tassellatura |
| frammento | Shader frammento |



| Valore &#39;primitiveType&#39; | Descrizione |
| --- | --- |
| punto | Rendering come punti |
| linelloop | Rendering come loop di linea |
| patch[1..N] | Esegui il rendering come patch con [1..N] vertici |


+++

#### Proprietà

Consentire di impostare parte dello stato OpenGL.

+++Definizione elemento XML
Proprietà <b>Nome:</b>

<b>Attributi:</b>

* name: il nome della proprietà da impostare. Il nome si basa sulla funzione OpenGL o sul nome glEnum:
  * Sintassi Enums: senza il prefisso &#39;GL\_&#39;, in minuscolo. Esempi: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;
  * Sintassi delle funzioni: senza il prefisso &#39;gl&#39;, in minuscolo e con tutte le parole separate dal carattere &#39;\_&#39;. Esempio: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* Sintassi Enums: senza il prefisso &#39;GL\_&#39;, in minuscolo. Esempi: glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;

* Sintassi delle funzioni: senza il prefisso &#39;gl&#39;, in minuscolo e con tutte le parole separate dal carattere &#39;\_&#39;. Esempio: glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* value: il valore della proprietà.


| Valori &#39;name&#39; | Valori di &#39;value&#39; | Descrizione |
| --- | --- | --- |
| blend\_enabled | booleano | Attivare/disattivare il metodo di fusione |
|  | true |  |
|  | falso |  |
| blend\_func | stringa, stringa | Impostare le funzioni di fusione delle origini e delle destinazioni |
|  | zero | per l’enumerazione OpenGL GL GL\_ZERO |
|  | uno | per OpenGL enum GL GL\_ONE |
|  | src\_color | per OpenGL enum GL GL\_SRC\_COLOR |
|  | one\_minus\_src\_color | per enum OpenGL GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | per OpenGL enum GL GL\_DST\_COLOR |
|  | one\_minus\_dst\_color | per enum OpenGL GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | per OpenGL enum GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | per enum OpenGL GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_alfa | per OpenGL enum GL GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | per enum OpenGL GL\_ONE\_MINUS\_DST\_ALPHA |
|  | costante\_colore | per OpenGL enum GL GL\_CONSTANT\_COLOR |
|  | one\_minus\_constant\_color | per enum OpenGL GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | costante\_alfa | per enum OpenGL GL GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | per enum OpenGL GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | per enum OpenGL GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | per OpenGL enum GL GL\_SRC1\_COLOR |
|  | one\_minus\_src1\_color | per enum OpenGL GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | per OpenGL enum GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | per enum OpenGL GL\_ONE\_MINUS\_SRC1\_ALPHA |
| cull\_face\_enabled | booleano | Attivare/disattivare l’eliminazione dei volti |
|  | true |  |
|  | falso |  |
| cull\_face\_mode | stringa | Impostare la modalità di taglio dei volti |
|  | primo piano | per enum OpenGL GL GL\_FRONT |
|  | retro | per enumerazione OpenGL GL GL\_BACK |
|  | front\_and\_back | per enum OpenGL GL\_FRONT\_AND\_BACK |
| profondità\_func | stringa | Impostare la funzione di confronto profondità |
|  | mai | per OpenGL enum GL GL\_NEVER |
|  | meno | per OpenGL enum GL GL\_LESS |
|  | lequal | per OpenGL enum GL GL\_LEQUAL |
|  | uguale | per enum OpenGL GL GL\_EQUAL |
|  | notequal | per enum OpenGL GL GL\_NOTEQUAL |
|  | gequal | per enum OpenGL GL GL\_GEQUAL |
|  | maggiore | per OpenGL enum GL GL\_GREATER |
|  | sempre | per OpenGL enum GL GL\_ALWAYS |


+++

#### Uniformi

Consente di ignorare alcune uniformi definite a livello globale o nella tecnica principale. Ciò consente di modificare il comportamento dello shader per questa tecnica o passaggio di rendering.

Per ulteriori dettagli sulla definizione delle <b>uniformi</b>, vedere la sezione seguente.

+++Esempio


+++

## Destinazioni rendering

Per i passaggi di rendering &quot;fuori schermo&quot;, è necessario definire le destinazioni di rendering nel passaggio di rendering.

+++Definizione elemento XML
<b>Nome:</b> output

<b>Attributi:</b>

* allegato: il punto di attacco OpenGL, ispirato ai nomi OpenGL:\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;colore[0..3]&#39;\
  GL\_PROFONDITÀ\_ATTACHMENT => &#39;profondità&#39;

allegato: il punto di attacco OpenGL, ispirato ai nomi OpenGL:\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;colore[0..3]&#39;\
GL\_PROFONDITÀ\_ATTACHMENT => &#39;profondità&#39;

* nome: il nome della destinazione di rendering.\
  Può essere utilizzato in un passaggio di rendering successivo per associare questa destinazione di rendering come campionatore.

nome: il nome della destinazione di rendering.\
Può essere utilizzato in un passaggio di rendering successivo per associare questa destinazione di rendering come campionatore.

* formato: il formato interno della destinazione di rendering.

formato: il formato interno della destinazione di rendering.

* clear: attributo facoltativo che definisce un valore clear.\
  Se presente, la destinazione di rendering verrà azzerata con questo valore all’inizio della passata di rendering.\
  Se mancante, la destinazione di rendering manterrà il contenuto precedente.

+++

>[!NOTE]
>
> Le destinazioni di rendering del colore non sono consentite in un passaggio di rendering &quot;su schermo&quot;, ma una destinazione di rendering della profondità può essere condivisa con qualsiasi passaggio di rendering (ma è probabile che interrompa il rendering quando si mixano più materiali nella scena).

<b>Informazioni sui formati</b>

Per i formati profondità, sono supportati tutti i formati OpenGL solo profondità (senza stencil):

* GL\_PROFONDITÀ\_COMPONENT16 => &#39;profondità 26&#39;
* GL\_PROFONDITÀ\_COMPONENT24 => &#39;profondità 34&#39;
* GL\_PROFONDITÀ\_COMPONENT32 => &#39;profondità 42&#39;
* GL\_PROFONDITÀ\_COMPONENT32F => &#39;profondità 42f&#39;

Per i formati colore, il nome è basato sui nomi enum OpenGL, senza il prefisso &#39;GL\_&#39;, in lettere minuscole.\
I formati a tre canali (RGB) non sono supportati. Utilizza invece un formato RGBA.\
Profondità di bit per canale supportato:

* Numero intero senza segno normalizzato: 8, 16
* Virgola mobile: 16, 32

Un&#39;eccezione a queste regole è il formato GL\_R11F\_G11F\_B10F, che è supportato.:

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### Campionatori

Se si consente di ignorare alcuni campionatori definiti a livello globale, questi non possono essere definiti in una tecnica. Ciò consente di definire un utilizzo del campionatore per questo passaggio di rendering o di leggere da una destinazione di rendering di un passaggio di rendering precedente.

Per ulteriori dettagli sulla definizione dei campionatori, vedere la sezione <b>Campionatori</b>.

+++Esempio


+++

## Formato vertice di input

Ciò consente di definire la semantica di ogni attributo definito nello shader dei vertici.

<b>Definizione elemento XML:</b>

Nome: &#39;vertexformat&#39;

Attributi:

* &#39;name&#39;: nome dell&#39;attributo definito nello shader del vertice.
* &#39;semantico&#39;: semantico dell&#39;attributo.

| Valore &#39;semantico&#39; | Descrizione |
| --- | --- |
| posizione | Posizione vertice (float3) |
| normale | Vertice normale (float3) |
| texcoord[0..N] | Buffer coordinate texture vertice N (float2) |
| tangente[0..N] | Buffer tangente vertice N (float4) |
| binormale[0..N] | Buffer binormale vertice N (float4) |

Esempio:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## Campionatori

Ciò consente di definire l’uso di ciascun campionatore.\
Viene utilizzato dall’applicazione per determinare la texture da impostare nei campionatori specificati.

<b>Definizione elemento XML:</b>

Nome: &#39;sampler&#39;

Attributi:

* &#39;name&#39;: il nome della variabile del campionatore nel file shader.
* &#39;utilizzo&#39;: utilizzo del campionatore. Corrisponde all’utilizzo specificato nel nodo Output del grafico.

| Valore &#39;usage&#39; | Descrizione |
| --- | --- |
| diffusione | Mappa diffusa |
| opacità | Mappa opacità |
| con emissioni | Mappa di emissione |
| ambientocclusione | Mappa occlusione ambiente |
| ambiente | Mappa ambiente |
| maschera | Mappa maschera |
| detailnormal | Dettagli mappa normale |
| normale | Mappa normale |
| rilievo | Mappa rilievo |
| height | Mappa height |
| spostamento | Spostamento mappa |
| specularlevel | Specular level mappa |
| specularcolor | Mappa colore Specular |
| specular | Specular mappa |
| lucentezza | Mappa lucidità |
| ruvidità | Mappa rugosità |
| anisotropilivello | Mappa del livello di antisotropia |
| anisotropiangolo | Mappa dell&#39;angolo dell&#39;antisotropia |
| trasmissivo | Mappa trasmissiva |
| riflesso | Mappa di riflessione |
| rifrazione | Mappa rifrazione |
| ambiente | Mappa ambiente (mappa cubo) |
| panorama | Mappa Panorama (Mappa Latitudine/Longitudine) |
| maschera blu | Una texture di dithering 256x256 |

* Sono supportati più utilizzi.
  * Esempio:

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;: valore booleano che indica se il campionatore deve essere visualizzato nell&#39;interfaccia grafica

* Esempio:

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


Modalità di disposizione:

<table data-preserve-html="true"><tbody><tr><th>Nome</th><th>Valore</th></tr><tr><td rowspan="4">texture_wrap_s, texture_wrap_t, texture_wrap_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">ripeti<br/><br/></td></tr></tbody></table>

Filtro Texture

<table data-preserve-html="true"><tbody><tr><th>Nome</th><th>Valore</th></tr><tr><td rowspan="6">texture_min_filter, texture_mag_filter<br/><br/><br/></td><td>più vicino</td></tr><tr><td>lineare</td></tr><tr><td colspan="1">nearest_mipmap_nearest</td></tr><tr><td colspan="1">linear_mipmap_nearest</td></tr><tr><td colspan="1">nearest_mipmap_linear</td></tr><tr><td colspan="1">linear_mipmap_linear</td></tr></tbody></table>

Esempio:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## Uniformi

Questo consente di aggiungere ulteriori informazioni sulle uniformi di ogni shader.

<b>Definizione elemento XML:</b>

Nome: &#39;uniforme&#39;

Attributi:

&#39;name&#39;: nome dell&#39;uniforme nel file shader.

| Valore &#39;semantico&#39; | Descrizione |
| --- | --- |
| mondo | Matrice mondo (float16) |
| worldinversetranspose | Matrice mondiale di trasposizione inversa (float16) |
| worldviewprojection | World View Projection Matrix (float16) |
| viewinverse | Matrice inversa mondiale (float16) |
| worldview | World View Matrix (float16) |
| modelview | Matrice vista modello (float16) |
| proiezione | Matrice di proiezione (float16) |
| ambiente | Colore ambiente scena (float3) |
| lightposition[0..N] | Posizione dell&#39;ennesima luce della scena (float3) |
| lightcolor[0..N] | Colore dell&#39;ennesima luce della scena (float3) |
| intensità luce[0..N] | Intensità dell&#39;ennesima luce della scena (a virgola mobile) |
| globaltime | Ora corrente in sec (a virgola mobile) |
| risoluzione | Risoluzione finestra vista (int2) |
| Topolino | Posizione del mouse (int2) |
| campionepostablesize | Numero di campioni da utilizzare per calcolare l’illuminazione ambientale (int) |
| irradianceshcoef | Matrice di vettori di armoniche sferiche (float3[10]) |
| panoramipmapheight | Numero di livelli mipmap nella mappa panoramica (a virgola mobile) |
| panorama | Angolo Angolo di rotazione della mappa panoramica (a virgola mobile) |
| intensità panoramica | Intensità della mappa panoramica (a virgola mobile) |
| computebinormalinfragmentshader | Il binormale viene calcolato per frammento? (se non per vertice) (bool) |
| isdirectxnormal | Il formato mappa normale è DirectX? (bool) |
| uvwscale | Valori di scala di u, v, w (float3) |
| renderuvtile | Esegui il rendering di 1 solo riquadro UV? (bool) |
| uvtilecoords | Coordinata della porzione UV da sottoporre a rendering (int2) |

&#39;semantico&#39;: semantico dell&#39;uniforme. Tutte le matrici sono float16.

Esempio:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


Esempio:

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### Altri parametri

Altre informazioni aggiuntive possono essere aggiunte a ciascuna uniforme per:

* definire il valore predefinito
* valori morsetto
* controllare la modalità di visualizzazione dell&#39;uniforme nell&#39;applicazione:
* impostare l&#39;etichetta
* imposta le informazioni del widget utilizzato per modificare il valore nell’applicazione:
* nome widget, min, max, incremento/decremento passaggio
* raggruppare le uniformi nei widget di gruppo

Poiché le uniformi possono essere sostituite per ogni tecnica, consente di visualizzare una configurazione GUI specifica per ogni tecnica.

<b>Definizione elemento XML:</b>

Nome: &#39;uniforme&#39;

Attributi:

* &#39;name&#39;: nome dell&#39;uniforme nel file shader.
* &#39;default&#39;: il valore predefinito uniforme
* &#39;min&#39;: valore minimo dell&#39;intervallo di validità
* &#39;max&#39;: valore massimo dell&#39;intervallo di validità
* &#39;guiName&#39;: il nome dell&#39;uniforme nell&#39;interfaccia grafica dell&#39;applicazione
* &#39;guiGroup&#39;: nome del gruppo da inserire nell&#39;interfaccia utente grafica dell&#39;applicazione
* &#39;guiWidget&#39;: nome del widget utilizzato per modificare il valore uniforme nell&#39;interfaccia utente grafica dell&#39;applicazione

| Valore &#39;guiWidget&#39; | Descrizione |
| --- | --- |
| Cursore di | Widget cursore per floatN |
| angolo | Widget Angolo per float |
| colore | Widget Colore per colore float3, float4 |
| casella di controllo | Widget CheckBox per bool |

* &#39;guiMin&#39;: valore minimo del widget
* &#39;guiMax&#39;: valore massimo del widget

## Esempio: tassellatura/parallasse

### File Shader Vertice Parallasse

Disponibile in .\tessellation\_parallax\parallax\vs.glsl

Contenuto:

> #version 120

attributo vec4 iVS\_Position;\
attributo vec4 iVS\_Normal;\
attributo vec2 iVS\_UV;\
attributo vec4 iVS\_Tangent;\
attributo vec4 iVS\_Binormal;

variazione vec3 iFS\_Normal;\
variazione vec2 iFS\_UV;\
variazione vec3 iFS\_Tangent;\
variabile vec3 iFS\_Binormal;\
variazione vec3 iFS\_PointWS;

matrice uniforme mat4 worldMatrix;\
matrice uniforme mat4 worldViewProjMatrix;

void main()\
&lbrace;\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_Binormal = iVS\_Binormal.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
&rbrace;

### File dello shader del vertice di tassellatura

Disponibile in .\tessellation\_parallax\tessellation\vs.glsl

Contenuto:

&#x200B;>> 

&#x200B;#version 120

attributo vec4 iVS\_Position;\
attributo vec4 iVS\_Normal;\
attributo vec2 iVS\_UV;\
attributo vec4 iVS\_Tangent;\
attributo vec4 iVS\_Binormal;

variazione di vec4 oVS\_Normal;\
variazione di vec2 oVS\_UV;\
variabile vec4 oVS\_Tangent;\
variabile vec4 oVS\_Binormal;

void main()\
&lbrace;\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_Tangent = iVS\_Tangent;\
oVS\_Binormal = iVS\_Binormal;\
&rbrace;

### File dello shader di controllo della tassellatura

Disponibile in .\tessellation\_parallax\tessellation\tcs.glsl

Contenuto:

&#x200B;>> 

&#x200B;#version 400 core\
&#x200B;#extension GL\_ARB\_tessellation\_shader : attiva

layout(vertici = 3) out;

in vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

Fattore di tassellatura del galleggiante uniforme;

void main()\
&lbrace;\
gl\_TessLevelOuter[0] = tassellationFactor;\
gl\_TessLevelOuter[1] = tassellationFactor;\
gl\_TessLevelOuter[2] = tassellationFactor;\
gl\_TessLevelInner[0] = tassellationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
TCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
&rbrace;

### File dello shader di valutazione della tassellatura

Disponibile in .\tessellation\_parallax\tessellation\tcs.glsl

Contenuto:

&#x200B;>> 

&#x200B;#version 400 core

layout(triangoli, uguale\_spaziatura, ccw) in;

in vec4 oTCS\_Normal[];\
in vec2 oTCS\_UV[];\
in vec4 oTCS\_Tangent[];\
in vec4 oTCS\_Binormal[];

matrice uniforme mat4 worldMatrix;\
matrice uniforme mat4 worldViewProjMatrix;

Uniform Sampler2D heightMap;

piastrellatura a virgola mobile uniforme = 1,0 f;\
altezza mobile uniformeMapScale = 1.0f;

out vec3 iFS\_Normal;\
out vec2 iFS\_UV;\
out vec3 iFS\_Tangent\
out vec3 iFS\_Binormal;\
out vec3 iFS\_PointWS;

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
&lbrace;\
restituire uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
&rbrace;

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
&lbrace;\
restituire uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
&rbrace;

void main()\
&lbrace;\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw));\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTexSample = texture(heightMap, newUV \&#42; affiancamento).x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42; affiancamento;\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
&rbrace;

### File Shader frammento

Disponibile in .\tessellation\_parallax\fs.glsl

Contenuto:

&#x200B;>> 

&#x200B;#version 120

// #define ALG\_NORMAL\_DIRECTX\
&#x200B;#define ALG\_NORMAL\_OPENGL

&#x200B;#ifdef ALG\_NORMAL\_DIRECTX\
// RIFLETTI #define\_NORMALE\_X\
&#x200B;#define RIFLETTI\_NORMALE\_Y\
// #define RIFLETTI\_NORMALE\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_DIRECTX

&#x200B;#ifdef ALG\_NORMAL\_OPENGL\
// RIFLETTI #define\_NORMALE\_X\
&#x200B;#define RIFLETTI\_NORMALE\_Y\
// #define RIFLETTI\_NORMALE\_Z\
&#x200B;#endif //#ifdef ALG\_NORMAL\_OPENGL

variazione vec3 iFS\_Normal;\
variazione vec2 iFS\_UV;\
variazione vec3 iFS\_Tangent;\
variabile vec3 iFS\_Binormal;\
variazione vec3 iFS\_PointWS;

lampada uniforme vec30Pos = vec3(0.0f,0.0f,70.0f);\
uniforme vec3 Lamp0Color = vec3(1.0f,1.0f,1.0f);\
lampada uniforme vec31Pos = vec3(70.0f,0.0f,0.0f);\
uniforme vec3 Lamp1Color = vec3(0.198f,0.198f,0.198f);\
bool flipNormal uniforme = true;\
TilingDetail float uniforme = 3.0f;\
SpecExpon a virgola mobile uniforme = 50,0;\
float uniforme Ks = 1,0;\
int parallax uniforme\_mode = 0;\
Fattore di tassellatura del galleggiante uniforme = 4,0;\
altezza mobile uniformeMapScale = 1.0f;\
profondità float uniforme\_detail = 0,5f;\
float uniforme Kr = 0,5f;\
int uniforme KF\_on = 1;\
flottante uniforme KF = 1,0f;\
colore uniforme vec3 Ambi = vec3(0,07f,0,07f,0,07f);\
piastrellatura a virgola mobile uniforme = 1,0 f;\
int enableTilingInFS uniforme = 0;

Uniform Sampler2D heightMap;\
sample2D normalMap uniforme;\
Uniform sampler2D detailNormalMap;\
emissiveMap del campionatore uniforme2D;\
common sampler2D diffusoMap;\
uniformesampler2D specularMap;\
uniformecampionatore2D opacityMap;\
Uniform samplerCube environmentMap;

matrice uniforme mat4 worldMatrix;\
matrice uniforme mat4 worldInverseTransposeMatrix;\
matrice uniforme mat4 viewInverseMatrix;

vec4 litFct(float NdotL, float NdotH, float specExp)\
&lbrace;\
ambiente flottante = 1,0;\
diffusione a virgola mobile = max(NdotL, 0,0);\
specular float = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
ritorno vec4(ambiente, diffusione, specular, 1,0);\
&rbrace;

vec3 lerpFct(vec3 v0, vec3 v1, percentuale variabile)\
&lbrace;\
return v0 + (v1-v0) \&#42; percento;\
&rbrace;

// Ombreggiatura Phong\
void phong\_ombreggiature(\
in vec3 LightColor\
in vec3 normalWS,\
in vec3 pointToLightDirWS,\
in vec3 pointToCameraDirWS,\
inout vec3 DiffuseContrib\
inout vec3 SpecularContrib)\
&lbrace;\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
&rbrace;

vec3 fixNormalSample(vec3 v)\
&lbrace;\
risultato vec3 = v - vec3(0,5,0,5,0,5);

&#x200B;#ifdef RIFLETTI\_NORMALE\_X\
risultato.x = -risultato.x;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_X\
&#x200B;#ifdef RIFLETTI\_NORMALE\_Y\
risultato.y = -risultato.y;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Y\
&#x200B;#ifdef FLIP\_NORMAL\_Z\
result.z = -result.z;\
&#x200B;#endif // ifdef FLIP\_NORMAL\_Z

risultato di ritorno;\
&rbrace;

vec3 normalVecOSToWS(vec3 normale)\
&lbrace;\
ritorno normale;\
&rbrace;

void main()\
&lbrace;\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalizza(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_Tangent);\
vec3 binormalOS = normalize(iFS\_Binormal);

// ------------------------------------------\
// Accertarsi che il TBN sia ortonorizzato\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumululatedNormalOS = normalOS;

// ------------------------------------------\
// Aggiorna UV\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0? iFS\_UV : (iFS\_UV \&#42; affiancamento);\
height a virgola mobile = texture2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tassellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
+= uv (height \&#42; s.xy \&#42; parallasse) ;

// ------------------------------------------\
// Aggiungi normale da normalMap\
vec3 normalTS = texture2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumululatedNormalOS = cumululatedNormalOS + normalMapOS;\
cumululatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
// Aggiungi normalmap dei dettagli\
vec3 normalDetailTS = texture2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,Profondità\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumululatedNormalOS = cumululatedNormalOS + normalDetailOS;\
cumululatedNormalOS = normalize(cumulatedNormalOS);

if (lunghezza(normaleTS)&lt;0,0001)\
cumululatedNormalOS = normalOS;

vec3 cumululatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// Calcola diffusione e Specular

// Contributo leggero 0\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_ombreggiatura(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

// Contributo leggero 1\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_ombreggiatura(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffusaColor = texture2D(diffusaMap,uv);

vec3 specularColor = texture2D(specularMap,uv).rgb;\
vec3 R = reflection(pointToCameraDirWS,cumululatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl;

if (KF >= 0,0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS))),0)\&#42;KF\_on;\
else\
FallofRefl = (1-max((((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS)))),0))\&#42;KF\_on;

if (KF\_su == 0)\
FallofRefl=1,0;

vec3 Ambiant\_final = diffusoColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = texture2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
&#x200B;+ specularColor\&#42;specContrib\
&#x200B;+ diffusioneColor.rgb\&#42;diffContrib\
&#x200B;+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
&#x200B;+ emissivo;

// Colore finale\
vec4 finalColor4 = vec4(finalcolor, texture2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
&rbrace;

### File GLSLFX

Il file glslfx definisce due tecniche per il rendering della geometria:

* Uno utilizza la tecnica di tassellatura hardware
* L’altro si basa su un effetto parallasse che verrà utilizzato come failback se l’hardware dell’utente non supporta la tassellatura.

Disponibile in .\tessellation\_parallax\fs.glsl

Contenuto:

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
