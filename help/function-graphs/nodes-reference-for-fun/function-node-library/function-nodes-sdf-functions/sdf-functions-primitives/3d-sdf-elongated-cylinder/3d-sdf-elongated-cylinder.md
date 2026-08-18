---
title: Cilindro allungato
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Cilindro allungato
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
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
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../working-with-sdf-functions.md)

## Input

|  |  |
| :--- | :--- |
| <b>Height</b> *Mobile* | Height Z-up dei cilindri iniziale e finale dalla base.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio</b> *Mobile* | Raggio dei cilindri iniziale e finale.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Arrotondamento</b> *Mobile* | Raggio degli archi arrotondati applicati agli spigoli del cilindro allungato.<br><br><i>Nota:</i> spigoli rigidi possono apparire dove i raggi di arrotondamento si intersecano.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione centrale</b> *Float3* | Posizione nello spazio globale del perno del cilindro allungato.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Distanza di allungamento</b> *Mobile* | La distanza lungo la quale il cilindro iniziale è allungato.<br>Cioè la distanza tra i centri dei cilindri iniziale e finale.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
