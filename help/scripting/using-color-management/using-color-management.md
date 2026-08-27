---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Scoprite come utilizzare le funzioni di gestione del colore nello scripting Substance 3D Designer Python per colori precisi.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilizzo della gestione colore
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# Utilizzo della gestione colore

La classe </b>SDColorManagementEngine <b>, accessibile dalla classe <b>SDApplication</b>, contiene informazioni sulle *impostazioni correnti di gestione del colore*.

## Accesso al motore di gestione dei colori ed esecuzione di query

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


È inoltre possibile *assegnare spazi colore* alle risorse bitmap da Python.

### Impostazione degli spazi colore nelle risorse bitmap

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## Scrittura di texture SDT con conversioni di spazio colore

Il metodo **save** della classe **SDTexture** ora accetta un parametro **outputColorSpace** facoltativo. Quando specificato, la conversione dello spazio colore verrà applicata *prima del salvataggio dell&#39;immagine*.

Se la modalità di gestione del colore supporta i profili ICC incorporati *e*, anche il formato del file di destinazione li supporta, il profilo ICC dello spazio colore sarà *incorporato nel file di immagine risultante*.
