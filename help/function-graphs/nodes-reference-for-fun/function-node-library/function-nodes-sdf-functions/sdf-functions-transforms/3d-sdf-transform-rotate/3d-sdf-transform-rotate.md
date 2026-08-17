---
title: Ruota
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Ruota
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Ruota

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Ruota](./3d-sdf-transform-rotate.png "Ruota")

<b>In:</b> Funzione SDF > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Ruotare una forma SDF attorno a uno o più assi da un punto fulcro regolabile, in giri.<br>Utilizzare l&#39;helper <b>Trasforma pivot</b> di <b>Visualizzatore 3D</b> per visualizzare la rotazione eseguita.

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
| <b>SDF</b> *Mobile* | Forma SDF di input. |
| <b>Angolo</b> *Mobile* | Angolo, in giri, in cui viene ruotata la forma SDF.<br><br>L&#39;angolo viene visualizzato da un cerchio nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. Allineate la fotocamera in modo da visualizzare la freccia <b>Asse</b> come centro di questo cerchio per visualizzare chiaramente l&#39;angolo di rotazione come frazione di una curva.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Asse</b> *Float3* | Vettore normalizzato che definisce l&#39;asse attorno al quale viene ruotata la forma SDF.<br>Ad esempio (0, 1, 0) ruota la forma SDF attorno all’asse Y del relativo punto fulcro locale.<br><br>L&#39;asse è visualizzato da una freccia nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. Il colore della freccia è mappato sui componenti XYZ di questo vettore.<br><br><i>Impostazione predefinita: (0, 1, 0)</i> |
| <b>Posizione dei punti cardini</b> *Float3* | Posizione dello spazio globale del fulcro locale della forma SDF, in cui (0, 0, 0) posiziona il fulcro al centro della forma SDF. Definisce l’origine della rotazione.<br><br>Il pivot viene visualizzato dall&#39;inizio della freccia nell&#39;helper <b>Trasforma pivot</b> del <b>Visualizzatore 3D</b>. |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
