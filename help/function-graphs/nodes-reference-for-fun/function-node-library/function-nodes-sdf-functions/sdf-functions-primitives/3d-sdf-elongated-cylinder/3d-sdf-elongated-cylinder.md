---
title: Cilindro allungato
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cilindro allungato
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%
---

# Cilindro allungato

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona cilindro allungato](./3d-sdf-elongated-cylinder.png "Cilindro allungato")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cilindro allungato di lunghezza regolabile, raggio e arrotondamento degli spigoli.<br>Il cilindro allungato è il risultato del collegamento di due cilindri.

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
| <b>Height</b> *Virgola mobile* | Height Z-up dei cilindri iniziale e finale dalla base.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio</b> *Virgola mobile* | Raggio dei cilindri iniziale e finale.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Arrotondamento</b> *Virgola mobile* | Raggio degli archi arrotondati applicati agli spigoli del cilindro allungato.<br><br><i>Nota:</i> spigoli rigidi possono apparire dove i raggi di arrotondamento si intersecano.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione centrale</b> *Virgola mobile 3* | Posizione nello spazio globale del perno del cilindro allungato.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Distanza di allungamento</b> *Virgola mobile* | La distanza lungo la quale il cilindro iniziale è allungato.<br>Cioè la distanza tra i centri dei cilindri iniziale e finale.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
