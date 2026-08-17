---
title: Toroide
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Toro
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# Toroide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Toro](./3d-sdf-torus.png "Toro")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una Funzione SDF per un toro, che è una forma formata spazzando un cerchio minore lungo un cerchio maggiore.<i>Entrambi i cerchi hanno raggi regolabili.

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
| <b>Raggio principale</b> *Mobile* | Raggio del cerchio lungo il quale viene effettuata la sweep del disco secondario per formare la superficie del toro.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio minore</b> *Mobile* | Raggio del cerchio trascinato lungo il cerchio principale per formare la superficie del toro.<br><br><i>Impostazione predefinita: 0.2</i> |
| <b>Posizione centrale</b> *Float3* | Posizione dello spazio globale del perno del toro.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
