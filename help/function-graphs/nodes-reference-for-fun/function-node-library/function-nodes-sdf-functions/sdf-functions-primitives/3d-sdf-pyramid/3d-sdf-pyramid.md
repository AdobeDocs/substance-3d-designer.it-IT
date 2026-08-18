---
title: Piramide
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Piramide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# Piramide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona piramide](./3d-sdf-pyramid.png "Piramide")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Una Funzione SDF per una piramide di height regolabile, dimensioni di base e posizione di base.

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
| <b>Height</b> *Mobile* | Height Z-up dell&#39;apice della piramide dalla base.<br><br><i>Impostazione predefinita: 1</i> |
| <b>Dimensioni base</b> *Float2* | Dimensione della base della piramide in X e Y.<br><br><i>Impostazione predefinita: (1, 1)</i> |
| <b>Posizione di base</b> *Float3* | Posizione nello spazio globale della base della piramide.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
