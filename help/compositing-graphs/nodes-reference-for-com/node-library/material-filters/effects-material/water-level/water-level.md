---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Utilizzare il nodo Livello acqua per unire i materiali in base al height del livello dell'acqua per creare effetti realistici sull'acqua.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Livello dell'acqua
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Livello dell&#39;acqua

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## Livello dell&#39;acqua

**Ingresso:** *Filtri/Effetti Materiale*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Effetto all-in-one che aggiunge un livello dell&#39;acqua a un input di materiale completo. Affinché l’effetto funzioni, il materiale di input deve avere una mappa di altezza di buona qualità. Il risultato è corretto per PBR.

## Parametri

### Input

* **Maschera**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.

### Parametri

* **Canali**\
  Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Livello dell&#39;acqua**: *0.0 - 1.0* Controllo principale per aumentare o ridurre il livello dell&#39;acqua.
* **Oscurità dell&#39;acqua**: *0.0 - 1.0* Imposta la &quot;trasparenza&quot; generale dell&#39;acqua.
* **Umidità bordi**: *0.0 - 1.0* Determina l&#39;aspetto bagnato che devono avere i bordi dell&#39;acqua.
* **Distanza bagnata bordi**: *0.0 - 1.0* Imposta la distanza dei bordi bagnati.
* **Entità sfocatura Profondità**: *0,0 - 1,0* Imposta la quantità di sfocatura in base alla profondità sotto l’acqua. Modifica il raggio di sfocatura.
* **Opacità sfocatura Profondità**: *0.0 - 1.0* Determina la quantità di sfocatura della profondità che viene fusa, che può essere utilizzata per ridurre l’effetto della sfocatura.
* **Colore fango**: *(Valore colore)*Imposta il colore dell&#39;effetto fango.
* **Profondità dei fanghi**: *0.0 - 1.0* Imposta la profondità in corrispondenza della quale i fanghi iniziano ad apparire, rispetto al livello dell&#39;acqua.
* **Opacità fango**: *0.0 - 1.0* Imposta l&#39;opacità globale dell&#39;effetto fango.
* **Gelo**: *0.0 - 1.0* Imposta la quantità di gelo. Inizia a comparire dai bordi esterni e si sposta verso l’interno.
* **Intensità gelo**: *0.0 - 1.0* Imposta l&#39;intensità del gelo e controlla l&#39;&quot;opacità&quot; dell&#39;effetto.
* **Crepe di gelo**: *0,0 - 1,0* Imposta la quantità di crepe nelle transizioni da congelato a liquido.
* **Formato Frost Normal**: *DirectX/OpenGL* Scambia il canale verde dell’effetto Frost Normalmap.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
