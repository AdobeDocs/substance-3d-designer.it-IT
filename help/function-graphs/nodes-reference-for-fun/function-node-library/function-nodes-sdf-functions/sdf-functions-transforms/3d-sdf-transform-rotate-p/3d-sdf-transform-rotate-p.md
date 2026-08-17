---
title: Ruota P
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Ruota P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Ruota P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Ruota P](./3d-sdf-transform-rotate-p.png "Ruota P")

<b>In:</b> Funzione SDF > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Ruota lo spazio globale attorno a un asse con un angolo regolabile.<br>La posizione del mondo trasformato in output può essere collegata all&#39;input <b>P</b> della maggior parte delle Funzioni SDF per definirle in questo spazio del mondo trasformato.<br><br>Utilizzare l&#39;helper <b>Trasforma pivot</b> di <b>Visualizzatore 3D</b> per visualizzare la rotazione eseguita.<br><br><i>Suggerimento:</i> le trasformazioni P possono essere concatenate, ma tenete presente che i risultati dipendono dall&#39;ordine delle operazioni.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../working-with-sdf-functions.md)

## Input

|  |  |
| :--- | :--- |
| <b>Angolo</b> *Mobile* | L&#39;angolo, a rotazione, a cui ruota lo spazio mondiale.<br><br>L&#39;angolo viene visualizzato da un cerchio nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. Allineate la fotocamera in modo da visualizzare la freccia <b>Asse</b> come centro di questo cerchio per visualizzare chiaramente l&#39;angolo di rotazione come frazione di una curva. |
| <b>Asse</b> *Float3* | Vettore normalizzato che definisce l&#39;asse attorno al quale viene ruotato lo spazio globale.<br>Ad esempio (0, 1, 0) ruoterà lo spazio globale attorno all’asse Y del punto fulcro.<br><br>L&#39;asse è visualizzato da una freccia nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. Il colore della freccia è mappato sui componenti XYZ di questo vettore.<br><br><i>Impostazione predefinita: (0, 1, 0)</i> |
| <b>Posizione dei punti cardini</b> *Float3* | Posizione dello spazio globale del perno che definisce l&#39;origine della rotazione.<br><br>Il punto pivot viene visualizzato dall&#39;inizio della freccia nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
