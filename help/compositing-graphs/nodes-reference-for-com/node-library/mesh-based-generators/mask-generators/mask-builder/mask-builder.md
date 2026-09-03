---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/mask-builder.html"
breadcrumb-title: ''
description: Utilizza il nodo Crea maschera per combinare più input di maschera e creare pattern di maschera complessi per effetti di materiale.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Mask Builder
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Generatore maschera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 10%

---


# Generatore maschera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mask-builder.resources/mask-builder-01.png){width="128px"}

<b>In:</b> Generatori Basati Su Trama > Generatori di maschere

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Si tratta più o meno della versione Designer di Painter Mask Builder.

Si tratta di uno strumento complicato inteso come un generatore di maschere onnicomprensivo, basato su mappe con baking, parametri utente e pattern e mappe grunge. È principalmente inteso come un nodo molto avanzato, pieno controllo per fondere in piega dirt e usura dei bordi. Questo nodo è abbastanza potente da simulare ogni altro generatore di maschere.

Nessun bakes è esplicitamente richiesto, ma più fornisci, più questo nodo è in grado di fare.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Occlusione ambiente</b> <i>Input scala di grigi</i> |  |
| <b>Curvatura</b> <i>Input scala di grigi</i> |  |
| <b>Spazio globale normale</b> <i>Input colore</i> |  |
| <b>Input Grunge</b> <i>Input scala di grigi</i> |  |
| <b>Input Grunge 2</b> <i>Input scala di grigi</i> |  |
| <b>Input Dispersione</b> <i>Input scala di grigi</i> | Timbro dispersione personalizzato, necessario per utilizzare i parametri della Dispersione. |
| <b>Maschera (facoltativo)</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per mascherare gli effetti del nodo. |
| <b>Posizione</b> <i>Input colore</i> | Utilizzato per gli effetti Triplanari e Dall&#39;alto in basso. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Livello</b> <i>0.0 - 1.0</i> | Imposta il livello totale dell’effetto, rivelandolo gradualmente. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto del risultato. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte il risultato. Utile per ottenere l’opposto della maschera che state creando. |
| <b>Usa Triplanare</b> <i>Falso/Vero</i> | Consente la proiezione triplanare, evitando cuciture con mappe di grungi. |
| <b>Contrasto di fusione triplanare</b> <i>0.0 - 1.0</i> | Imposta il contrasto per la fusione triplanare. |
| <b>Grunge</b> <i>0.0 - 1.0</i> | Imposta la quantità di Grunge da fondere in tutto il mondo. |
| <b>Grunge</b> |  |
| <b>Scala</b> <i>0 - 10</i> | Imposta la scala della Grunge globale. |
| <b>Usa Grunge personalizzata</b> <i>Falso/Vero</i> | Abilita l&#39;input Grunge personalizzato. |
| <b>Grunge personalizzata secondaria</b> <i>0.0 - 1.0</i> | Abilita un secondo input di Grunge personalizzato. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte la mappa della Grunge. |
| <b>AO</b> <i>-1.0 - 1.0</i> | Imposta l’entità dell’effetto nelle aree AO occluse. Può essere modificato con il gruppo seguente. |
| <b>AO</b> |  |
| <b>Intervallo</b> <i>0.0 - 1.0</i> | Imposta la soglia o l&#39;intervallo per l&#39;aspetto di dirt. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto dell’effetto AO. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Imposta la quantità di disturbo/grunge da fondere nell’effetto AO. |
| <b>Scala disturbo</b> <i>0 - 10</i> | Consente di impostare la scala del disturbo/grunge dell’operatore aereo. |
| <b>Tipo di disturbo</b> <i>Macchie, Nuvole, Umidità, Disturbo Bianco</i> | Consente di passare da un tipo di rumore di tipo AO a un altro. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte l’interpretazione della mappa AO: appariranno disturbi in aree AO luminose, non scure. |
| <b>Curvatura</b> <i>0.0 - 1.0</i> | Consente di impostare l’effetto che deve apparire sui bordi della curvatura; può essere sia convessa che concava. Modificate questa impostazione con il gruppo sottostante. |
| <b>Curvatura</b> |  |
| <b>Intervallo convesso</b> <i>-1.0 - 1.0</i> | Consente di impostare l’effetto che dovrà essere applicato ai bordi convessi (chiari) della curvatura. |
| <b>Contrasto convesso</b> <i>0.0 - 1.0</i> | Imposta il contrasto dell’effetto Convesso. |
| <b>Inversione convessa</b> <i>Falso/Vero</i> | Inverte l’interpretazione dei bordi convessi. |
| <b>Intervallo concavo</b> <i>-1.0 - 1.0</i> | Consente di impostare l’effetto da visualizzare sui bordi concavi (scuri) della curvatura. |
| <b>Contrasto concavo</b> <i>0.0 - 1.0</i> | Imposta il contrasto dell&#39;intervallo concavo. |
| <b>Inversione concava</b> <i>Falso/Vero</i> | Inverte l’interpretazione dei bordi concavi. |
| <b>Smoothness</b> <i>0.0 - 16.0</i> | Quantità di sfocatura e arrotondamento da applicare ai bordi della curvatura. |
| <b>Incremento livello</b> <i>0.0 - 1.0</i> | Un richiamo aggiuntivo se l’effetto non è sufficientemente visibile. |
| <b>Disturbo</b> <i>0.0 - 1.0</i> | Consente di impostare l’influenza del disturbo o della grunge sull’effetto Curvatura. |
| <b>Scala disturbo</b> <i>0 - 10</i> | Imposta la scala del disturbo. |
| <b>Tipo di disturbo</b> <i>Macchie, Nuvole, Umidità, Disturbo Bianco</i> | Scegli tra 4 diversi tipi di disturbo. |
| <b>Sfumatura superiore/inferiore</b> <i>-1.0 - 1.0</i> | Fusione o maschera con una sfumatura dall’alto verso il basso in base alla mappa Posizione. I valori positivi rendono le immagini più luminose, mentre i valori negativi nascondono gli effetti esistenti. |
| <b>Sfumatura</b> |  |
| <b>Intervallo</b> <i>0.0 - 1.0</i> | Imposta la posizione della sfumatura. |
| <b>Contrasto</b> <i>0.0 - 1.0</i> | Regola il contrasto della sfumatura. |
| <b>Inverti</b> <i>Falso/Vero</i> | Inverte la sfumatura. Scambia efficacemente il basso e l&#39;alto. |
| <b>Spazio globale normale</b> <i>0.0 - 1.0</i> | Simile a Sfumatura alto/basso, ma con la mappa di posizione e in sei direzioni, simile a una falsa illuminazione. I valori positivi si schiariscono, quelli negativi si scuriscono. |
| <b>Spazio globale normale</b> |  |
| <b>Intensità massima</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensità inferiore</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensità anteriore</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensità retro</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensità destra</b> <i>-1.0 - 1.0</i> |  |
| <b>Intensità sinistra</b> <i>-1.0 - 1.0</i> |  |
| <b>Scratches</b> <i>-1.0 - 1.0</i> | Fusione graffi nelle aree bianche. |
| <b>Scratches</b> |  |
| <b>Importo</b> <i>0 - 4096</i> | Imposta la quantità totale di graffi. |
| <b>Scala</b> <i>0.0 - 1.0</i> | Consente di impostare la scala dei singoli graffi. |
| <b>Dispersione</b> <i>-1.0 - 1.0</i> | Dispersione un timbro personalizzato all’interno di aree bianche. |
| <b>Dispersione</b> |  |
| <b>Scala</b> <i>0 - 50</i> | Scala totale dell’effetto. |
| <b>Densità</b> <i>0.0 - 1.0</i> | Controllo densità diffusione, numero da visualizzare. |
| <b>Dimensioni</b> <i>0.0 - 4.0</i> | Dimensione del timbro sparso. |
| <b>Variazione dimensioni</b> <i>0.0 - 1.0</i> | Variazione entro la dimensione del timbro. |
| <b>Variazione opacità</b> <i>0.0 - 1.0</i> | Variazione nell’opacità del timbro. |
