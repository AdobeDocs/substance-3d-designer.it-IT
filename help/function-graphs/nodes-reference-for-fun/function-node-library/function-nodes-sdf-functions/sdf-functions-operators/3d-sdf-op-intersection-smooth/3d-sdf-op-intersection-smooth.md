---
title: Arrotondamento intersezione
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Operatore > Arrotondamento intersezione
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%

---


# Arrotondamento intersezione

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona di smusso dell&#39;intersezione](./3d-sdf-op-intersection-smooth.png "Smussato dell&#39;intersezione")

<b>In:</b> Funzione SDF > Operatore

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Restituisce il volume comune a due forme SDF, in pratica il volume creato quando due forme si sovrappongono, con l&#39;arrotondamento regolabile dei bordi della loro intersezione.

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
| <b>SDF 1</b> *Mobile* | La prima forma SDF. |
| <b>SDF 2</b> *Mobile* | La seconda forma SDF. |
| <b>Smoothness</b> *Mobile* | Smoothness dei bordi in corrispondenza dell&#39;intersezione delle due forme SDF.<br><br><i>Nota:</i> bordi rigidi possono apparire nel punto in cui i raggi di arrotondamento si intersecano.<br><br><i>Impostazione predefinita: 0</i> |
