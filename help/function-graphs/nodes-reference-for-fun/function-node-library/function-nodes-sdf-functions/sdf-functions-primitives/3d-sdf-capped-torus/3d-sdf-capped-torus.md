---
title: Toro chiuso
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Primitivo > Toro con limiti
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Toro chiuso

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona toro con copertura](./3d-sdf-capped-torus.png "Toro con copertura")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un toro con cappuccio, in cui l&#39;apertura del cerchio minore lungo un cerchio principale può essere chiusa da un angolo.<br>Entrambi i cerchi hanno raggi regolabili.

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
| <b>Raggio maggiore</b> *Mobile* | Raggio del cerchio principale lungo il quale viene effettuato lo sweep del cerchio secondario per formare la superficie del toro.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio secondario</b> *Mobile* | Raggio del cerchio minore che viene trascinato lungo il cerchio principale per formare la superficie del toro.<br><br><i>Impostazione predefinita: 0.2</i> |
| <b>Angolo</b> *Mobile* | Angolo centrale, in giri, che definisce l&#39;arco di rifilatura del cerchio principale lungo il quale il cerchio secondario non verrà spostato.<br><br><i>Impostazione predefinita: 0.75</i> |
| <b>Scostamento angolo</b> *Mobile* | Offset lungo il raggio principale dell&#39;arco di rifilatura lungo il quale il cerchio secondario non verrà spostato.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Simmetrico</b> *Booleano* | Controlla se l&#39;arco di rifilo deve essere disegnato in una o due direzioni.<br><br><i>Impostazione predefinita: True</i> |
| <b>Posizione centrale</b> *Float3* | Posizione nello spazio globale del perno del toro con cappuccio.<br><br><i>Impostazione predefinita: (0, 0, 0,5)</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
