---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce linea per creare sorgenti luminose lineari in ambienti HDRI per simulare la fluorescenza e l’illuminazione a strisce.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce linea
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---


# Luce linea

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-line-light.png){width="200px"}

## Luce linea

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una forma di linea proiettata sfericamente in base alle coordinate di due punti nello spazio. Rispetto alla [Luce forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md), offre più opzioni per orientare le forme e applicare pattern ripetuti alla forma chiara.

Le modalità di posizionamento per questo nodo sono leggermente più complesse rispetto ad altri nodi luce HDRI. Si consiglia di provare alcune modalità di dimensioni diverse per trovare quello che funziona per voi scenario.

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
  * **Posizione UV Punto 1**:\
    Solo con messa a terra/a soffitto e Distanza dall&#39;origine. Imposta la posizione del primo punto nello spazio UV.
  * **Posizione UV Punto 2**:\
    Solo con messa a terra/a soffitto e Distanza dall&#39;origine. Imposta la posizione del secondo punto nello spazio UV.
  * **Posizione Mondiale Punto 1**: *-2.0 - 2.0*\
    Solo con la modalità Posizioni mondiali. Imposta il primo punto nello spazio mondo. Nessuna interazione di visualizzazione 2D supportata.
  * **Posizione Mondiale Punto 2**: *-2.0 - 2.0*\
    Solo con la modalità Posizioni mondiali. Imposta il secondo punto nello spazio mondo. Nessuna interazione di visualizzazione 2D supportata.
  * **Height assoluto di righe**: *0.0 - 1.0*\
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
* **Rotazione riga**: *0,0 - 1,0*\
  Ruota la linea lungo l&#39;asse della lunghezza. La linea viene trattata come un nastro piatto durante la rotazione.
* **Thickness di righe**: *0.0 - 1.0*\
  Imposta il thickness della scheda di linea.
* **Pattern**: *Quadrato Smussato, Quadrato Nitido, Cono, Emisfero, Input Immagine*\
  Selezionare la forma del motivo da utilizzare.
* **Durezza motivo**: *0,0 - 1,0*\
  Impostate la durezza/il contrasto del pattern.
* **Modalità UV Pattern**: *Allunga, Allunga solo al centro, Ripeti + Spaziatura*\
  Imposta come utilizzare la maschera di pattern secondaria, applicata sopra l’immagine della forma.
* **Spaziatura ripetizione pattern**: *0.0 - 1.0*\
  Solo se Modalità UV pattern è impostato su Ripeti + Spaziatura. Impostate la spaziatura tra i pattern ripetuti.
* **Abilita ritaglio terreno**: *False/True*\
  Abilita il ritaglio del disegno con linee. L’effetto non è visibile quando si utilizza la modalità di posizionamento Terra/Soffitto.
* **Height terreno**: *-2.0 - 0,0*\
  Imposta il height relativo del piano di arrotondamento utilizzato per il ritaglio. Ha effetto sulla griglia del terreno disegnata.
* **Abilita input in background**: *False/True*\
  Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo.
* **Colore di sfondo**: *(valore colore)*\
  Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita.
* **Gamma sfondo**: *sRGB, lineare* Se viene utilizzato l’input di sfondo, imposta come interpretare l’input di sfondo.

## Immagini di esempio

![](../../../../../../assets/line-light-ex.gif)

</td>
</tr>
</table>
