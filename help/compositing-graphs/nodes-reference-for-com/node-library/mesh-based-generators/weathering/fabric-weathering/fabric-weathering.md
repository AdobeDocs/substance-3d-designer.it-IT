---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: Utilizzare il nodo Weathering tessuto per aggiungere effetti di usura e invecchiamento ai materiali in tessuto in base alla geometria e alla curvatura della trama.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Weathering dei tessuti
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---


# Weathering dei tessuti

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

## Weathering dei tessuti

**Ingresso:** *Generatori Basati Su Trama**/Meteorizzazione*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Aggiunge un effetto di usura casuale del tessuto, con controllo per l&#39;età e la sporcizia.\
Questo effetto non funziona molto bene a meno che tu non abbia correttamente baked AO e World Space Normalmaps collegato, poiché richiede questi per calcolare e generare adeguatamente tutto.

Assicurati di aver compreso appieno le [modalità di creazione dei collegamenti](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) quando lavori con i materiali completi.

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
  * **Utilizzato**: *0.0 - 1.0* Fusioni in dirt accumulato molto scuro in pieghe, in base a AO. I valori Massimo e Minimo tendono a essere molto estremi, utilizzali con cautela.
  * **Età**: *0.0 - 1.0* Fusioni su un modello di usura di affiancatura globale. Il controllo soglia sottostante controlla l’influenza AO. I valori massimo e minimo tendono a essere molto estremi.
  * **Soglia di validità**: *0.0 - 1.0* Imposta l&#39;estensione con cui l&#39;oggetto AO influisce sul parametro Age.
  * **Pieghe di età**: *0.0 - 1.0* Controlla la fusione di sottili pieghe aggiuntive nell&#39;effetto Età.
  * **Scala Scratches bordi netti**: *1.0 - 32.0* Imposta la scala dei piccoli graffi, che eliminano principalmente l&#39;effetto Usato ed Età.
  * **Intensità alterazione bordi netti**: *0.0 - 1.0* Imposta l&#39;intensità dell&#39;alterazione per i piccoli graffi sopra riportati.
  * **Desaturazione vecchio tessuto**: *0.0 - 1.0* Controlla la desaturazione dell&#39;effetto Età.
  * **Luminosità vecchio tessuto**: *0.0 - 1.0* Controlla la luminosità dell&#39;effetto Età. *Si tratta di un parametro molto importante da modificare per ottenere l&#39;aspetto desiderato, ma i risultati possono essere estremi: utilizzare con modifiche secondarie.*
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

![](../../../../../../assets/fabric-ex.gif)

</td>
</tr>
</table>
