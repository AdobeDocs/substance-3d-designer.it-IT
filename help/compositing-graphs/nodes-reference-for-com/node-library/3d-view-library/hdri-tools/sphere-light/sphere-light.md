---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Utilizzate il nodo Luce sfera per aggiungere sorgenti di luce sferica agli ambienti HDRI per un migliore controllo dell’illuminazione.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luce sfera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Luce sfera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-sphere-light.png){width="200px"}

## Luce sfera

**Ingresso:** *Visualizzazione/Strumento HDRI 3D*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Genera una forma sferica proiettata. La trasformazione della sfera è guidata da un gizmo di trasformazione.

La Sfera Light è abbastanza versatile e ha opzioni che gli permettono non solo di generare semplici luci rotonde, ma anche pianeti o altri corpi celesti. Se non avete bisogno delle opzioni di illuminazione e rotazione più avanzate, date un&#39;occhiata a [Shape Light](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md).

## Input

* **Input immagine di sfondo**: *Input colore* Sfondo opzionale su cui comporre la luce generata.
* **Input immagine forma**: *Input colore* Immagine facoltativa da mappare sulla luce sfera. Utilizzato solo quando Metodo colore forma è impostato su Input immagine.

### Parametri

* **Modalità posizione**: *Distanza dall&#39;origine, Posizione nel mondo*\
  Scegliete tra due modalità di posizionamento. La distanza dall&#39;origine è simile alle coordinate polari, la sfera è impostata rispetto al centro del panorama, la posizione del mondo funziona come le coordinate 3D standard.
* **Coordinate posizione**
  * **Vettore Su**: *Z Su, Y Su*\
    Solo con la modalità Posizione mondo (World Position), determinate l&#39;orientamento del sistema di coordinate.
  * **Posizione Mondo Sfera**: *-2.0 - 2.0*\
    Solo con la modalità Posizione mondo, imposta la posizione della sfera nello spazio mondo.
  * **Posizione**:\
    Solo in modalità Distanza dall&#39;origine. Imposta la posizione rispetto al centro. Può essere manipolato nella vista 2D.
  * **Distanza dall&#39;origine**: *0.0 - 20.0* Solo in modalità Distanza dall&#39;origine. Imposta la distanza dall&#39;origine e influisce sulle dimensioni visibili della sfera.
* **Metodo Colore Forma**: *RGB, Temperatura (Kelvin), Input Immagine*\
  Scegliere il metodo da utilizzare per impostare il colore della forma. Image Input consente di utilizzare il secondo slot di ingresso.
* **Colore**: *(valore colore)*\
  Solo con Metodo colore forma impostato su RGB. Seleziona il colore della forma.
* **Temperatura forma**: *800.0 - 20000.0*\
  Solo con il Metodo colore forma impostato su Temperatura. Imposta il valore Kelvin per il colore della forma.
* **Gamma input immagine Sfera**: *sRGB, lineare*\
  Solo con Metodo colore forma impostato su Input immagine. Determinare come interpretare l&#39;input dell&#39;immagine della forma.
* **Rotazione sfera**: *0,0 - 1,0*\
  Solo con Metodo colore forma impostato su Input immagine. Ruota la sfera attorno al centro per orientare l&#39;immagine mappata.
* **Esposizione (EV)**: *0,0 - 10,0*\
  Imposta il valore di esposizione per la forma generata, che idealmente corrisponde al valore di esposizione dell&#39;immagine di sfondo.
* **Raggio sfera**: *0,0 - 1,0*\
  Imposta raggio/dimensione della sfera.
* **Durezza sfera**: *0,0 - 1,0*\
  Imposta la durezza/decadimento della sfera.
* **Ombreggiatura**: *Nessuna, Scurire Gli Arti, Ombreggiatura Luce*\
  Impostare se una qualsiasi ombreggiatura deve essere applicata alla sfera. Consente di non visualizzare la sfera come oggetto solido e non illuminato. Scurire gli arti significa scurire leggermente i bordi; Ombreggiatura Luce significa illuminare la sfera con un’Ombreggiatura opzionale Luce.
* **Ombreggiatura Luce Posizione Mondo**: *-1.0 - 1.0*\
  Se l’Ombreggiatura è impostata su Luce Ombreggiatura, la posizione della luce sulla sfera è controllata qui.
* **Trasparenza Penombra**: *0,0 - 1,0*\
  Se Ombreggiatura è impostato su Luce Ombreggiatura, controlla la fine dell’ombreggiatura.
* **Abilita input in background**: *False/True*\
  Attiva/disattiva l’uso di un’immagine di sfondo facoltativa. Compone la luce generata sopra lo sfondo.
* **Colore di sfondo**: *(valore colore)*\
  Se l’opzione Input sfondo non viene utilizzata, imposta qui un valore per lo sfondo in tinta unita.
* **Gamma sfondo**: *sRGB, lineare* Se viene utilizzato l’input di sfondo, imposta come interpretare l’input di sfondo.

## Immagini di esempio

![](../../../../../../assets/sphere-light-ex.gif)

![](../../../../../../assets/spherelight-ex1.png)

</td>
</tr>
</table>
