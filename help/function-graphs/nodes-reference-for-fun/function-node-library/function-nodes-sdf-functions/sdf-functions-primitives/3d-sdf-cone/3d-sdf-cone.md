---
title: Cono
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Cono
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%
---

# Cono

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Cono](./3d-sdf-cone.png "Cono")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cono di height, raggio e posizione regolabili.

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
| <b>Raggio</b> *Virgola mobile* | Raggio della base del cono.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Height</b> *Virgola mobile* | Height Z-up dell&#39;apice del cono dalla base.<br><br><i>Impostazione predefinita: 1</i> |
| <b>Posizione centrale</b> *Virgola mobile 3* | Posizione dello spazio globale del perno del cono.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
