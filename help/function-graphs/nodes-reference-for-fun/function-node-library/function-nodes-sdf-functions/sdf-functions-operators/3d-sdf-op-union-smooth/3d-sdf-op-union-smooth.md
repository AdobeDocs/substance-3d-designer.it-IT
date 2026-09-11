---
title: Unione uniforme
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Operatore > Uniforma unione
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Unione uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Unione uniforme](./3d-sdf-op-union-smooth.png "Unione uniforme")

<b>In:</b> Funzione SDF > Operatore

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Restituisce i volumi aggiunti di due forme SDF, con arrotondamento regolabile dei bordi della relativa intersezione.

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
| <b>SDF 1</b> *Virgola mobile* | La prima forma SDF. |
| <b>SDF 2</b> *Virgola mobile* | La seconda forma SDF. |
| <b>Smoothness</b> *Virgola mobile* | Raggio di arrotondamento, a partire dai bordi dell&#39;intersezione.<br><br><i>Impostazione predefinita: 0</i><br><br><i>Nota:</i> bordi rigidi possono apparire nel punto di intersezione dei raggi di arrotondamento. |
