---
title: Ripeti intervallo specchio
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Operatore > Ripeti intervallo specchiatura
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Ripeti intervallo specchio

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Ripeti intervallo mirror](./3d-sdf-op-repeat-mirror.png "Ripeti intervallo mirror")

<b>In:</b> Funzione SDF > Operatore

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Riflette e duplica una forma SDF un numero qualsiasi di volte a una spaziatura regolare negli assi positivo o negativo X, Y e Z.<br>Ogni volta che l&#39;operatore ripete una forma, questa viene riflessa. Ciò determina visivamente un&#39;alternanza tra l&#39;orientamento originale della forma e una copia capovolta.

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
| <b>SDF</b> *Mobile* | Forma SDF di input. |
| <b>Importo +</b> *Intero3* | Quantità di duplicazioni lungo gli assi X, Y e Z positivi.<br><br><i>Impostazione predefinita: (2, 0, 0)</i> |
| <b>Importo -</b> *Intero3* | Quantità di duplicazioni lungo gli assi X, Y e Z negativi.<br><br><i>Impostazione predefinita: (2, 0, 0)</i> |
| <b>Spaziatura</b> *Float3* | Spazio mondiale tra ogni duplicato.<br><br>La spaziatura viene visualizzata da un helper cubico, che rappresenta lo spazio tra i duplicati nelle direzioni X, Y e Z. La spaziatura inizia in corrispondenza della <b>posizione di origine</b> e viene aumentata simmetricamente da essa.<br><br><i>Impostazione predefinita: (2, 2, 2)</i> |
| <b>Posizione origine</b> *Float3* | Definisce il centro della forma SDF che verrà duplicata.<br><br>La posizione di origine è visualizzata dalla posizione centrale dell&#39;helper cubico.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
