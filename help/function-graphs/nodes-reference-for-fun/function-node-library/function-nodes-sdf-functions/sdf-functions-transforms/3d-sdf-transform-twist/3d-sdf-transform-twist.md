---
title: Torsione (inesatta)
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Torsione (inesatta)
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
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
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../../../../../learning-tutorials/nodes/working-with-sdf-functions/working-with-sdf-functions.md)

## Input

|  |  |
| :--- | :--- |
| <b>SDF</b> *Virgola mobile* | Forma SDF di input. |
| <b>Angolo</b> *Virgola mobile* | Angolo, in giri, della rotazione applicata alla fine della torsione. |
| <b>Inizio</b> *Virgola mobile* | Posizione del mondo sull&#39;asse Z in cui inizia la torsione. Tutto il volume sottostante non è distorto. |
| <b>Fine</b> *Virgola mobile* | Posizione del mondo sull&#39;asse Z in cui termina la torsione. Tutto il volume di cui sopra viene ruotato in modo uniforme all’angolo specificato. |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
