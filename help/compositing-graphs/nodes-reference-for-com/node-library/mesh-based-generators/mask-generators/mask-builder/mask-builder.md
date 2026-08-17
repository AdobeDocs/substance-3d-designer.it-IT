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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---


# Generatore maschera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mask-builder.png){width="128px"}

## Generatore maschera

**Ingresso:** *Generatori Basati Su Trama**/Generatori Maschera*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una maschera in bianco e nero in base alle mappe con baking e alle impostazioni dell’utente. Si tratta più o meno della versione Designer di Painter Mask Builder.

Si tratta di uno strumento complicato inteso come un generatore di maschere onnicomprensivo, basato su mappe con baking, parametri utente e pattern e mappe grunge. È principalmente inteso come un nodo molto avanzato, pieno controllo per fondere in piega dirt e usura dei bordi. Questo nodo è abbastanza potente da simulare ogni altro generatore di maschere.

Nessun bakes è esplicitamente richiesto, ma più fornisci, più questo nodo è in grado di fare.

## Parametri

### Input

* **Occlusione ambiente**: *Input scala di grigi*
* **Curvatura**: *Input scala di grigi*
* **Spazio Mondiale Normale**: *Input Colore*
* **Input Grunge**: *Input scala di grigi*
* **Input Grunge 2**: *Input scala di grigi*
* **Input Dispersione**: *Input scala di grigi*\
  Timbro dispersione personalizzato, necessario per utilizzare i parametri della Dispersione.
* **Maschera (facoltativo)**: *Input scala di grigi*\
  Slot maschera utilizzato per mascherare gli effetti del nodo.
* **Posizione**: *Input colore*\
  Utilizzato per gli effetti Triplanari e Dall&#39;alto in basso.

### Parametri

* **Livello**: *0,0 - 1,0*\
  Imposta il livello totale dell’effetto, rivelandolo gradualmente.
* **Contrasto**: *0.0 - 1.0*\
  Regola il contrasto del risultato.
* **Inverti**: *Falso/Vero*\
  Inverte il risultato. Utile per ottenere l’opposto della maschera che state creando.
* **Usa Triplanare**: *Falso/Vero* Consente la proiezione Triplanare, evitando cuciture con mappe di grungi.
* **Contrasto fusione triplanare**: *0.0 - 1.0* Imposta il contrasto per la fusione triplanare.
* **Grunge**: *0.0 - 1.0* Imposta la quantità di Grunge da combinare a livello globale.
* **Grunge**
  * **Scala**: *0 - 10* Imposta la scala della Grunge globale.
  * **Usa Grunge personalizzata**: *False/True* Abilita l&#39;input Grunge personalizzato.
  * **Grunge personalizzata secondaria**: *0.0 - 1.0* Abilita un secondo input personalizzato per la Grunge.
  * **Inverti**: *Falso/Vero*\
    Inverte la mappa della Grunge.
* **AO**: *-1.0 - 1.0* Imposta l&#39;estensione in base alla quale l&#39;effetto dovrebbe apparire nelle aree AO occluse. Può essere modificato con il gruppo seguente.
* **AO**
  * **Intervallo**: *0.0 - 1.0* Imposta la soglia o l&#39;intervallo per l&#39;aspetto del dirt.
  * **Contrasto**: *0.0 - 1.0*\
    Regola il contrasto dell’effetto AO.
  * **Disturbo**: *0.0 - 1.0* Imposta la quantità di disturbo/grunge da fondere nell&#39;effetto AO.
  * **Scala disturbo**: *0 - 10* Imposta la scala del disturbo/grunge dell&#39;operatore aereo.
  * **Tipo di disturbo**: *Macchie, nuvola, umidità, disturbo bianco* Alterna 4 tipi diversi di disturbo AO.
  * **Inverti**: *Falso/Vero*\
    Inverte l’interpretazione della mappa AO: appariranno disturbi in aree AO luminose, non scure.
