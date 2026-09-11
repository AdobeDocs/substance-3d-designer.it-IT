---
title: Offset P
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Scostamento P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Offset P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Scostamento P](./3d-sdf-transform-offset-p.png "Scostamento P")

<b>In:</b> Funzione SDF > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Sposta lo spazio globale lungo un vettore.<br>La posizione del mondo Trasforma per l&#39;output può essere collegata all&#39;input <b>P</b> della maggior parte delle Funzioni SDF per definirle in questo spazio del mondo Trasforma.<br><br><i>Suggerimento:</i> I Trasforma P possono essere concatenati, ma tenete presente che i risultati dipendono dall&#39;ordine delle operazioni.

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
| <b>Scostamento</b> *Float3* | Distanza di offset dello spazio globale nelle direzioni X, Y e Z. |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
