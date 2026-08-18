---
title: Cilindro
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cilindro
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Cilindro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona cilindro](./3d-sdf-cylinder.png "Cilindro")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cilindro di height regolabile, raggio e arrotondamento degli spigoli.

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
| <b>Height</b> *Mobile* | Height Z-up del cilindro dalla base.<br><br><i>Impostazione predefinita: 1</i> |
| <b>Raggio</b> *Mobile* | Raggio del cilindro.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Arrotondamento</b> *Mobile* | Raggio degli archi arrotondati applicati ai bordi del cilindro.<br><br><i>Nota:</i> bordi rigidi possono apparire nel punto di intersezione dei raggi di arrotondamento.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione dei punti cardini (locale)</b> *Float3* | Posizione nello spazio globale del perno locale del cilindro, in cui (0, 0, 0) posiziona il perno al centro del cilindro.<br><br><i>Impostazione predefinita: (0, 0, -0.5)</i> |
| <b>Posizione centrale</b> *Float3* | Posizione dello spazio globale del perno del cilindro.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
