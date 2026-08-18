---
title: Cono chiuso 2 punti
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cono chiuso 2 punti
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Cono chiuso 2 punti

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Cono chiuso con 2 punti](./3d-sdf-capped-cone-2-points.png "Cono chiuso con 2 punti")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF di un cono chiuso definita dalle posizioni della base e della sommità.<br>La base e la parte superiore dispongono di raggi regolabili.

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
| <b>Base posizione</b> *Float3* | Posizione della base del cono con capping.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Posizione superiore</b> *Float3* | La posizione della parte superiore del cono con capping.<br><br><i>Impostazione predefinita: (0, 0, 1)</i> |
| <b>Base raggio</b> *Mobile* | Raggio della base del cono chiuso.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio superiore</b> *Mobile* | Raggio della parte superiore del cono chiuso.<br><br><i>Impostazione predefinita: 0.2</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
