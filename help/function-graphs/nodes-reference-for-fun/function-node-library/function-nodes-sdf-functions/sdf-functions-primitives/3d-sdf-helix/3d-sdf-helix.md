---
title: Elica (ca.)
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Funzione SDF > Di base > Elica (circa)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Elica (ca.)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Elica (circa) icon](./3d-sdf-helix.png "Elica (circa)")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per l&#39;approssimazione di un&#39;elica, ovvero una forma formata da un cerchio lungo una curva che si avvolge lungo una curva verso l&#39;alto attorno a un asse.<br><br><i>Nota:</i>Poiché questa Funzione SDF è un&#39;approssimazione, è possibile che vengano visualizzati artefatti durante il rendering.

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
| <b>Raggio maggiore</b> *Virgola mobile* | Distanza della curva di avvolgimento dall&#39;asse.<br><br><i>Impostazione predefinita: 0.4</i> |
| <b>Raggio secondario</b> *Virgola mobile* | Raggio del cerchio che viene trascinato lungo la curva per formare la superficie dell&#39;elica.<br><br><i>Impostazione predefinita: 0.1</i> |
| <b>Height</b> *Virgola mobile* | Height Z-up dell&#39;elica.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Finestre</b> *Virgola mobile* | Il numero di volte in cui la curva si avvolge completamente attorno all&#39;asse in passaggi di 0,5.<br>Cioè, quante volte l&#39;elica ruoterà all&#39;interno di un height di 0,5.<br><br><i>Impostazione predefinita: 4</i> |
| <b>Posizione centrale</b> *Virgola mobile 3* | Posizione dello spazio globale del fulcro dell&#39;elica.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
