---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Utilizza il nodo Leather Weathering per aggiungere modelli di usura ed effetti di invecchiamento ai materiali in pelle in base alla curvatura della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Agenti meteorologici in pelle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Agenti meteorologici in pelle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## Agenti meteorologici in pelle

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Aggiunge un effetto casuale di usura della pelle, con controllo per l&#39;età e la sporcizia. È simile a [Weathering tessuto](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md), ma ottimizzato specificamente per il cuoio.\
Questo effetto non funziona molto bene a meno che tu non abbia correttamente baked AO e World Space Normalmaps collegate, in quanto richiede questi per calcolare e generare adeguatamente tutto.

Assicurati di aver compreso appieno le [modalità di creazione dei collegamenti](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes) quando lavori con i materiali completi.

## Parametri

### Input

* **Occlusione ambiente**: *Input scala di grigi*\
  Mappa con baking utilizzata per effetti interni e mascheratura.
* **Spazio Mondiale Normale**: *Input Colore*
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
* **Effetto**
  * **Dust**: *0.0 - 1.0* Le sfumature si fondono in un effetto dust più scuro, in base alle aree rivolte verso l&#39;alto nella mappa normale di World Space.
  * **Sporcizia**: *0.0 - 1.0* Fusioni in un effetto dirt/sfumino globale, basato principalmente sulle aree occluse (scure) nell&#39;oggetto principale.
  * **Indossamento bordi**: *0.0 - 1.0* Aggiunge un effetto di nitidezza/intensificazione ai bordi, in base a Normale materiale.
  * **Usato**: *0.0 - 1.0* Si fonde in un aspetto in pelle usurato globale.
  * **Età**: *0.0 - 1.0* Si fonde con un aspetto in pelle usurata in pieghe basate su AO. Il posizionamento è influenzato molto da Age Treshold.
  * **Soglia età**: *0.0 - 1.0* Imposta la soglia di aspetto per l&#39;effetto Età.
  * **Scala Crepe**: *1.0 - 16.0* Imposta la profondità del cuoio usurato dall&#39;effetto Usato ed Età.
  * **Intensità alterazione Crepe**: *0.0 - 1.0* Imposta l’intensità della pelle usurata dall’effetto Usato ed Età.
  * **Scala Scratches bordi netti**: *1.0 - 32.0*
  * **Intensità alterazione bordi netti**: *0,0 - 1,0* Scratches
  * **Desaturazione pelle usata**: *0.0 - 1.0* Imposta la saturazione dell&#39;aspetto in pelle usurata dagli effetti Età e Usato.
  * **Luminosità pelle usata**: *0.0 - 1.0* Imposta la luminosità dell&#39;aspetto in pelle usurata dagli effetti Età e Usato.
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
