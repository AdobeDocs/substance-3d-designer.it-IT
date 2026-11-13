---
title: Cono chiuso
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Primitivo > Cono con copertura
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%
---

# Cono chiuso

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona a forma di cono chiuso](./3d-sdf-capped-cone.png "Cono chiuso")

<b>In:</b> Funzione SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Funzione SDF per un cono con estremità chiusa e raggio di base e estremità regolabili.

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
| <b>Base raggio</b> *Virgola mobile* | Raggio della base del cono chiuso.<br><br><i>Impostazione predefinita: 0.5</i> |
| <b>Raggio superiore</b> *Virgola mobile* | Raggio della parte superiore del cono chiuso.<br><br><i>Impostazione predefinita: 0.2</i> |
| <b>Height</b> *Virgola mobile* | Height Z-up del cono con estremità chiusa dalla base.<br><br><i>Impostazione predefinita: 1</i> |
| <b>Posizione centrale</b> *Virgola mobile 3* | Posizione dello spazio globale del perno del cono chiuso.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>P</b> *Virgola mobile 3* | La posizione Trasforma nello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
