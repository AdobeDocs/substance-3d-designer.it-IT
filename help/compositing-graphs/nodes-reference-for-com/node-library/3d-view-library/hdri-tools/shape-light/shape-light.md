---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce forma per aggiungere sorgenti luminose a forma personalizzata agli ambienti HDRI per creare effetti di luce creativi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma luce
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Forma luce

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## Forma luce

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una forma rettangolare proiettata sfericamente. La trasformazione della forma è guidata da un gizmo di trasformazione.

## Input

* **Input immagine di sfondo**: *Input colore* Sfondo opzionale su cui comporre la luce generata.
* **Input immagine forma**: *Input colore* Immagine facoltativa da mappare sulla luce sfera. Utilizzato solo quando Metodo colore forma è impostato su Input immagine.

## Parametri

* **Matrice forme**
  * **Matrice**: *(Matrice Di Trasformazione)*\
    Controllo di trasformazione per il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro.
  * **Scostamento**: *-2,0 - 2,0*\
    Sposta o converte il risultato. Il risultato può essere modificato interagendo direttamente con l&#39;area di lavoro.
* **Forma**: *Rettangolo, Disco*\
  Scegliete la forma da posizionare.
* **Metodo Colore Forma**: *RGB, Temperatura (Kelvin), Input Immagine*\
  Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso.
* **Colore**: *(valore colore)*\
  Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma.
* **Temperatura forma**: *800.0 - 20000.0*\
  Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma.
* **Gamma input immagine forma**: *sRGB, lineare*\
  Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma.
* **Esposizione forma (EV)**: *0,0 - 10,0*\
  Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo.
* **Durezza forma**: *0,0 - 1,0*\
  Impostate la durezza dei bordi della forma.
* **Esposizione hotspot (EV)**: *0.0 - 10.0*\
  Imposta Esposizione del punto attivo centrale. Si noti che questo non è molto visibile in modalità RGB.
* **Dimensione hotspot**: *0,0 - 1,0*\
  Dimensioni del punto attivo centrale.
* **Falloff hotspot**: *0,0 - 1,0*\
  Decadimento del punto caldo centrale.
* **Posizione punto attivo**: *0.0 - 1.0*\
  Posizione X e Y del punto attivo centrale.
* **Abilita input in background**: *False/True*\
  Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo.
* **Colore di sfondo**: *(valore colore)*\
  Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita.
* **Gamma sfondo**: *sRGB, lineare* Se viene utilizzato l’input di sfondo, imposta come interpretare l’input di sfondo.

## Immagini di esempio

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