* **Curvatura**: *0.0 - 1.0* Imposta la quantità di effetto da visualizzare sui bordi della curvatura; può essere sia convessa che concava. Modificate questa impostazione con il gruppo sottostante.
* **Curvatura**
  * **Intervallo convesso**: *-1.0 - 1.0* Imposta l&#39;effetto da visualizzare sui bordi di curvatura convessi (luminosi).
  * **Contrasto convesso**: *0.0 - 1.0* Imposta il contrasto dell&#39;effetto Convesso.
  * **Inversione convessa**: *False/True* Inverte l&#39;interpretazione dei bordi convessi.
  * **Intervallo concavo**: *-1.0 - 1.0* Imposta l&#39;effetto da visualizzare sui bordi di curvatura concava (scuri).
  * **Contrasto concavo**: *0.0 - 1.0* Imposta il contrasto dell&#39;intervallo concavo.
  * **Inversione concava**: *False/True* Inverte l&#39;interpretazione dei bordi concavi.
  * **Smoothness**: *0,0 - 16,0* Quantità di sfocatura e arrotondamento da applicare ai bordi della curvatura.
  * **Incremento livello**: *0.0 - 1.0* Incremento aggiuntivo se l&#39;effetto non è sufficientemente visibile.
  * **Disturbo**: *0.0 - 1.0* Imposta l&#39;influenza del disturbo/della grunge sull&#39;effetto Curvatura.
  * **Scala disturbo**: *0 - 10* Imposta la scala del disturbo.
  * **Tipo di disturbo**: *Macchie, Nuvola, Umidità, Rumore bianco* Scegli tra 4 tipi di disturbo diversi.
* **Sfumatura dall&#39;alto verso il basso**: *-1.0 - 1.0* Sfumatura o maschere con una sfumatura dall&#39;alto verso il basso in base alla mappa Posizione. I valori positivi rendono le immagini più luminose, mentre i valori negativi nascondono gli effetti esistenti.
* **Sfumatura**
  * **Intervallo**: *0.0 - 1.0* Imposta la posizione della sfumatura.
  * **Contrasto**: *0.0 - 1.0*\
    Regola il contrasto della sfumatura.
  * **Inverti**: *Falso/Vero*\
    Inverte la sfumatura. Scambia efficacemente il basso e l&#39;alto.
* **Spazio normale**: *0.0 - 1.0* Simile alla sfumatura alto/basso, ma con la mappa di posizione e in sei direzioni, simile alla falsa illuminazione. I valori positivi si schiariscono, quelli negativi si scuriscono.
* **Spazio globale normale**
  * **Intensità massima**: *-1,0 - 1,0*
  * **Intensità inferiore**: *-1,0 - 1,0*
  * **Intensità anteriore**: *-1,0 - 1,0*
  * **Intensità schiena**: *-1,0 - 1,0*
  * **Intensità destra**: *-1,0 - 1,0*
  * **Intensità sinistra**: *-1,0 - 1,0*
* **Scratches**: *-1.0 - 1.0* Fonde i graffi nelle aree bianche.
* **Scratches**
  * **Quantità**: *0 - 4096* Imposta la quantità totale di graffi.
  * **Scala**: *0.0 - 1.0* Imposta la scala dei singoli graffi.
* **Dispersione**: *-1.0 - 1.0* Dispersione un timbro personalizzato all&#39;interno di aree bianche.
* **Dispersione**
  * **Scala**: *0 - 50* Scala totale dell&#39;effetto.
  * **Densità**: *0.0 - 1.0* Controllo densità diffusione, numero da visualizzare.
  * **Dimensioni**: *0,0 - 4,0* Dimensioni del timbro sparso.
  * **Variazione dimensioni**: *0.0 - 1.0* Variazione entro la dimensione del timbro.
  * **Variazione opacità**: *0.0 - 1.0* Variazione nell&#39;opacità del timbro.

## Immagini di esempio

|  |
| --- |
| Nessuna immagine allegata alla pagina. |

</td>
</tr>
</table>
