---
title: Torsione (inesatta)
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Torsione (inesatta)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Torsione (inesatta)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Torsione (inesatta)](./3d-sdf-transform-twist.png "Torsione (inesatta)")

<b>In:</b> Funzione SDF > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Ruota una forma SDF attorno all&#39;asse Z locale tra un punto iniziale e un punto finale, a un angolo regolabile.<br><br><i>Nota:</i>Poiché questa funzione di trasformazione non è esatta, è possibile che vengano visualizzati artefatti durante il rendering.

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
| <b>Angolo</b> *Mobile* | Angolo, in giri, della rotazione applicata alla fine della torsione. |
| <b>Inizio</b> *Mobile* | Posizione del mondo sull&#39;asse Z in cui inizia la torsione. Tutto il volume sottostante non è distorto. |
| <b>Fine</b> *Mobile* | Posizione del mondo sull&#39;asse Z in cui termina la torsione. Tutto il volume di cui sopra viene ruotato in modo uniforme all’angolo specificato. |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
