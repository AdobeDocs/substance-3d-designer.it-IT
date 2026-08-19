---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Da bitmap a luce materiale per convertire rapidamente le immagini bitmap in materiali con illuminazione ottimizzata per flussi di lavoro veloci.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Da bitmap a luce materiale
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Da bitmap a luce materiale

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## Da bitmap a luce materiale

**Ingresso:** *Filtri Materiale/1 Clic*

**Intermedio**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Questo nodo converte un singolo input Diffusione/Colore di base in un materiale completo. La semplice versione &quot;light&quot; di [Bitmap2Material di Allegorithmic, acquistabile separatamente](https://www.allegorithmic.com/products/bitmap2material), offre un assaggio della versione completa. Può funzionare bene per i casi più semplici.

Sebbene non sia garantito che si traduca in materiali perfetti e corretti per PBR, è un buon modo e veloce per iniziare se hai solo un&#39;immagine singola e desideri un materiale completo.

## Parametri

* **Canali**
  * Attiva e disattiva i canali di materiale in questo gruppo, ad esempio quando si utilizzano mappe Specular/lucidità anziché Metallico/Rugosità.
* **Globale**
  * **Bilanciamento Profondità**: *-1.0 - 1.0* Imposta un effetto di distorsione/spostamento per Heightmap.
* **Diffusione**
  * **Contrasta**: *0.0 - 1.0* Aggiunge nitidezza al risultato della diffusione.
  * **Tonalità**: *0,0 - 1,0* Le tonalità si diffondono con uno scostamento di tonalità selezionato dall&#39;utente.
  * **Saturazione**: *0.0 - 1.0* Modifica la saturazione del risultato Diffuso.
  * **Luminosità**: *0.0 - 1.0* Regola La Luminosità Diffusa Dei Risultati.
  * **Contrasto**: *-1,0 - 1,0*\
    Regola il contrasto del risultato.
* **Rilievo**\
  Il gruppo di Rilievi controlla sia l’output normale che quello di Height.
  * **Formato normale di output**: *DirectX, OpenGL* Alterna i formati normali (capovolge in verde).
  * **Inverti Rilievo generato**: *False/True* Inverte l&#39;interpretazione del height.
  * **Intensità normale**: *0.0 - 20.0* Imposta l&#39;intensità della mappa normale generata.
  * **Equalizzatore Rilievo**: *0.0 - 1.0* Imposta i saldi di conversione per scale di dettaglio diverse.
  * **Intensità pizzicore**: *0.0 - 1.0* Rende più nitide le transizioni normali. Aggiunge efficacemente un filtro di nitidezza prima di convertirlo in normale, rendendo i bordi più pronunciati.
  * **Nitidezza normale**: *0.0 - 1.0* Nitidezza Normalmap dopo la conversione, rende visibili i dettagli.
  * **Sfumatura normale**: *0.0 - 1.0* Sfuma Normalmap dopo la conversione e nasconde i dettagli.
* **Specular**
  * **Influenza diffusa Specular**: *0.0 - 1.0* Imposta l&#39;influenza della diffusione sullo Specular. Influisce anche sugli output di lucidità e rugosità.
  * **Saturazione Specular**: *0.0 - 1.0* Modifica la saturazione per l&#39;output dello Specular.
  * **Nitidezza Specular**: *0.0 - 1.0* Output Nitidezza Specular.
  * **Specular levei in**: *0.0 - 1.0* Imposta i livelli di input per l&#39;interpretazione degli Specular.
  * **Specular levei in uscita**: *0.0 - 1.0* Modifica i livelli di output dello Specular.
  * **Influenza Specular metallici**: *0.0 - 1.0* Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa degli Specular.
* **Lucentezza**
  * **Livelli di lucidità in**: *0.0 - 1.0* Imposta i livelli di input per l&#39;interpretazione di lucidità.
  * **Livelli di lucidità in uscita**: *0.0 - 1.0* Modifica i livelli di output di lucidità.
  * **Influenza lucidità metallica**: *0.0 - 1.0* Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa di lucidità.
* **Rugosità**
  * **Livelli di rugosità in**: *0.0 - 1.0* Imposta i livelli di input per l&#39;interpretazione della rugosità.
  * **Livelli di rugosità in uscita**: *0.0 - 1.0* Modifica i livelli di output della rugosità.
  * **Influenza rugosità metallica**: *0.0 - 1.0* Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa di lucidità.
* **Occlusione ambiente**
  * **Occlusione ambiente in modalità diffusa**: *0.0 - 1.0* Consente di creare fusioni di oggetti AO generati in output diffuso.
  * **Diffusione Occlusione ambiente**: *0.0 - 1.0* Imposta la distanza di diffusione dell&#39;oggetto AO generato.
  * **Distanza luce Occlusione ambiente**: *0.0 - 1.0* Imposta l&#39;interpretazione &quot;profondità&quot; di AO. Ha meno influenza quando c&#39;è una grande diffusione.
  * **Angolo luce Occlusione ambiente**: *0.0 - 1.0* Imposta l&#39;angolo di proiezione dell&#39;illuminazione dell&#39;ambiente. Può essere utilizzato per compensare qualsiasi AO direzionale già presente nella Diffusione, se impostato su un angolo opposto.
  * **Livelli Occlusione ambiente**: *0.0 - 1.0* Modifica i livelli di output di AO.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
