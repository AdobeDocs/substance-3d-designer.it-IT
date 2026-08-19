---
title: Cilindro 2 punti
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cilindro 2 punti
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Cilindro 2 punti

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Cilindro 2 punti](./3d-sdf-cylinder-2-points.png "Cilindro 2 punti")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cilindro di raggio regolabile definito dalle posizioni dei dischi iniziale e finale.

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
| <b>Inizio</b> *Float3* | Posizione del disco iniziale del cilindro.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Fine</b> *Float3* | Posizione del disco finale del cilindro.<br><br><i>Impostazione predefinita: (0, 0, 1)</i> |
| <b>Raggio</b> *Mobile* | Raggio del cilindro.<br><br><i>Impostazione predefinita: 0.25</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
