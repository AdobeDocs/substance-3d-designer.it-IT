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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Livello dell&#39;acqua

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

<b>Tra:</b> Filtri materiali > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Effetto all-in-one che aggiunge un livello dell&#39;acqua a un input di materiale completo. Affinché l’effetto funzioni, il materiale di input deve avere una mappa di altezza di buona qualità. Il risultato è corretto per PBR.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Livello dell&#39;acqua</b> <i>0.0 - 1.0</i> | Comando principale per aumentare o ridurre il livello dell&#39;acqua. |
| <b>Acqua scura</b> <i>0.0 - 1.0</i> | Imposta la &quot;trasparenza&quot; generale dell&#39;acqua. |
| <b>Umidità bordi</b> <i>0.0 - 1.0</i> | Determina il grado di umidità dei bordi dell’acqua. |
| <b>Distanza bagnata bordi</b> <i>0.0 - 1.0</i> | Imposta il valore raggiunto dai bordi bagnati. |
| <b>Profondità quantità sfocatura</b> <i>0.0 - 1.0</i> | Imposta la quantità di sfocatura in base alla profondità sotto l’acqua. Modifica il raggio di sfocatura. |
| <b>Opacità sfocatura Profondità</b> <i>0.0 - 1.0</i> | Determina la quantità di sfocatura profondità da utilizzare per ridurre l’effetto della sfocatura. |
| <b>Colore fango</b> <i>(valore colore)</i> | Consente di impostare il colore dell’effetto fango. |
| <b>Profondità dei fanghi</b> <i>0.0 - 1.0</i> | Imposta la profondità in corrispondenza della quale inizia a comparire il fango, rispetto al livello dell&#39;acqua. |
| <b>Opacità fango</b> <i>0.0 - 1.0</i> | Imposta l’opacità globale dell’effetto fango. |
| <b>Ghiaccio</b> <i>0.0 - 1.0</i> | Imposta la quantità di gelo. Inizia a comparire dai bordi esterni e si sposta verso l’interno. |
| <b>Intensità gelo</b> <i>0.0 - 1.0</i> | Imposta l’intensità del gelo, controlla l’&quot;opacità&quot; dell’effetto. |
| <b>Crepe da gelo</b> <i>0.0 - 1.0</i> | Imposta la quantità di crepe nelle transizioni da congelato a liquido. |
| <b>Formato Frost Normal</b> <i>DirectX/OpenGL</i> | Alterna il canale verde dell’effetto Frost Normalmap. |
