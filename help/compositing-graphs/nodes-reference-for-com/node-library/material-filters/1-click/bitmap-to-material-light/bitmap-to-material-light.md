---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# Da bitmap a luce materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

<b>In:</b> Filtri materiali > 1 Clic

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo nodo converte un singolo input Diffusione/Colore di base in un materiale completo. La semplice versione &quot;light&quot; di [Bitmap2Material di Allegorithmic, acquistabile separatamente](https://www.allegorithmic.com/products/bitmap2material), offre un assaggio della versione completa. Può funzionare bene per i casi più semplici.

Sebbene non sia garantito che si traduca in materiali perfetti e corretti per PBR, è un buon modo e veloce per iniziare se hai solo un&#39;immagine singola e desideri un materiale completo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attiva e disattiva i canali di materiale in questo gruppo, ad esempio quando si utilizzano mappe Specular/lucidità anziché Metallico/Rugosità. |
| <b>Globale</b> |  |
| <b>Saldo Profondità</b> <i>-1.0 - 1.0</i> | Imposta la distorsione/scostamento per la mappa altezza. |
| <b>Diffusione</b> |  |
| <b>Contrasta</b> <i>0.0 - 1.0</i> | Aggiunge nitidezza al risultato della diffusione. |
| <b>Tonalità</b> <i>0.0 - 1.0</i> | Tinta la diffusione con uno scostamento tonalità selezionato dall’utente. |
| <b>Saturazione</b> <i>0.0 - 1.0</i> | Modifica la saturazione del risultato della Diffusa. |
| <b>Luminosità</b> <i>0.0 - 1.0</i> | Regola la luminosità dei risultati delle Diffuse. |
| <b>Contrasto</b> <i>-1.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Rilievo</b> | Il gruppo di Rilievi controlla sia l’output normale che quello di Height. |
| <b>Formato Normale Di Output</b> <i>DirectX, OpenGL</i> | Passa da un formato Normale a un altro (capovolge il colore verde). |
| <b>Inverti Rilievo generato</b> <i>Falso/Vero</i> | Inverte l’interpretazione del height. |
| <b>Intensità normale</b> <i>0.0 - 20.0</i> | Imposta l&#39;intensità della mappa normale generata. |
| <b>Equalizzatore Rilievo</b> <i>0.0 - 1.0</i> | Imposta i saldi di conversione per scale di dettaglio diverse. |
| <b>Intensità pizzico</b> <i>0.0 - 1.0</i> | Rende più nitide le transizioni normali. Aggiunge efficacemente un filtro di nitidezza prima di convertirlo in normale, rendendo i bordi più pronunciati. |
| <b>Nitidezza normale</b> <i>0.0 - 1.0</i> | Nitidezza Normalmap dopo la conversione, rende visibili i dettagli. |
| <b>Sfumatura normale</b> <i>0.0 - 1.0</i> | Sfuma Normalmap dopo la conversione e nasconde i dettagli. |
| <b>Specular</b> |  |
| <b>Influenza Specular-Diffusa</b> <i>0.0 - 1.0</i> | Imposta l&#39;influenza della diffusione sullo Specular. Influisce anche sugli output di lucidità e rugosità. |
| <b>Saturazione Specular</b> <i>0.0 - 1.0</i> | Modifica la saturazione dell’output degli Specular. |
| <b>Nitidezza Specular</b> <i>0.0 - 1.0</i> | Rende più nitido l’output dello Specular. |
| <b>Specular levei In</b> <i>0.0 - 1.0</i> | Imposta i livelli di input per l’interpretazione degli Specular. |
| <b>Specular levei in uscita</b> <i>0.0 - 1.0</i> | Modifica i livelli di output dello Specular. |
| <b>Influenza Specular Metallico</b> <i>0.0 - 1.0</i> | Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa dello Specular. |
| <b>Lucentezza</b> |  |
| <b>Lucentezza livelli in</b> <i>0.0 - 1.0</i> | Imposta i livelli di input per l&#39;interpretazione della Lucentezza. |
| <b>Lucentezza livelli in uscita</b> <i>0.0 - 1.0</i> | Modifica i livelli di output della Lucentezza. |
| <b>Influenza Lucentezza Metallica</b> <i>0.0 - 1.0</i> | Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa Lucentezza. |
| <b>Rugosità</b> |  |
| <b>Livelli Di Rugosità In</b> <i>0.0 - 1.0</i> | Imposta i livelli di input per l’interpretazione della rugosità. |
| <b>Livelli di rugosità in uscita</b> <i>0.0 - 1.0</i> | Modifica i livelli di output della rugosità. |
| <b>Rugosità metallica influenza</b> <i>0.0 - 1.0</i> | Determina l&#39;influenza dell&#39;input metallico opzionale sulla mappa Lucentezza. |
| <b>Occlusione ambiente</b> |  |
| <b>Occlusione ambientale Nelle Diffuse</b> <i>0.0 - 1.0</i> | Fusioni in AO generato in output Diffusa. |
| <b>Occlusione ambientale pagine affiancate</b> <i>0.0 - 1.0</i> | Consente di impostare la distanza di diffusione dell’audio originale generato. |
| <b>Occlusione ambientale distanza luce</b> <i>0.0 - 1.0</i> | Imposta l’interpretazione &quot;profondità&quot; di AO. Ha meno influenza quando c&#39;è una grande diffusione. |
| <b>Occlusione ambientale angolo luce</b> <i>0.0 - 1.0</i> | Imposta l’angolo di dominante AO con illuminazione falsa. Può essere utilizzato per compensare qualsiasi AO direzionale già presente nella Diffusa, se impostato su un angolo opposto. |
| <b>Livelli Occlusione ambientale</b> <i>0.0 - 1.0</i> | Modifica i livelli di output AO. |
