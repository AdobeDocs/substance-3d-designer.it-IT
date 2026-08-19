---
title: Piano
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Piano
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Piano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona piano](./3d-sdf-plane.png "Piano")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un piano di orientamento, posizione e dimensione regolabili.

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
| <b>Normale</b> *Float3* | Il vettore normale dello spazio mondo del piano, che ne controlla l&#39;orientamento.<br>Il vettore è normalizzato.<br><br><i>Impostazione predefinita: (0, 0, 1)</i> |
| <b>Dimensioni</b> *Float2* | Dimensione del piano in X e Y.<br><br><i>Impostazione predefinita: (1, 1)</i> |
| <b>Thickness</b> *Mobile* | Thickness del piano, applicato in tutte le direzioni.<br>Il piano viene arrotondato quando si aumenta il thickness.<br><br><i>Impostazione predefinita: 0</i> |
| <b>Posizione centrale</b> *Float3* | Posizione dello spazio globale del perno del piano.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
