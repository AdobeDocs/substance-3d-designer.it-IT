---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce piano per aggiungere sorgenti luminose planari agli ambienti HDRI per il controllo direzionale dell’illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce piano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---


# Luce piano

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-plane-light.png){width="200px"}

## Luce piano

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una forma piano proiettata sfericamente. Il piano può essere posizionato e orientato in 3D utilizzando i parametri di input.

Si distingue dalla [Luce forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) più semplice in quanto ha più opzioni di posizionamento avanzate al di fuori di una proiezione Distanza dall&#39;origine più semplice e consente di applicare più pattern e maschere, simili a [Luce linea](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

## Input

* **Input immagine di sfondo**: *Input colore*\
  Sfondo opzionale su cui comporre la luce generata.
* **Input immagine forma**: *Input colore*\
  Immagine opzionale da mappare su luce di linea. Utilizzato solo quando Metodo colore forma è impostato su Input immagine.
* **Input immagine pattern**: *Input scala di grigi*\
  Immagine con pattern personalizzato, utilizzata quando il parametro &quot;Pattern&quot; è impostato su &quot;Image Input&quot;.

## Parametri

* **Modalità Posizione**: *Posizioni Terra/Soffitto, Distanza dall&#39;origine, Mondo*\
  Selezionate tre diverse modalità di posizionamento. Le opzioni di manipolazione per il supporto di Distanza dall&#39;origine/Soffitto e Terra nella vista 2D consentono di modificare le posizioni di World solo mediante le proprietà, ma supportano anche un posizionamento più preciso.
* **Mostra griglia terreno**: *False/True*\
  Funzione di supporto per consentire la creazione di una griglia di terra di debug. Consente di stimare la posizione delle linee nello spazio.
* **Coordinate posizione**
  * **Vettore Su**: *Z Su, Y Su*\
    Solo con la modalità Posizione mondo (World Position), determinate l&#39;orientamento del sistema di coordinate.
  * **Posizione UV piano**:\
    Solo con messa a terra/a soffitto e Distanza dall&#39;origine. Imposta la posizione del piano nello spazio UV.
  * **Posizione Plane World**: *-2.0 - 2.0*\
    Solo con la modalità Posizioni mondiali. Imposta lo spazio del mondo della posizione piana. Nessuna interazione di visualizzazione 2D supportata.
  * **Height assoluto del piano**: *0,0 - 1,0*\
    Solo con la modalità di posizione Terra/Soffitto, imposta il height assoluto dal soffitto. Utilizzate Mostra griglia terreno per stimare meglio la posizione.
  * **Distanza dall&#39;origine**: *0.0 - 1.0*\
    Solo con la modalità Posizione Distanza dall&#39;origine. Imposta la distanza dal centro del panorama per entrambi i punti.
* **Metodo Colore Forma**: *RGB, Temperatura (Kelvin), Input Immagine*\
  Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso.
* **Colore**: *(valore colore)*\
  Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma.
* **Temperatura**: *800,0 - 20000,0*\
  Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma.
* **Modalità UV immagine forma**: *Allunga, Allunga solo al centro, Ripeti + Spaziatura*\
  Solo con Metodo colore forma impostato su Input immagine. Consente di impostare il modo in cui l&#39;immagine viene applicata alla forma della linea e determina il comportamento di ripetizione UV.
* **Spaziatura ripetizione immagine forma**: *0.0 - 1.0*\
  Solo con Metodo colore forma impostato su Input immagine e con Metodo UV impostato su Ripeti + Spaziatura. Imposta la spaziatura quando l’immagine si ripete lungo la linea.
* **Gamma immagine forma**: *sRGB, lineare*\
  Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma.
* **Esposizione (EV)**: *0,0 - 10,0*\
  Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo.
* **Scala piano**: *0,0 - 1,0*\
  Impostate la scala uniforme della forma Piano.
* **Dimensione piano**: *0,0 - 1,0*\
  Impostate le dimensioni non uniformi della forma Piano.
* **Rotazione piano**: *0,0 - 1,0*\
  Ruota piano lungo l&#39;asse centrale.
* **Pattern**: *Quadrato Smussato, Quadrato Nitido, Cono, Emisfero, Input Immagine*\
  Selezionare la forma del motivo da utilizzare.
* **Durezza motivo**: *0,0 - 1,0*\
  Impostate la durezza/il contrasto per il pattern.
* **Modalità UV pattern**: *Allunga, Allunga solo al centro*\
  Imposta come utilizzare la maschera di pattern secondaria, applicata sopra l’immagine della forma.
* **Abilita ritaglio terreno**: *False/True*\
  Attiva questa opzione se il piano può essere ritagliato da un piano terreno o se viene ancora visualizzato quando si va al di sotto di esso. Usate Mostra griglia terreno per una migliore stima.
* **Height terreno**: *-2.0 - 0,0*\
  Regolate il height terra per il ritaglio.
* **Abilita input in background**: *False/True*\
  Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo.
* **Colore di sfondo**: *(valore colore)*\
  Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita.
* **Gamma sfondo**: *sRGB, lineare* Se viene utilizzato l’input di sfondo, imposta come interpretare l’input di sfondo.

## Immagini di esempio

![](../../../../../../assets/plane-light-ex.gif)

</td>
</tr>
</table>
