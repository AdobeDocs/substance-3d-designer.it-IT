---
title: Capovolgi
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Trasforma > Capovolgi
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# Capovolgi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Inverti icona](./3d-sdf-transform-flip.png "Inverti")

<b>In:</b> Funzione SDF > Trasforma

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Applica un Trasforma speculare alla forma SDF di input.<br>Esegue essenzialmente una scala negativa sugli assi selezionati.

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
| <b>Asse mirror</b> *Intero3* | Utilizzare un valore Integer3 per impostare l&#39;asse mirror desiderata.<br>Ad esempio (1, 0, 0) rifletterà l&#39;asse X.<br><br><i>Impostazione predefinita: (1, 0, 0)</i> |
| <b>P</b> *Float3* | La posizione trasformata dello spazio mondiale. Utilizza questo input per applicare trasformazioni aggiuntive utilizzando i nodi <b>Offset P</b> e <b>Rotazione P</b>.<br><br><i>Impostazione predefinita: la posizione dello spazio globale non trasformata.</i> |
