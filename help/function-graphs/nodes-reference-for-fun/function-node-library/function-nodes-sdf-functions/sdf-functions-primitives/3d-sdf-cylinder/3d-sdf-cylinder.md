---
title: Cilindro
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cilindro
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
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
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../../../../../learning-tutorials/nodes/working-with-sdf-functions/working-with-sdf-functions.md)

## Input

|  |  |
| :--- | :--- |
| <b>Height</b> *Virgola mobile* | Height Z-up del cilindro dalla base.<br><br><i>Impostazione predefinita: 1</i> |
| <b>Raggio</b> *Virgola mobile* | Raggio del cilindro.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Arrotondamento</b> *Virgola mobile* | Raggio degli archi arrotondati applicati ai bordi del cilindro.<br><br><i>Nota:</i> bordi rigidi possono apparire nel punto di intersezione dei raggi di arrotondamento.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione dei punti cardini (locale)</b> *Virgola mobile 3* | Posizione nello spazio globale del perno locale del cilindro, in cui (0, 0, 0) posiziona il perno al centro del cilindro.<br><br><i>Impostazione predefinita: (0, 0, -0.5)</i> |
| <b>Posizione centrale</b> *Virgola mobile 3* | Posizione dello spazio globale del perno del cilindro.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
