---
title: Cubo
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Cubo
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Cubo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona cubo](./3d-sdf-cube.png "Cubo")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cubo, con dimensioni XYZ regolabili e arrotondamento dei bordi.

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
| <b>Dimensioni</b> *Float3* | Dimensione del cubo su X, Y e Z.<br><br><i>Impostazione predefinita: (1, 1, 1)</i> |
| <b>Arrotondamento</b> *Mobile* | Raggio degli archi arrotondati applicati ai bordi del cubo.<br><br><i>Nota:</i> bordi rigidi possono apparire nel punto di intersezione dei raggi di arrotondamento.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione dei punti cardini (locale)</b> *Float3* | Posizione dello spazio globale del fulcro locale del cubo, in cui (0, 0, 0) posiziona il fulcro al centro del cubo.<br><br><i>Impostazione predefinita: (0, 0, -0.5)</i> |
| <b>Posizione centrale</b> *Float3* | Posizione dello spazio globale del fulcro del cubo.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
