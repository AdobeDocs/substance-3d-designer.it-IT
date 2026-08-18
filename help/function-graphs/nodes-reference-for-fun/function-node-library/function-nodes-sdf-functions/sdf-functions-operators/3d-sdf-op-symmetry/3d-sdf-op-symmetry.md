---
title: Simmetria
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Funzione SDF > Operatore > Simmetria
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Simmetria

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona simmetria](./3d-sdf-op-symmetry.png "Simmetria")

<b>In:</b> Funzione SDF > Operatore

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Capovolge e duplica una forma SDF su un piano speculare, quindi restituisce l&#39;unione della forma SDF di base e dei suoi duplicati.<br>La simmetria può essere applicata contemporaneamente su tutti gli assi.

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
| <b>Posizione del piano di simmetria</b> *Float3* | Posizione dello spazio mondo del centro del piano dello specchio.<br>Questa posizione è condivisa da tutti i piani speculari se la simmetria viene applicata su più assi.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Asse mirror</b> *Intero3* | Imposta le assi mirrori desiderate.<br><br>Ad esempio, (1, 0, 0) applicherà la simmetria sull&#39;asse X.<br><br><i>Impostazione predefinita: (1, 0, 0)</i> |
| <b>Capovolgi asse</b> *Intero3* | Imposta gli assi da capovolgere.<br><br>Ad esempio, (1, 0, 0) capovolgerà la direzione della simmetria sull&#39;asse X.<br><br><i>Impostazione predefinita: (0, 0, 0)</i> |
| <b>Pre-offset</b> *Float3* | Scostamento sugli assi X, Y e Z applicato alla forma prima di applicare l&#39;operatore di simmetria. |
