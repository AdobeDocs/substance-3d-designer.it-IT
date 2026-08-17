---
title: Capsula
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Capsula
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Capsula

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Capsula](./3d-sdf-capsule.png "Capsula")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una Funzione SDF per una capsula di lunghezza e raggio regolabili.<br>La capsula è il risultato del collegamento di due sfere.

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
| <b>Inizio</b> *Float3* | Posizione della sfera iniziale.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Fine</b> *Float3* | Posizione della sfera finale.<br><br><i>Impostazione predefinita: (0, 0, 1)</i> |
| <b>Raggio</b> *Mobile* | Raggio delle sfere iniziale e finale.<br><br><i>Impostazione predefinita: 0.25</i> |
| <b>Inizio/fine alla punta</b> *Booleano* | Controlla se le posizioni <b>Inizio</b> e <b>Fine</b> devono essere alle estremità delle sfere.<br>Controlla ad esempio se il height della capsula deve includere il raggio delle sfere.<br><br><i>Impostazione predefinita: False</i> |
| <b>Posizione centrale</b> *Float3* | Posizione nello spazio globale del perno della capsula.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
