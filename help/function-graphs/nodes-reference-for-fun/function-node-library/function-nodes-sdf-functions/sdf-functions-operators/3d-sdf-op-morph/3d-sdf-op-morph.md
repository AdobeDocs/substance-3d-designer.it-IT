---
title: Morphing
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Operatore > Morphing
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Morphing

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona morphing](./3d-sdf-op-morph.png "Morphing")

<b>In:</b> Funzione SDF > Operatore

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Restituisce l&#39;interpolazione lineare tra una forma SDF di base e una forma SDF di destinazione in base a un fattore di mixaggio regolabile.

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
| <b>SDF di base</b> *Mobile* | La forma SDF di base. |
| <b>SDF di destinazione</b> *Mobile* | La forma SDF di destinazione. |
| <b>Fattore misto</b> *Mobile* | Fattore di mixaggio utilizzato per modificare le forme di input, dove 0 è la forma base e 1 la forma di destinazione. |
