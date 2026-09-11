---
title: Imposta materiale
description: Impostate il colore di base, la ruvidità e la metallizzazione del materiale di una scena SDF.
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# Imposta materiale

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Imposta icona materiale](set-material.png "Imposta materiale")

<b>Ingresso:</b> Funzione 3D > Materiale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Impostate il colore di base, la ruvidità e la metallizzazione del materiale di una scena SDF.

Questi valori possono quindi essere recuperati per tutte le forme SDF suddivise negli output dello splatter [Forma v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md).

</td>
</tr>
</table>

>[!INFO]
> 
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../working-with-sdf-functions.md)

## Input

|                            |                                  |
|----------------------------|----------------------------------|
| <b>Scena SDF</b> *Mobile* | Scena SDF di input. |
| <b>Colore di base</b> *Float3* | Il valore del colore di base di RGB da impostare. |
| <b>Metallicità</b> *Mobile* | Valore di metallizzazione da impostare. |
| <b>Rugosità</b> *Mobile* | Valore di rugosità da impostare. |
