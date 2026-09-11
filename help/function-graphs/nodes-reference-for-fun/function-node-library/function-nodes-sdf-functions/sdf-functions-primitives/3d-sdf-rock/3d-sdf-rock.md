---
title: Rock
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Rock
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Rock

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Rock](./3d-sdf-rock.png "Rock")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una Funzione SDF per una forma rocciosa parametrica e casuale, costruita con Funzioni SDF.

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
| <b>Max. facet</b> *Numero intero* | Numero massimo di sfaccettature della roccia (fino a 32).<br><br><i>Impostazione predefinita: 8</i> |
| <b>Smoothness</b> *Virgola mobile* | Raggio degli archi arrotondati applicato ai bordi della roccia.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Casualità</b> *Virgola mobile* | Modifica l&#39;orientamento e la distanza delle facce rispetto al centro.<br>Di conseguenza, valori maggiori producono una roccia più piccola.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Valore di inizializzazione</b> *Virgola mobile* | Valore di inizializzazione per il parametro <b>Casualità</b>.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Scala</b> *Virgola mobile* | Scala globale della forma della roccia.<br>Applicato dopo <b>Casualità</b> e prima di <b>Smoothness</b>.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Posizione centrale</b> *Float3* | Posizione dello spazio globale del perno della roccia.<br><br><i>Impostazione predefinita: (0, 0, 0.5)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
