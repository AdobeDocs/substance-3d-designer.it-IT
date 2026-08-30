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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# Weathering dei tessuti

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fabric-weathering.resources/fabric-weathering.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Meteo

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Si tratta di un effetto di materiale completo che funziona su più canali contemporaneamente. Aggiunge un effetto di usura casuale del tessuto, con controllo per l&#39;età e la sporcizia.<br>Questo effetto non funziona molto bene a meno che non si disponga di mappe AO e World Space Normalmap eseguite i baking correttamente collegate, in quanto richiede queste mappe per calcolare e generare tutto in modo adeguato.

Assicurati di aver compreso appieno le [modalità di creazione dei collegamenti](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) quando lavori con i materiali completi.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> | Mappa con baking utilizzata per effetti interni e mascheratura. |
| <b>Spazio Normale Del Mondo</b> <i>Input colore</i> |  |
| <b>Maschera</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. Può essere attivato/disattivato con il parametro &quot;Maschera&quot;. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Canali</b> | Attivate e disattivate i canali del materiale in questo gruppo, ad esempio quando utilizzate mappe Specular/lucidità invece di Metallico/Rugosità. |
| <b>Avanzate</b> |  |
| <b>Formato Normale</b> <i>DirectX, OpenGL</i> | Passa da un formato Normalmap a un altro (inverte il canale verde). |
| <b>Maschera</b> <i>Falso/Vero</i> | Attiva o disattiva l’uso della mappa maschera. |
| <b>Effetto</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | Fusione un effetto dust più scuro, basato sulle aree rivolte verso l’alto nella mappa normale di World Space. |
| <b>Irritazione</b> <i>0.0 - 1.0</i> | Fusioni di un effetto dirt/sfumino globale, basato principalmente sulle aree occluse (scure) nell’oggetto principale. |
| <b>Indossamento bordi</b> <i>0.0 - 1.0</i> | Aggiunge ai bordi un effetto di nitidezza/intensificazione basato su Materiale normale. |
| <b>Utilizzato</b> <i>0.0 - 1.0</i> | Fusioni in dirt accumulato molto scuro in pieghe, basato su AO. I valori Massimo e Minimo tendono a essere molto estremi, utilizzali con cautela. |
| <b>Età</b> <i>0.0 - 1.0</i> | Fusioni su un modello di usura Affiancamento globale. Il controllo soglia sottostante controlla l’influenza AO. I valori massimo e minimo tendono a essere molto estremi. |
| <b>Soglia di validità</b> <i>0.0 - 1.0</i> | Imposta l’entità dell’influenza dell’AO sul parametro Age. |
| <b>Pieghe Di Età</b> <i>0.0 - 1.0</i> | Controlla la fusione di sottili pieghe aggiuntive nell’effetto Età. |
| <b>Scala Scratches bordi netti</b> <i>1.0 - 32.0</i> | Imposta la scala dei piccoli graffi, che eliminano principalmente l’effetto Usato ed Età. |
| <b>Intensità alterazione Scratches bordi netti</b> <i>0.0 - 1.0</i> | Imposta l’intensità dell’alterazione per i piccoli graffi di cui sopra. |
| <b>Desaturazione precedente dell&#39;infrastruttura</b> <i>0.0 - 1.0</i> | Controlla la desaturazione dell’effetto Età. |
| <b>Luminosità vecchio tessuto</b> <i>0.0 - 1.0</i> | Controlla la luminosità dell’effetto Età. *Si tratta di un parametro molto importante da modificare per ottenere l&#39;aspetto desiderato, ma i risultati possono essere estremi: utilizzare con modifiche secondarie.* |
| <b>Fusione</b> |  |
| <b>Intensità Diffusa</b> <i>0.0 - 1.0</i> | Intensità di fusione della Diffusione. |
| <b>Intensità Colore di base</b> <i>0.0 - 1.0</i> | Intensità di fusione del colore di base. |
| <b>Intensità normale</b> <i>0.0 - 1.0</i> | Intensità di fusione del normale. |
| <b>Intensità Specular</b> <i>0.0 - 1.0</i> | Forza di fusione dello Specular. |
| <b>Intensità Lucentezza</b> <i>0.0 - 1.0</i> | Forza di fusione della lucidità. |
| <b>Intensità rugosità</b> <i>0.0 - 1.0</i> | Forza di fusione della rugosità. |
| <b>Intensità Occlusione ambientale</b> <i>0.0 - 1.0</i> | Intensità di fusione dell’Occlusione ambiente. |
| <b>Intensità Height</b> <i>0.0 - 1.0</i> | Forza di fusione del Height. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fabric-weathering.resources/fabric-ex.gif" />
        </td>
    </tr>
</table>
