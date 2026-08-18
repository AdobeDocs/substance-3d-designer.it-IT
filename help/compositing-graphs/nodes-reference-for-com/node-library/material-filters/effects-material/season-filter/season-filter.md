---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Utilizza il nodo Filtro stagione per applicare effetti stagionali ai materiali per creare variazioni in primavera, estate, autunno e inverno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtro stagione
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Filtro stagione

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## Filtro stagione

**Ingresso:** *Filtri/Effetti Materiale*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo aggiunge effetti come livello dell&#39;acqua animato, neve, ghiaccio e/o muschio.

Tenete presente che si tratta di un filtro meno recente che non deve essere completamente corretto da PBR. Viene conservato principalmente per motivi preesistenti/di compatibilità, anche se in alcuni casi può ancora essere utile. Le versioni più recenti corrette per PBR sono disponibili in [Copertina Snow](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e [Livello acqua](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

Il nodo richiede un corretto insieme di input di materiale, principalmente con una Heightmap o Normalmap decentemente dettagliata.

## Parametri

### Input

* **Maschera** : *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;.

### Parametri

* **Canali**
  * Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità.
* **Avanzate**
  * **Formato normale**: *DirectX, OpenGL*\
    Passa da un formato Normalmap a un altro (inverte il canale verde).
  * **Maschera**: *False/True*\
    Attiva o disattiva l’uso della mappa maschera.
  * **Intensità luce**: *0,0 - 1,0*\
    Intensità della luce (simulata).
  * **Angolo luce**: *0,0 - 1,0*\
    Angolo di incidenza della luce (simulata)
* **Effetto**
  * **Effetto da Height o Normale**: *Height, Normale* Scegli quale mappa di input determina gli effetti.
  * **Livello dell&#39;acqua**: *0.0 - 1.0* Aumenta o riduce il livello dell&#39;acqua in base alle informazioni di Height/Normale.
  * **Dettagli acqua**: *0.0 - 1.0* Imposta la quantità di dettagli nell&#39;acqua.
  * **Rifrazione**: *0.0 - 1.0* Imposta la quantità di rifrazione falsa nell&#39;effetto.
  * **Riflessione**: *0.0 - 1.0* Imposta la quantità di riflesso falso nell&#39;effetto.
  * **Distanza di riflessione**: *0.0 - 1.0* Controlla gli elementi visivi di riflessione.
  * **Angolo Di Riflessione**: *0.0 - 1.0* Controlla Gli Elementi Visivi Di Riflessione.
  * **Direzione flusso**: *0.0 - 1.0* Controlla il flusso dell&#39;animazione (utilizzare Substance Player per visualizzare).
  * **Ghiaccio**: *0.0 - 1.0* Imposta il grado di congelamento dell&#39;acqua.
  * **Dettagli ghiaccio**: *0.0 - 1.0* Imposta la quantità di dettagli nel ghiaccio.
  * **Snow**: *0.0 - 1.0* Imposta la quantità di copertura innevata.
  * **Moss**: *0.0 - 1.0* Imposta la quantità di copertura del muschio.
  * **Scala Moss**: *1 - 4* Imposta la scala della texture del muschio generata.
  * **Colore Moss**: *(Valore colore)*Imposta il colore del muschio.
  * **Colore acqua**: *(Valore colore)*Imposta il colore dell&#39;acqua, inclusa l&#39;alfa/opacità.
* **Fusione**
  * **Intensità diffusione**: *0,0 - 1,0*\
    Intensità di fusione della Diffusione.
  * **Intensità colore di base**: *0,0 - 1,0*\
    Intensità di fusione del colore di base.
  * **Intensità normale**: *0,0 - 1,0*\
    Intensità di fusione del normale.
  * **Intensità Specular**: *0,0 - 1,0*\
    Forza di fusione dello Specular.
  * **Intensità lucidità**: *0,0 - 1,0*\
    Forza di fusione della lucidità.
  * **Intensità rugosità**: *0,0 - 1,0*\
    Forza di fusione della rugosità.
  * **Intensità Occlusione ambiente**: *0,0 - 1,0*\
    Intensità di fusione dell’Occlusione ambiente.
  * **Intensità Height**: *0,0 - 1,0*\
    Forza di fusione del Height.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
